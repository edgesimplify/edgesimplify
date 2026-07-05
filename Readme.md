# EdgeSimplify

> Building an open, production-grade CDN stack for ISPs — multi-datacenter edge caching, control plane, and routing. Built in public.

[![Website](https://img.shields.io/badge/website-edgesimplify.com-065A82)](https://edgesimplify.com)
[![Substack](https://img.shields.io/badge/blog-Substack-FF6719)](https://edgesimplify.substack.com)
[![Status](https://img.shields.io/badge/status-early%20development-E8B84B)](#roadmap)

---

## The problem

Mid-tier ISPs and regional hosting providers pay heavily for upstream transit and third-party CDNs — yet they often can't (or won't) route customer traffic through someone else's network, for reasons of cost, privacy, or regulation.

Building an in-house CDN is the obvious answer, but it takes years of specialized engineering. The knowledge lives inside a handful of hyperscalers and commercial CDN vendors, and the open-source pieces (caches, load balancers, DNS) are components — not a coherent, operable system.

## What EdgeSimplify is

An open, production-grade stack that lets an ISP stand up its **own multi-datacenter CDN on its own hardware** — in weeks, not years.

Planned building blocks:

- **Edge caching** across multiple points of presence
- **Central control plane** for configuration and cache management
- **GeoDNS / anycast routing** to steer users to the nearest PoP
- **Health checking and failover** between datacenters
- **Metrics and observability** for cache hit-ratio, traffic, and origin offload

## Why I'm building this

I architect and operate cloud & CDN infrastructure at a regional ISP. The **single-datacenter version of this stack already serves production traffic** — this project is the effort to generalize it into a multi-datacenter, self-hostable system that any mid-tier operator can run.

I'm building it **in public**, documenting the architecture and the decisions every week.

## Who it's for

- Tier 2–3 ISPs and regional operators
- Hosting and cloud providers who want in-house content delivery
- Enterprises that must keep traffic on their own infrastructure

## Roadmap

| Phase | Focus | Status |
|-------|-------|--------|
| 0 | Architecture & design docs | 🟡 In progress |
| 1 | Control plane + single-PoP reference deployment | ⚪ Planned |
| 2 | Multi-PoP routing (GeoDNS/anycast) + config sync | ⚪ Planned |
| 3 | Failover, observability, operational tooling | ⚪ Planned |

## Follow along

- 📨 **Weekly build log:** [edgesimplify.substack.com](https://edgesimplify.substack.com)
- 🌐 **Website:** [edgesimplify.com](https://edgesimplify.com)

## Consulting

I'm available for consulting on CDN architecture, multi-datacenter infrastructure, Kubernetes, and high-availability / disaster-recovery design. Reach out: **megamir.amir@gmail.com**

## License

Apache-2.0 — see [LICENSE](LICENSE).
