# STRIDE Threat Model for LLM Guardrails on AWS & GCP

This repo documents a STRIDE-based threat model for Large Language Model (LLM) applications with guardrails, deployed on AWS and GCP. It focuses on:
- Input/output guardrails
- Tool / API permissioning
- Sensitive data protection
- Observability and governance

## Contents

- `docs/architecture-aws.md`: Reference architecture on AWS (API Gateway / ALB, ECS/EKS or Lambda, Bedrock, RDS/DynamoDB, KMS, CloudWatch).
- `docs/architecture-gcp.md`: Reference architecture on GCP (Cloud Endpoints / API Gateway, GKE/Cloud Run, Vertex AI, Cloud SQL/Firestore, KMS, Cloud Logging).
- `models/stride-llm-common.md`: Common STRIDE threats and mitigations for LLM guardrails.
- `models/stride-llm-aws.md`: AWS-specific threats and mitigations.
- `models/stride-llm-gcp.md`: GCP-specific threats and mitigations.
- `tables/*.csv`: Tabular versions of the threat models for import into tools.

The model assumes:
- User traffic via HTTPs APIs.
- Orchestrator / guardrail service in front of LLM endpoints.
- Tools and data sources accessed via a controlled gateway.
