<!--
Licensed to the Apache Software Foundation (ASF) under one
or more contributor license agreements.  See the NOTICE file
distributed with this work for additional information
regarding copyright ownership.  The ASF licenses this file
to you under the Apache License, Version 2.0 (the
"License"); you may not use this file except in compliance
with the License.  You may obtain a copy of the License at

  http://www.apache.org/licenses/LICENSE-2.0
-->

# GKE right-sizing analysis — Datadog utilization × GCP billing

Generated 2026-07-07. 7-day average node utilization per GKE cluster
(Datadog agent host metrics: CPU busy % = 100−idle; memory used % = 1−pct_usable)
crossed with 30-day GCP node cost attributed via the `goog-k8s-cluster-name`
billing label. **Binding utilization** = max(CPU, mem) — the resource that
prevents shrinking the node pool. Savings model: right-size the pool so binding
utilization reaches 60% → potential ≈ cost × (1 − binding/60%).

Caveats: node-level averages (peaks/burst headroom not modeled — verify p95 before
acting); autoscaled/spot pools already flex; clusters with no cost row lack the
billing label or spend <$100/30d. Datadog CCM is NOT enabled, so this is the
no-add-on approximation of workload cost allocation (issue #3).

| Cluster | 30d node cost | CPU % | Mem % | Binding % | Est. monthly savings |
|---|---:|---:|---:|---:|---:|
| video-cluster-1 | $X | 25% | 11% | 25% | $X |
| api-cluster-1 | $X | 15% | 21% | 21% | $X |
| video-cluster-2 | $X | 22% | 7% | 22% | $X |
| ads-cluster-1 | $X | 8% | 39% | 39% | $X |
| api-cluster-2 | $X | 22% | 24% | 24% | $X |
| api-cluster-3 | $X | 7% | 12% | 12% | $X |
| data-cluster-1 | $X | 23% | 36% | 36% | $X |
| api-cluster-4 | $X | 14% | 24% | 24% | $X |
| ml-cluster-1 | $X | 7% | 10% | 10% | $X |
| ads-cluster-2 | $X | 6% | 31% | 31% | $X |
| jobs-cluster-1 | $X | 5% | 8% | 8% | $X |
| ml-cluster-2 | $X | 3% | 22% | 22% | $X |
| data-cluster-2 | $X | 8% | 18% | 18% | $X |
| image-cluster-1 | $X | 8% | 6% | 8% | $X |
| ml-cluster-3 | $X | 5% | 14% | 14% | $X |
| jobs-cluster-2 | $X | 4% | 10% | 10% | $X |
| image-cluster-2 | $X | 5% | 5% | 5% | $X |
| analytics-cluster-1 | $X | 19% | 22% | 22% | $X |
| video-cluster-3 | $X | 3% | 6% | 6% | $X |
| ads-cluster-3 | $X | 7% | 42% | 42% | $X |
| analytics-cluster-2 | $X | 7% | 11% | 11% | $X |
| ads-cluster-4 | $X | 7% | 40% | 40% | $X |
| jobs-cluster-3 | $X | 1% | 5% | 5% | $X |
| video-cluster-4 | $X | 15% | 27% | 27% | $X |
| admin-cluster-1 | $X | 5% | 11% | 11% | $X |
| ml-cluster-4 | $X | 7% | 18% | 18% | $X |
| ml-cluster-5 | $X | 12% | 26% | 26% | $X |
| agents-cluster-1 | $X | 13% | 16% | 16% | $X |
| agents-cluster-2 | $X | 21% | 21% | 21% | $X |
| web-cluster-1 | $X | 39% | 31% | 39% | $X |
| web-cluster-2 | $X | 13% | 57% | 57% | $X |
| web-cluster-3 | $X | 14% | 62% | 62% | $X |
| web-cluster-4 | $X | 13% | 61% | 61% | $X |
| image-cluster-3 | $X | 2% | 94% | 94% | $X |
| **Total (34 matched clusters)** | **$X** | | | | **$X** |

## Top actions

- **video-cluster-1** — $X/30d at 25% binding (25% CPU / 11% mem): ~$X/mo potential.
- **api-cluster-1** — $X/30d at 21% binding (15% CPU / 21% mem): ~$X/mo potential.
- **video-cluster-2** — $X/30d at 22% binding (22% CPU / 7% mem): ~$X/mo potential.
- **ads-cluster-1** — $X/30d at 39% binding (8% CPU / 39% mem): ~$X/mo potential.
- **api-cluster-2** — $X/30d at 24% binding (22% CPU / 24% mem): ~$X/mo potential.
