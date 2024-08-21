[Back to Tools](./README.md)

---

# Istio

Istio is an open-source, platform agnostic service mesh.

## Service Mesh

A Service Mesh is a software layer than manages communication between services within a service-oriented application architecture.

### Problems Solved by Service Mesh

* **Inter-service Communication** - services need to be able to communicate with each other.
* **Encrypted Communication** - without TLS, data in transit may be vulnerable to attackers.
* **Service Management** - as a platform scales up it can become costly to manage the configuration of services, load balancers, firewall rules, etc.
* **Principal of Least Privileged Access** - not all services need access to all others.

### Features of a Service Mesh

* **Service Discovery** - services don't need their dependencies hard-coded to run; instead they can query a Service Registry to obtain a list of existing dependent services.
* **Service Identity** - a service mesh distributes mTLS certificates to each service, allowing each to identify itself in service-to-service communication. This also ensures encryption of data in transit over the network.
* **Traffic Splitting** - conduct canary deployments of service releases easily using a service mesh control plane.
