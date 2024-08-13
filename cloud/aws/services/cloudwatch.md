[Back to AWS](../README.md)

---

# CloudWatch

Monitoring / metrics collection system / instrumentation
* Stores metrics data for 2 weeks
* Accessible via API so you can pull and store data long term if desired
* Each service provides unique data points
* User can write custom metrics reports and have the data dumped into CloudWatch

## CloudWatch Alarms
* Triggered by the breach of a defined metric threshold
* Can trigger auto-scaling, termination, reboot
* Up to 5,000 alarms per account (soft limit)
* Can send notification to SNS (email, txt, PagerDuty, etc.)

## CloudWatch Logs
* Collect logs by streaming (near-real-time)
* Configure agents on EC2 instances
* Collect Route 53 DNS queries

### Questions to answer
* Are we over provisioned? Under provisioned?
* What exactly is the current demand?
* Where are the architectural bottlenecks?
* How is the app performing? LB? EC2 instance?
* Are there idle instances?
