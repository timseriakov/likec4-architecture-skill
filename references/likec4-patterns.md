# LikeC4 Architecture Patterns

Use these as starting templates when user intent is architectural but specifics are incomplete.

## 1. Monolith + Database

Use when system is single deployable unit.

- `system Product`
- `container App`
- `container Database`
- Relationships: `User -> App`, `App -> Database`

## 2. Modular Monolith

Use when one deployment with clear internal modules.

- `container App`
- nested components (`Billing`, `Orders`, `Auth`)
- explicit internal relationships between components

## 3. Microservices + Queue

Use when async boundaries and independent services are present.

- containers: `Gateway/API`, `Service A`, `Service B`, `Queue`, `DB`
- relationships: `Gateway -> Service A`, `Service A -> Queue`, `Service B -> Queue`, `Service B -> DB`

## 4. Event-Driven Data Pipeline

Use when data flows across producers/consumers.

- producer services
- stream/queue
- consumers/processors
- storage/warehouse

Relationship labels should show intent (`Publishes`, `Consumes`, `Transforms`, `Stores`).

## 5. External Integrations

Use when third-party APIs dominate architecture.

- internal system boundary
- external services as separate elements
- label trust boundaries and data directions

## View strategy

Minimum recommended:

- Context view: users + external systems + product boundary
- Container view: deployable/runtime units and their main flows

Add component views only for:

- critical use-cases,
- high-change areas,
- migration boundaries.
