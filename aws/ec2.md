# Elastic Compute Cloud (EC2)

* Purchase access to instances of VMs
* Linux or Windows
* Xen or Nitro hypervisor
* Bare metal is available
* EC2 gives you a price-fixed menu of combinations of CPU, RAM, storage, and I/O
* Soft limit on instances - 20/account
* Fees include OS license
* Dedicated Instances - AWS guarantees that instance is running on a physical host w/ no other customers
* Dedicated Hosts - AWS provides physical hosts - the host never changes. Good for when your license requires a specific host
* AMI - Amazon Machine Image
    * Bit-for-bit copy of the root volume
    * Choice of OS
    * Provided by
        * AWS
        * Trusted providers (MS, Debian, Red Hat, etc.)
        * The community
* EC2 best practices
    * Treat VM instances as disposable
    * Immutable Infrastructure - get everything right in the AMI first, don't rely on shell'ing into an instance to set it up
    * Treat logs as streams - always ship them off the host into a log aggregation system
    * Leverage roles - control which AWS services (S3, Dynamo, etc.) can be used from a given instance
    * Automate deployments
    * Monitor w/ CloudWatch
    * Enable scaling and self-healing using Auto Scaling
