# Backend engineering challenge (2026 edition)

## Overview
Build a small integration service that ingests raw data from external sources and sends it to Databox using the Ingestion API. The goal is to demonstrate sound engineering practices, clear reasoning, and appropriate tradeoffs.

There is no single correct solution. The solution approach is as important as the final result.

---

## Goal
Create a service that:
- Collects raw data from external APIs or open data sources
- Defines a dataset schema for the ingested data
- Pushes raw data to Databox via the Ingestion API
- Creates metrics from the raw data in the Databox app and adds them to a databoard

The service should be designed with extensibility in mind.

---

## Requirements
- Ingest raw data from one or more external sources (sufficient to manually create 3–5 meaningful metrics in the Databox app)
- Define and document the dataset schema
- Push raw data to Databox
- Create metrics and a databoard in the Databox app and provide a shareable link
- Include basic local logging:
  - Service provider
  - Time of sending
  - Data sent (rows and columns)
  - Success or failure
  - Error message if applicable
- Include basic demonstration data
- Include instructions to run the service

Metrics are created manually in the Databox app; they are not expected to be created programmatically.

---

## Technology
- Use PHP, .NET, or TypeScript
- Any frameworks or libraries may be used
- Example APIs: GitHub (OAuth2), Asana, Strava, or similar

---

## Level specific expectations

**Junior**
- One data source is sufficient
- Focus on correctness and code clarity
- Minimal tests are acceptable

**Mid level**
- Two data sources
- Basic extensibility
- Meaningful tests
- Clear structure and error handling

**Senior**
- Two or more data sources
- At least one OAuth2 integration
- Extensible architecture
- Discussion of tradeoffs, scalability, and configurability

---

## Submission
- We expect the solution to be submitted within **one week**, unless agreed otherwise.
- If the repository is private, grant read access to the GitHub users **tadejrola** and **sparkica**
- Provide a link to a Git repository
- Include setup and run instructions
- Include a shareable Databox databoard link
- Include the email used for Databox signup

---

## Intellectual property
This repository contains only the challenge description. Candidate submissions remain the candidate’s intellectual property and will not be used in production.

---

## Notes
Be concise when describing decisions and alternatives. Partial solutions with clear reasoning are acceptable.

