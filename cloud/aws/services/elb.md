[Back to AWS](../README.md)

---

# Elastic Load Balancing (ELB)

Managed system for distributing traffic across EC2 instances.

* Spans all AZs in one region
* Supports health checks
* Integrates w/ Auto Scaling
* Integrates w/ Route 53
* Three types of LBs
    * Classic
    * Application - forwards to Target Groups - good for microservices
    * Network - improved latency and handles long-running connections
