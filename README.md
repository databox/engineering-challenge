# Backend engineering challenge

## Overview
This challenge is designed to assess how you approach building a small but realistic integration service. The goal is not only to produce working code, but to demonstrate sound engineering judgment, clear reasoning, and pragmatic decision making.

The assignment is intentionally open ended. There is no single correct solution. We are primarily interested in how you think, structure problems, and explain tradeoffs.


## Goal
Build a service that extracts **raw data** from external data sources and sends it to the Databox platform using the Databox Ingestion API.

From the ingested raw data, you will then create metrics **inside the Databox app** (rather than pushing metrics directly via the API).

The service should be designed with extensibility in mind, as if it were the starting point for a production integration.


## Core requirements (all levels)
These requirements apply to all candidates, regardless of seniority. Depth and completeness expectations vary by level and are described below.

- Extract raw data from external APIs or open data sources
- Define a **dataset schema** for the raw data you will send (fields and data types)
- Push the extracted raw data to Databox using the Ingestion API
- In the Databox app, create **metrics derived from the raw data** and add them to a Databox databoard
- Provide a shareable link to the databoard
- Include basic local logging of:
  - Service provider
  - Time of sending
  - Data sent (rows and columns)
  - Success or failure
  - Error message if applicable
- Provide basic demonstration data
- Include instructions on how to run the service locally

Schema should be treated as a first class artifact. Document how source data maps to your dataset schema.


## Technology constraints
- Use one of the following languages: PHP, .NET, or TypeScript
- You may choose any framework or libraries you feel are appropriate
- Use external APIs such as GitHub, Asana, Strava, or another comparable service


## Time expectations
We aim to be respectful of your time.

- Expected effort is approximately 4 to 8 hours, depending on level and scope
- You do not need to implement everything perfectly
- Partial solutions with clear reasoning and good structure are acceptable

If you feel the scope is too large for the time you have available, document what you would do next and why.


## Level specific expectations

### Junior engineers
Focus on correctness, clarity, and fundamentals.

Expected scope:
- One data source is sufficient
- OAuth is not required
- Simple, readable structure with clear separation of concerns
- Basic error handling
- Minimal tests are acceptable

What we evaluate:
- Code readability and organization
- Ability to follow API documentation
- Basic understanding of data flow and schema definition
- Willingness to explain decisions and assumptions

Architecture documentation is optional and can be brief.


### Mid level engineers
Focus on solid execution and maintainable design.

Expected scope:
- Two data sources
- Clearly defined dataset schema
- Basic extensibility, for example adding another integration without major refactoring
- Meaningful unit tests
- Clear deployment and run instructions

What we evaluate:
- Clean abstractions and separation of responsibilities
- Thoughtful error handling and logging
- Test strategy and coverage choices
- Ability to explain tradeoffs and constraints

A short architecture or design explanation is expected.


### Senior engineers
Focus on judgment, tradeoffs, and system design.

Expected scope:
- Two or more data sources
- At least one integration using OAuth2
- Well designed dataset schema with evolution in mind
- Architecture designed for extensibility and future growth
- Discussion of configurability, scalability, and operational concerns
- Reasonable testing strategy, not just coverage numbers

What we evaluate:
- Quality of architectural decisions
- Ability to scope appropriately and avoid over engineering
- Clear articulation of alternatives and tradeoffs
- Production minded thinking, including observability, failure modes, and deployment

A clear architecture and decision narrative in markdown is required.


## Optional considerations (primarily senior level)
- Expose functionality via API endpoints
- Periodic or scheduled data sending and reasoning behind the chosen approach
- Ideas for scaling, configuration management, or future optimizations

You may describe these without fully implementing them.


## Submission instructions
- We expect the solution to be submitted **within one week**, unless agreed otherwise.
- Provide a link to a Git repository with your solution
- Include:
  - Instructions to run the service
  - Any setup steps or configuration required
  - A shareable Databox databoard link
  - The email address used to sign up for Databox

If the repository is private, grant read access to the specified reviewers: `tadejrola`, `sparkica`


## Evaluation philosophy
We value clarity of thought over completeness. We would rather see a smaller, well reasoned solution than a large, rushed one.

During follow up discussions, we will focus on:
- Why you made certain decisions
- What you would change with more time
- How you would evolve the solution in a real production environment

Good luck. We look forward to reviewing your work.

## Final note on intellectual property

This repository contains only the challenge description. Candidate submissions remain the candidate’s intellectual property and will not be used in production.
