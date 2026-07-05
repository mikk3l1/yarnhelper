# Yarn Helper Web App Constitution
<!-- Sync Impact Report
- Version change: 0.1.0 → 1.0.0
- Modified principles: Initial draft formalized into five enforceable principles
- Added sections: Core Principles, Product Constraints, Development Workflow
- Removed sections: None
- Templates requiring updates: ✅ .specify/templates/plan-template.md, ✅ .specify/templates/spec-template.md, ✅ .specify/templates/tasks-template.md
- Follow-up TODOs: None
-->

## Core Principles

### I. Frontend-First Delivery
The product MUST remain usable as a frontend-only web app in the initial release. New features MUST avoid requiring a backend unless a frontend-only solution is demonstrably insufficient for the user need. When a backend dependency appears necessary, the team MUST document the tradeoff and prefer a lightweight workaround before implementing server-side infrastructure.

### II. Data Resilience and Adapter-Based Integration
The app MUST function with local, static, or embedded data as its default source of truth. Public APIs MAY be used only as optional adapters, never as a required dependency for core recommendation behavior. If external data is unavailable, the system MUST degrade gracefully and still provide useful guidance based on available local data.

### III. Explainable Recommendations
Every yarn suggestion MUST include a clear explanation of why it was recommended. The system MUST surface the comparison criteria used, such as meterage, weight class, fiber type, and estimated similarity, so users can understand the recommendation rather than receiving a black-box result.

### IV. Simplicity Over Scope
The initial product MUST prioritize an MVP that solves the core substitution problem quickly and clearly. Features that expand scope, add account systems, or introduce complexity without improving the core task MUST be deferred unless they are explicitly required for the MVP.

### V. Explicit Assumptions and Testable Behavior
The team MUST make assumptions explicit when data is incomplete or uncertain. Product changes MUST be expressed in testable terms, including user-visible outcomes and fallback behavior, so the app can be validated without relying on unstated assumptions.

## Product Constraints

The project MUST remain aligned with these boundaries:
- Frontend-only delivery for the initial version
- No paid services or backend dependency required for core functionality
- Static or local data preferred over fragile external integrations
- Focus on yarn substitution and comparison, not a full yarn encyclopedia
- Limited or incomplete data MUST still produce useful, transparent output

## Development Workflow

All work on this project MUST follow a deliberate delivery sequence:
- Define the user problem and scope before implementation
- Capture assumptions and open questions explicitly before making implementation choices
- Prefer simple, modular code over premature abstraction
- Keep computation logic separate from UI logic so recommendations remain testable
- Validate changes against the primary user journey: enter a yarn or pattern, review alternatives, and understand the recommendation

## Governance

This constitution supersedes informal product preferences for this project. Any change to scope, architecture, or quality expectations MUST be documented, reviewed, and versioned before implementation. Changes that materially alter the product direction, backend strategy, or the MVP boundary MUST be approved through a documented review and reflected in the constitution before work proceeds.

All implementation work MUST verify compliance with these principles before release. If a proposed change conflicts with this constitution, the team MUST either adapt the proposal to fit the constitution or explicitly document the exception and its rationale.

**Version**: 1.0.0 | **Ratified**: 2026-07-05 | **Last Amended**: 2026-07-05
