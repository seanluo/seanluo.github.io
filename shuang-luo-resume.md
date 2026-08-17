# Shuang Luo

Software Architect / Senior Full Stack Engineer

Shanghai, China | imluoshuang@gmail.com

---

## Summary

Software architect with 13 years building production systems in telecom identity and anti-fraud (STIR/SHAKEN, SIP, caller ID), fintech lending, and consumer-scale infrastructure at Tencent and JD.com. Designs the architecture and writes the code that ships it. Works both sides of AI-agent infrastructure: production MCP servers behind OAuth, and agent-assisted delivery at volume. Strongest on regulated domains, high-volume integrations, and correctness at system boundaries.

---

## Skills

**Domain:** STIR/SHAKEN call authentication, SIP signaling, PKI and certificate lifecycle, telecom anti-fraud, loan origination

**AI engineering:** MCP servers and tool schemas, OAuth-protected agent access, agent-assisted development (Claude Code, Codex), AGENTS.md context contracts

**Languages:** Go, Python, TypeScript

**Backend:** PostgreSQL, Redis, DynamoDB, Django and DRF, Node.js, Effect-TS, microservices, distributed job pipelines

**Frontend:** React, Next.js, Tailwind

**Platform:** AWS (Lambda, SQS, S3, RDS, EC2, VPC, Route 53, CloudFront, CloudFormation), Docker, nginx, CI/CD, OpenTelemetry, Grafana

---

## Experience

### Spectra Capital, LLC
**Senior Full Stack Software Engineer** | 12/2024 - 07/2026 | Shanghai, China (remote, US team)

Commercial lending platform: origination, underwriting, and servicing.

- Largest single contributor to a 5,042-commit TypeScript monorepo, with 1,198 commits over 19 months on a multi-person team.
- Led the shared-package boundary architecture separating runtime-neutral, frontend-only, and backend-only code, enforced by lint in CI rather than by convention.
- Led whole-monorepo upgrades to Node 24 with full ESM, TypeScript 6, and pnpm 11, and replaced fire-and-forget background work with an SQS-backed job pipeline that is retryable and observable.
- Designed the OpenTelemetry tracing conventions that auto-instrument 100+ database methods and 60+ external service calls, so production latency is diagnosed from a trace instead of a guess.
- Built the MCP server exposing the platform to AI agents, secured by full OAuth rather than a shared API key, with presigned direct-to-S3 upload for large documents.
- Authored the agent context contracts (AGENTS.md, CLAUDE.md) codifying architecture rules, test layout, and invariants, so coding agents and new engineers work from the same brief. Shipped production code at volume with agent tooling alongside conventional review.
- Integrated roughly two dozen third-party services across banking data, credit, CRM, identity, and e-signature. Implemented role-based access control on every API endpoint and ran the dependency-patching and vulnerability-review cadence.

### Neustar Inc., acquired by TransUnion
**System Architect** | 12/2020 - 11/2024 | Virginia, US and Shanghai, China
*Principal Software Engineer, 12/2020 - 03/2022*

Core member of the Communications Solutions Innovation Team, building nationwide call-authentication infrastructure.

- Designed and built the STIR/SHAKEN Interoperability Test Automation Platform, replacing manual cross-carrier testing with a repeatable automated suite.
- Prototyped STIR for Messaging, extending signed-identity guarantees from voice to SMS.
- Drove integration of nationwide call authentication and verification across Brazilian carriers, working through per-carrier signaling differences at national scale.
- Owned the certificate lifecycle underpinning SHAKEN (CA generation, signing, revocation, CRL, verification), hands-on with SIP across Oracle SBC, Kamailio, and Asterisk.

### Telo USA, Inc.
**Vice President of Technology** | 09/2016 - 12/2020 | Atlanta, GA

Led cross-functional engineering teams while remaining the lead full stack engineer on core products.

- Owned three revenue products end to end: **OpenCNAM**, a caller-ID platform with REST, SS7/SIGTRAN, ENUM, and SIP interfaces; **EveryoneAPI**, a reverse phone append API for fraud prevention; and the **OpenCNAM Storage Platform**.
- Architected high-availability, low-latency services against an explicit cost-per-query target, and standardized build and deployment across dev, test, and production.
- Introduced a microservices architecture with a decoupled frontend and backend, using AWS SQS for asynchronous processing.
- Built the monitoring stack on CloudWatch, InfluxDB, and Grafana, plus an invoicing system integrated with external financial platforms.

### Tencent Technology
**Software Engineer** | 05/2015 - 05/2016 | Shanghai, China

- Built web features and promotional campaigns for Tencent's gaming portfolio in the Operations Department of Interactive Entertainment Group (IEG).

### Tencent E-Commerce (ECC), acquired by JD.com
**Software Engineer** | 04/2013 - 05/2015 | Shanghai, China

- Built the cross-platform monitoring agent (Windows and Linux) for in-warehouse PCs and servers, with centralized remote deployment and updates.
- Led DevOps for the mobile division of one of China's largest B2C platforms: the Configuration Management Database (CMDB) that gave it a single source of truth for infrastructure, plus server monitoring and a status-code system that turned silent HTTP error spikes into actionable alerts.

---

## Selected Projects

### Licensed data platform for air pollutant research (university research lab)
**Sole architect and author** | 2022 - 2026 | Django, DRF, React, Docker

- Async job engine running numpy/scipy matching, and geocoding of Chinese addresses across Baidu, Gaode, and Tianditu, with per-vendor rate-limit throttling and conversion between Chinese and international coordinate systems.
- Designed the commercial layer from scratch: signed license files, per-installation activation, feature gates, a charge ledger with prepaid reservations, and settlement reconciliation that survives delivery succeeding while billing fails. 1,067 tests, zero type-checker errors enforced at merge.

### Public air quality health service (airhealthindex.org)
**Sole author** | 2025 - 2026 | Go, PostgreSQL

- Hourly health indices for cities across China on the Go standard library with one external dependency. When the upstream data feed is late, the cache serves the previous hour's snapshot rather than an error page.
- Map provider is selected automatically, with fallback, so the site stays compliant with Chinese mapping regulation and usable from outside China. Dual .org and .cn deployment with versioned releases, one-command rollback, and Chinese ICP registration.

---

## Education

**Nanjing University of Science and Technology** | Nanjing, China

- Master of Engineering, Computer Science | 2010 - 2013
- Bachelor of Engineering, Mechanical Engineering; Bachelor of Economics | 2005 - 2011
