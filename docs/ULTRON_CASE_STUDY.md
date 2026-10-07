# ULTRON / AI Agent Farm — Sanitized Case Study

## Problem

I wanted a local AI system that could do more than generate text. The goal was to coordinate research, drafting, QA, application preparation, payment monitoring, notifications, and recovery without treating every automated step as a completed business outcome.

## What I built

A Windows-based multi-agent workflow system using Python and local LLM inference.

### Core technologies

- Python 3
- Ollama / local LLMs
- REST APIs
- JSON
- SQLite
- Git / GitHub
- Windows background processes
- Stripe
- Twilio
- Wix
- Gmail-connected workflows

## Engineering principles

### 1. Human-in-the-loop boundaries

The system separates local preparation from external actions. A draft is not a send. An application package is not a submitted application. A checkout is not a paid transaction.

### 2. Truth-state tracking

Important money and application states are recorded separately:

- identified
- qualified
- prepared
- submitted
- reply received
- payment observed
- available balance
- payout
- bank arrival

### 3. Failure recovery

I added background watchdogs, startup processes, retry handling, local state, and focused tests so the system could recover from crashes and avoid requiring a manual “next step” after every task.

### 4. Link quality controls

After stale marketplace and expired application links surfaced during early iterations, I added hard source blocks and a current-run HTTP application-page probe. Broken, expired, generic-career-page, and blocked marketplace links are rejected before application handoff.

### 5. Local-first inference

The system uses local Ollama models for core inference so the automation can continue without a paid inference API dependency.

## Representative workflows

- direct-employer role discovery and application-pack preparation
- marketing research and content production
- QA/review gates
- Stripe direct-product payment observation
- buyer delivery handoff
- SMS alerts for meaningful human gates
- owned Wix content publishing
- runtime recovery and scheduled checks

## What this demonstrates

This project reflects my ability to:

- turn broad goals into operational workflows
- connect APIs and local tools
- design prompts and state machines
- test and debug automation
- identify failure loops
- add safety/approval boundaries
- improve systems based on real operational failures

## Privacy

The production repository is intended to remain private. This public case study deliberately omits credentials, private prospect/application data, full internal configs, and proprietary runtime implementation.
