[Back to AWS](../README.md)

---

# Elastic Compute Cloud (EC2)

EC2 is perhaps the most fundamental service of AWS. It allows users to purchase virtual compute environments ("instances") on-demand, which is contrary to the data center model of purchasing the maximum compute capacity you expect to need up front.

EC2 gives you a price-fixed menu of combinations of CPU, RAM, storage, and I/O

## Instance purchasing options

* **On demand** - pay by the second
* **Dedicated host** - AWS provides physical hosts - the host never changes. Good for when your license requires a specific host
* **Dedicated Instances** - AWS guarantees that instance is running on a physical host w/ no other customers

## Amazon Machine Images (AMIs)

AMIs are preconfigured templates for running an EC2 instance. You can launch multiple instances of the same AMI, including across different instance types.

AMIs include:

* OS (Linux or Windows - license fees are included in the price of the instance)
* Runtime
* Application server
* Application

AMIs are provided by:

* AWS
* Trusted providers (MS, Debian, Red Hat, etc.)
* The community

## Hypervisors

Xen and Nitro are supported. Bare metal is also available

## Instance limit

There is a soft limit of 20 instances per account. Contact AWS Support to change this.

## EC2 best practices
* Treat VM instances as disposable
* Immutable Infrastructure - get everything right in the AMI first, don't rely on shell'ing into an instance to set it up
* Treat logs as streams - always ship them off the host into a log aggregation system
* Leverage roles - control which AWS services (S3, Dynamo, etc.) can be used from a given instance
* Automate deployments
* Monitor w/ CloudWatch
* Enable scaling and self-healing using Auto Scaling
