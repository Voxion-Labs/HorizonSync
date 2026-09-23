# HorizonSync Operational & Contribution Protocols

HorizonSync operates under strict full-stack architectural and relational database constraints. We do not accept unoptimized React renders, insecure Server Actions, or schema mutations that break real-time synchronization. This repository is maintained as a proprietary, high-performance team collaboration platform.

If you intend to submit a Pull Request, you must adhere strictly to the following institutional directives.

## 1. Architectural Standards
All code submitted to HorizonSync must meet our baseline performance and security metrics:
* **Real-time Integrity:** Any modifications to the Pusher event fanout system must guarantee sub-millisecond delivery and zero message duplication.
* **Database Relational Strictness:** Changes to the Prisma schema require explicit, reversible migration paths. Orphaned relational data or unoptimized queries on the PostgreSQL layer will result in immediate rejection.
* **Component Isolation:** Ensure Next.js Server Components and Client Components are strictly delineated. Do not leak server secrets to the client bundle.

## 2. Pull Request (PR) Governance
Before initiating a merge request, ensure your PR adheres to this exact structure:
1. **[METRIC] Benchmark Data:** Provide before/after execution telemetry (e.g., Server Action latency, Prisma query execution time, initial page load metrics).
2. **[LOGIC] State Transition:** Explicitly document changes to the NextAuth session payload, UploadThing file handling, or AI drafting system prompts.
3. **[ISOLATION] Threat Model:** Prove that your modifications do not introduce Cross-Site Scripting (XSS) in Hubs messaging or expose private My Space documents to unauthorized users.

*Note: PRs failing to provide empirical telemetry or violating the full-stack isolation constraints will be closed immediately without review.*

## 3. Vulnerability Disclosure
**DO NOT** open public issues for authentication bypasses, real-time message hijacking, or database injection vulnerabilities. Public disclosure of critical threats compromises the integrity of the platform.
* All security reports must be routed internally.
* Contact the Lead Architect directly for secure transmission protocols.

## 4. Code of Conduct
We evaluate algorithmic efficiency and architectural integrity, not intentions. Your submissions will be scrutinized ruthlessly based on full-stack optimization and system determinism. Keep discussions clinical, objective, and exclusively focused on system architecture.