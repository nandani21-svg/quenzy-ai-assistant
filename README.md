# Quenzy

A serverless AI Q&A application built on AWS — ask any question and get an instant, live AI-generated answer.

## What it does
Quenzy is a personal AI assistant that answers questions in real time using a fully serverless AWS architecture. Type a question, and it's routed through a real cloud pipeline to a foundation model, with the answer streamed back into a clean chat interface.

## Architecture
User → API Gateway → AWS Lambda → Amazon Bedrock (Nova) → Response
## Tech stack
- **AWS Lambda** — serverless compute running the core logic (Python)
- **Amazon API Gateway** — public HTTP endpoint with CORS and rate limiting
- **Amazon Bedrock** — foundation model inference (Amazon Nova)
- **IAM** — least-privilege permissions between services
- **HTML/CSS/JavaScript** — lightweight, dependency-free frontend

## What I learned
Building this taught me real-world cloud debugging — not just following a tutorial. I worked through:
- CORS preflight failures caused by conflicting headers between Lambda and API Gateway
- IAM permission scoping for Lambda-to-Bedrock access
- Model deprecation and versioning issues on Bedrock
- Reading CloudWatch logs to trace failures end-to-end
- Adding throttling to protect a public endpoint from abuse

## Try it
Download `quenzy.html` and open it in your browser — it connects live to a deployed AWS backend.
