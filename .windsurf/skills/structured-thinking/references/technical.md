# Technical / Engineering Framework

## Phases

### Phase 1: Define & Scope
Understand requirements and constraints before writing a line of code.
- Tasks: Gather requirements, define success criteria, assess technical constraints, research existing solutions
- Subtasks: Write functional and non-functional requirements, identify stakeholders and their needs, define performance/scale targets, survey existing libraries/frameworks/APIs, document assumptions and open questions

### Phase 2: Design & Architecture
Make key technical decisions upfront to avoid costly refactoring.
- Tasks: Design system architecture, define data models, choose tech stack, plan integrations
- Subtasks: Draw system diagram (components, services, data flow), define API contracts or interfaces, choose database and data model, identify third-party dependencies, document architecture decision records (ADRs), review for security and scalability concerns

### Phase 3: Build (Core Implementation)
Implement the core functionality in a structured, testable way.
- Tasks: Set up project scaffolding, implement core features, write tests, do code reviews
- Subtasks: Initialize repo and CI/CD pipeline, implement feature by feature (not layer by layer), write unit/integration tests alongside code, set up logging and error handling, conduct peer code reviews

### Phase 4: Test & Harden
Verify the system works correctly, handles failure, and performs under load.
- Tasks: End-to-end testing, performance testing, security review, edge case handling
- Subtasks: Write E2E test suite for critical paths, run load/stress tests against targets, conduct security scan or review, test all error states and edge cases, fix identified issues and re-test

### Phase 5: Deploy & Operate
Ship to production and ensure the system runs reliably over time.
- Tasks: Set up production infrastructure, deploy, monitor, document
- Subtasks: Configure production environment and secrets, define deployment process (CI/CD, blue-green, etc.), set up monitoring and alerting, write runbooks for common incidents, document system for future maintainers, define on-call or support process

## Key Risks to Surface
- Under-specified requirements leading to rework
- Choosing tech based on hype, not fit
- Skipping architecture for "just get it working" and accumulating technical debt
- Insufficient test coverage — finding bugs in production instead of development
- No monitoring — flying blind after launch
- Underestimating deployment and ops complexity

## Type-specific notes
- APIs: Define the contract (OpenAPI spec, etc.) before building — consumers depend on it
- Data pipelines: Plan for failure and idempotency from the start
- Infrastructure/DevOps: Automate everything from day one; manual processes don't scale
- Mobile apps: Platform-specific constraints (App Store review, OS permissions) need early planning
- ML systems: Data quality and labeling pipelines are often harder than the model itself
