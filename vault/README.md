[Back to home](../README.md)

---

# HashiCorp Vault

Vault is a secrets management tool developed by HashiCorp.

## Fundamental Concepts of Secrets Management

### What is a Secret?

A "secret" in this context is any piece of data which may grant authentication or authorization, including username-password pairs, database credentials, API tokens, TLS certificates, etc.

### Challenges of Secrets Management

* Tracking who has access to them
* Tracking who actually uses them
* Rotating secrets periodically

### Secret Sprawl

Without a mature secrets management system in place, secrets tend to sprawl out across corporate infrastructure. They may be stored in plain text in Source Code Management (SCM) systems like git; they may be found in running Development applications and later reused in Production; they may be stored in Configuration Management systems like Ansible. Each of these systems could have large numbers of users with Read access who are able to access these secrets, however they may have no audit trail of users who actually _did_ access those secrets.

In addition to the problem of secrets disclosure through sprawl, this state also makes it difficult to rotate secrets. If a secret is hard coded in source code `n` number of times, it is significantly more complex to rotate than if it only existed in one place.

## How Vault Works

### Encryption

Vault is responsible for the encryption of secrets at rest inside its database, and in transit between Vault and its clients. Encryption can be configured, but is otherwise simple to implement.

### Access Control

Vault implements fine-grained access control. Vault Admins can be highly specific about which users/services may have access to which secrets.

### Audit Trail

Vault keeps track of which users/services accessed which secret, and when.

## Major Concepts of Vault

### Centralization of Secrets

Vault serves as a centralized repository of secrets - this enables easy rotation of secrets because there are no other copies to locate. Secrets can be removed from vulnerable systems (SCM, Config Mgmt, etc.) preventing their ongoing disclosure.

### Dynamic Secrets

Centralization of Secrets addresses the issue of secrets disclosure _before_ they are consumed. After a secret leaves Vault and is delivered to the requesting service, it can be vulnerable in other ways. Applications may log usernames/passwords to standard out which then gets shipped off to a log aggregation system (where many users have read access); the application may disclose credentials in error messages, tracebacks, and other diagnostic data; and it may disclose credentials to external application monitoring systems.

Dynamic Secrets are intended to replace static secrets. In this model Vault will programatically issue unique secrets to in-scope services. These dynamic secrets are ephemeral, with a configurable Time to Live (TTL). When a secret expires Vault can automatically issue a replacement.

This model has a few advantages: it makes a moving target of system credentials; it makes it easy to avoid sharing the same (static) secrets among multiple similar services; and by not sharing credentials, you can limit the blast radius of an attack/compromise by only revoking the affected credentials.

### Encryption as a Service

Cryptography is highly specialized discipline of software development, and when done improperly can lead to sensitive data disclosure. Because not all developers have the time to study cryptography, it is often not properly implemented in practice.

Vault provides a high-level API that can handle many cryptographic tasks for the application developer. Instead of requesting an encryption key and then having to correctly implement cryptography within the application, developers can simply request Vault handle these tasks in addition to managing encryption keys.

