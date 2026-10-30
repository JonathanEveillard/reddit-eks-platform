# Metrics

Before = original guide setup. After = my changes.

| Metric | Before (guide) | After | How measured |
|---|---|---|---|
| HIGH/CRITICAL CVEs, Argo CD image | v2.4.7: 154 (16 critical) | v3.5.5: 49 (1 critical) | Trivy 0.76.1, unique CVE IDs, scanned 2026-10-29 |
| Commit to running in cluster | | | Pipeline start to Argo "Healthy" timestamp |
| Env rebuild time (empty to app live) | | | `time make up` |
| Teardown completeness | | | Resources left after destroy |
| Long lived AWS keys in use | | 0 | IAM credential report |
| Publicly exposed services | | | LoadBalancer count |
| p95 latency @ N VUs | | | k6 |
| Max VUs with p95 < SLO | | | k6 ramp test |
| Cost per hour running | | | Cost Explorer, Project tag |