# Tech Stack Evaluation

## Project
Web-Based Campus Shuttle Route Recommendation System

## Requirements that drive the decision
List 3 to 5 requirements from your own docs/requirements.md. Include at
least 2 non-functional requirements.
- [FR 1]: [The system shall ...]
- [FR 2]: [The system shall ...]
- [FR 3]: [The system shall ...]
- [NFR 1]: [The system shall ...]
- [NFR 2]: [The system shall ...]
## Options
- Option A: Static Client-Side
- Option B: Python Microservice + Cloud Host
- Option C: Full-Stack Jamstack / Serverless

## Decision matrix
Weight: how important the criterion is for YOUR project (1 = low, 5 = high).
Score: how well each option does (1 = poor, 5 = excellent).
Weighted score = weight x score. Add them up for each option.

| Criterion                          | Weight | A score | B score | C score |
|------------------------------------|--------|---------|---------|---------|
| Fits my requirements               |    4   |    2    |    5    |    4    |
| Skills I already have              |    4   |    4    |    5    |    3    |
| Time to build before my deadline   |    5   |    5    |    4    |    2    |
| Free hosting and tools             |    5   |    5    |    3    |    4    |
| Performance and security needs     |    3   |    3    |    4    |    4    |
| Room to grow later                 |    2   |    1    |    4    |    5    |
| **Total (weighted)**               |   23   |   78    |   94    |   79    |

## Decision record
- **Context:** Need to deliver a functional project prototype within semester deadlines with zero hosting budget, leveraging existing Python programming skills while meeting both functional and non-functional requirements.
- **Decision:** Python Web App (FastAPI/Flask) with PostgreSQL hosted on Render's free tier.
- **Reasons:** 
1. Achieved the highest weighted score (94), directly matching existing Python proficiency to reduce onboarding time.
2. Fully supports dynamic backend logic, relational data storage, and unit testing workflows via pytest.
3. Provides a zero-cost cloud deployment option with an official managed database.
- **Consequences:** 
What becomes easy: Writing backend logic, testing core algorithms with pytest, and maintaining relational integrity.
What becomes harder: Managing cold starts and spin-down delays on Render’s free tier after inactivity.
- **Risks and next review:**
Risk: Free-tier compute limits or database inactivity pauses during final presentation grading.
Review: Test deployment latency one week before submission; if spin-down is unacceptable, implement a lightweight keep-alive or fall back to an SQLite container.
