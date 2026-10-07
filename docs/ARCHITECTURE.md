# Architecture Overview

```text
Operator / Human Gates
        |
        v
ULTRON Runtime / Commander
        |
        +--> Job + Schedule State
        |       |
        |       +--> SQLite / JSON
        |
        +--> Local LLM Inference
        |       |
        |       +--> Ollama
        |
        +--> Application / Research Workflows
        |
        +--> Marketing / Publishing Workflows
        |
        +--> Payment Observation
        |       |
        |       +--> Stripe
        |
        +--> Notifications
                |
                +--> Twilio
```

## Design notes

- Local work can proceed automatically when QA passes.
- External sends, submissions, contracts, spending, identity, and account actions remain human-gated.
- Payment and payout states are not collapsed into a single “money” status.
- Public portfolio material is separated from production source and operational data.
