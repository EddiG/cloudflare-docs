---
_build:
  publishResources: false
  render: never
  list: never
---

For customers using the legacy health check system with a public IP range, Cloudflare recommends that:

1. You configure the IP address for your tunnel health check target to be one from within the prefix range `172.64.240.252/30`.
2. Apply a policy-based route that matches packets with source IP address equal to the configured tunnel health check target (for example  `172.64.240.253/32`), and route them over the tunnel back to Cloudflare.