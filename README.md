# Hey, I'm Vannessa 👋

CS/IT student and founder building **Spectre Security** — 
AI runtime security infrastructure for LLM applications.

## Why I'm building this

Every company shipping AI products right now is flying blind on security.
There's no standard tooling for testing LLM applications against adversarial 
attacks, and no lightweight runtime protection layer built specifically for 
LLM traffic.

Traditional security tools — pen testing, WAFs, DLP systems — were designed 
for web apps and file systems. None of them understand prompts, responses, 
system instructions, or model behavior. The attack surface for LLM 
applications is completely different and nobody had built the right tools for it.

So I built them.

## What I noticed in the AI security space

- Most teams shipping LLM features have never run a formal security audit
- Prompt injection, jailbreaks, and data exfiltration from LLMs are already 
  happening in production — most teams don't know until it's too late
- The EU AI Act is law. NIST published its AI RMF. OWASP published its LLM 
  Top 10. No tools map real scan findings to these frameworks automatically
- We scanned a raw GPT-4 endpoint and found **22 critical vulnerabilities 
  in 4 minutes** — DAN jailbreak accepted, prompt injection succeeded, 
  system prompt extraction attempted. Grade F.

## What I built

**[Spectre Security](http://3.138.193.24:3000)** — two products, one platform:

🔍 **Spectre Scanner** — fires 43 adversarial attacks across 5 threat 
categories at any LLM endpoint. Returns a security grade (A–F), severity 
breakdown, and a PDF report with OWASP LLM Top 10 mapping and remediation 
guidance. Full scan completes in under 5 minutes.

🛡️ **Spectre Shield** — Python SDK that wraps any LLM call with one import. 
Inspects every prompt and response in real time against 67 detection rules — 
credential leakage, injection attempts, jailbreak patterns, and custom DLP 
policies. Under 30ms p95.

## Who this helps

- **Engineering teams** shipping LLM products who need a security audit 
  before launch
- **Security engineers** at companies adopting AI who need structured 
  tooling for LLM threat assessment
- **CISOs** who need compliance documentation — OWASP LLM Top 10, 
  NIST AI RMF — generated automatically from real scan results
- **AI startups** who need to answer "how do you secure your LLM?" 
  in enterprise sales conversations

## Current state

- ✅ 43 attacks across 5 categories
- ✅ 67 Shield detection rules
- ✅ 85/85 unit tests passing
- ✅ Deployed on AWS
- ✅ OWASP LLM Top 10 mapped to every finding
- ✅ Self-serve signup with magic link auth

## Stack
Python · FastAPI · Next.js · TypeScript · PostgreSQL · Redis · 
Celery · Docker · AWS EC2

## Background
CS/IT student · full-stack developer · previously built digital 
identity applications and marketplace platforms · currently focused 
on AI security infrastructure
