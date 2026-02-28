---
description: Engineering rules and architectural patterns for generating production-grade system designs. Use this skill when designing systems, evaluating architectures, or generating system design documents with /design-system.
---

# Engineering Rules

1. All write APIs must support idempotency.
2. Every service must define health/readiness endpoints.
3. All systems must define RTO and RPO.
4. Deployment plans must include rollback.
5. Avoid single points of failure.
6. All APIs must be versioned.
7. Data migrations must include rollback scripts.
8. Logging and tracing must be mandatory.

# System Design Template

## Assumptions

- [Assumption 1]
- [Assumption 2]

## Architecture Overview

- **Pattern**: [Chosen Architecture Pattern]
- **Justification**: [Reasoning for pattern choice]

## Component Responsibilities

- **[Component Name]**: [Primary Responsibility]
- **[Component Name]**: [Primary Responsibility]

## Data Model

- **Database Type**: [SQL/NoSQL/etc.]
- **Entities**: [List of core entities]

## API Contracts

- **[Method] [Endpoint]**: [Purpose] -> [Expected Output]

## Scaling Strategy

- **Target Metrics**: [Target Throughput/Latency]
- **Approach**: [Scaling Mechanism]

## Failure Modes

- **Failure Scenario**: [Description]
- **Mitigation/Fallback**: [Strategy]

## Deployment Plan

- **Strategy**: [Blue-Green/Canary/etc.]
- **Rollback Mechanism**: [Description]

## Testing Strategy

- **Test Type**: [Integration/E2E/Load/etc.]
- **Scope**: [Coverage Focus]

## Risk Register

- **Risk**: [Description]
- **Impact**: [High/Medium/Low]
- **Mitigation**: [Strategy]
