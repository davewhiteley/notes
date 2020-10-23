[Back to AWS](../README.md)

---

# Elastic Block Store (EBS)

Block Storage

* Users can update small blocks of a file, rather than the entire file
* Uses a more efficient protocol that the HTTP used for object storage
* Can be mounted (unlike object storage)
* Useful for files that change often
* Data is independent of EC2 instances - fault tolerant
* Pricing is by provisioned size, even if it is not full or even used at all
* Can only be used within the same AZ
* Point-in-time snapshots can be created and saved in S3
* Can be detached and attached to different instances
* Can be encrypted (AES-256)
* Can be used in RAID or LVM
