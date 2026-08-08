# `naserrouhi/resume.json`

> **Senior Software Engineer** · .NET · Backend · Distributed Systems · Clean Architecture

[![JSON Resume](https://img.shields.io/badge/format-JSON%20Resume-00A98F?style=for-the-badge&logo=json&logoColor=white)](https://jsonresume.org/)
[![.NET](https://img.shields.io/badge/.NET-8%2B-512BD4?style=for-the-badge&logo=dotnet&logoColor=white)](https://dotnet.microsoft.com/)
[![Open to Relocation](https://img.shields.io/badge/status-open%20to%20relocation-1f883d?style=for-the-badge)](#)
[![Validate JSON](https://img.shields.io/badge/CI-validate%20resume-blue?style=for-the-badge&logo=githubactions&logoColor=white)](#)

A developer-friendly, machine-readable version of my resume.

Instead of keeping my career only in a PDF, this repository treats it like software: **structured, versioned, reviewable, and automatable**.

```json
{
  "name": "Naser Rouhi",
  "role": "Senior Software Engineer",
  "experience": "8+ years",
  "specialties": [
    ".NET / ASP.NET Core",
    "Clean Architecture",
    "Microservices",
    "CQRS / DDD",
    "High-performance APIs",
    "Distributed systems"
  ],
  "status": "open-to-relocation"
}
```

## `whoami`

I build and scale backend-heavy web applications across finance, aviation, healthcare, transportation, and EHS products. My work centers on **.NET/C#**, architecture, data-intensive systems, observability, messaging, and maintainable engineering practices.

A few numbers from the resume:

- `70%` faster reporting/query workloads
- `80%` faster vehicle search with Elasticsearch
- `99.9%` data synchronization
- `40%` revenue growth after a product launch
- `40%+` faster issue resolution with ELK observability

## Repository map

```text
.
├── resume.json
├── README.md
├── package.json
└── .github/
    └── workflows/
        └── validate-resume.yml
```

## Use the data

### Inspect it

```bash
cat resume.json
```

### Query it with `jq`

```bash
# Current title
jq -r '.basics.label' resume.json

# Companies
jq -r '.work[].name' resume.json

# Skill groups
jq -r '.skills[] | "\(.name): \(.keywords | join(", "))"' resume.json
```

### Render with JSON Resume

```bash
npm install
npm run validate
npm run export
```

This generates an HTML resume from the same source of truth.

## Engineering stack

| Area | Stack |
|---|---|
| Back-End | .NET, ASP.NET Core, EF Core, LINQ, REST, SignalR, Blazor, ELSA |
| Architecture | Clean Architecture, Microservices, CQRS, DDD, SOLID |
| Data | SQL Server, PostgreSQL, MongoDB, Oracle, Elasticsearch, Redis |
| Messaging | RabbitMQ, Kafka |
| Front-End | ReactJS, Razor, jQuery |
| DevOps | Docker, CI/CD, Git, Azure, AWS, ELK |
| Practices | TDD, BDD, Unit & Integration Testing, AI-assisted development |

## Selected systems

**EHS Suite** — modular REST APIs, offline sync, Redis, ELK  
**Arobus** — B2C ticketing, microservices, DDD  
**Rebook Pump** — airline rebooking and fuel management  
**Bookkeeping Platform** — large-scale financial reporting, CQRS, Redis  
**Agah LMS** — financial education platform, DDD, TDD

## Why JSON?

Because a resume can be more than a document.

```text
PDF      → human-readable
JSON     → machine-readable
Git      → version history
CI       → validation
GitHub   → public engineering artifact
```

The goal is simple: **one source of truth for my professional profile**.

---

### Contact

- LinkedIn: https://www.linkedin.com/in/naser-rouhi-nomonia/
- GitHub: https://github.com/naserrouhi
- Email: naserrouhi.nomonia@gmail.com
- Location: Tehran, Iran
- Status: Open to relocation

> Professional work is primarily in private repositories and may be covered by NDA. This repository contains public resume information only.
