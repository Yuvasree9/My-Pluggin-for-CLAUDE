AI ARCHITECT PLUGIN
STANDARDS VERSION: v1.0

---

## I. ARCHITECTURE STANDARDS

1. No single point of failure allowed.
2. All services must expose health and readiness endpoints.
3. All external APIs must be versioned.
4. All write APIs must support idempotency.
5. All systems must define RTO and RPO.
6. All data models must define index strategy.
7. All migrations must include rollback scripts.
8. No shared database across bounded contexts.
9. All async systems must define backpressure handling.
10. Caching strategy must define invalidation policy.

---

## II. DEPLOYMENT STANDARDS

1. Environments must be separated (dev/stage/prod).
2. Infrastructure must be defined as code.
3. Rollback process must be documented.
4. Canary or phased release must be defined.
5. Secrets must be stored in secure vault (e.g., Secrets Manager).
6. IAM must follow least privilege.

---

## III. RESILIENCE STANDARDS

1. DB outage mitigation must be defined.
2. Service crash recovery must be defined.
3. Deployment failure rollback must be defined.
4. Monitoring and alert thresholds must be defined.
5. Backup and restore procedure must be documented.

---

## IV. SECURITY STANDARDS

1. All traffic must use TLS.
2. Data at rest must be encrypted.
3. PII classification must be defined.
4. Input validation required for all endpoints.
5. Authentication and authorization model required.

---

## V. COST GOVERNANCE

1. Scaling model must include cost implication.
2. Storage growth projection must be estimated.
3. High-traffic components must define optimization levers.

---

## VI. EVALUATION & AI SYSTEMS

1. All AI systems must define evaluation metrics.
2. Offline and online evaluation must be separated.
3. Drift monitoring must be defined.
4. Model rollback strategy required.

---

ENFORCEMENT

Non-compliance results in:

- Spec rejection
- Architecture review failure
- Governance flag

All specs must reference:
Standards Version: v1.0
