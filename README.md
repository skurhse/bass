# 🐟 bass

`bass` is a collection of [hypertext](https://en.wikipedia.org/wiki/Hypertext) [DevOps](https://en.wikipedia.org/wiki/DevOps) flashcards, organized around six engineering concepts:

- [Cloud computing](https://en.wikipedia.org/wiki/Cloud_computing): a [geo-redundant](https://en.wikipedia.org/wiki/Redundancy_(engineering)#Geographic_redundancy), [pay-as-you-go](https://en.wikipedia.org/wiki/Cloud_computing#Value_proposition) model for storage and compute services.
- [Computer networks](https://en.wikipedia.org/wiki/Computer_network): resource-sharing using digital [interconnections](https://en.wikipedia.org/wiki/Interconnection) with common [communication protocols](https://en.wikipedia.org/wiki/Communication_protocol).
- [Computer security](https://en.wikipedia.org/wiki/Computer_security): protection of systems from [threats](https://en.wikipedia.org/wiki/Threat_(computer_security)) enabled by [vulnerabilities](https://en.wikipedia.org/wiki/Vulnerability_(computer_security)).
- [Linux](https://en.wikipedia.org/wiki/Linux): a family of [Unix-like](https://en.wikipedia.org/wiki/Unix-like) operating systems based on the [Linux kernel](https://en.wikipedia.org/wiki/Linux_kernel).
- [Virtualization](https://en.wikipedia.org/wiki/Virtualization): technologies that subdivide physical resources into [virtual machines](https://en.wikipedia.org/wiki/Virtual_machine) and [operating systems](https://en.wikipedia.org/wiki/Operating_system).
- [Web Development](https://en.wikipedia.org/wiki/Web_development): the work involved in developing a [website](https://en.wikipedia.org/wiki/Website) for the [Internet](https://en.wikipedia.org/wiki/Internet).

### Usage
- Navigate `bass` using the [Table of Contents](#table-of-contents) or the GitHub [outline button](https://github.blog/changelog/2021-04-13-table-of-contents-support-in-markdown-files/) on the upper right (☰).
- Card categories are listed in alphabetical order; cards within categories are curated into narrative order.
- [Open source](https://en.wikipedia.org/wiki/Open_source), [Wikipedia](https://en.wikipedia.org/wiki/Wikipedia), and [IETF](https://www.ietf.org/about/introduction/#about) [RFC](https://www.ietf.org/process/rfcs/) hyperlinks are prioritized over proprietary resources, except in cases of original source material.

## Table of Contents

- [Cloud Computing](#cloud-computing)
  - [Amazon Web Services](#amazon-web-services)
  - [Infrastructure-as-code](#infrastructure-as-code)
  - [Google Cloud Platform](#google-cloud-platform)
  - [Kubernetes](#kubernetes)
  - [Microsoft Azure](#microsoft-azure)
- [Computer Networks](#computer-networks)
  - [Internet Protocol Suite](#internet-protocol-suite)
  - [Network Security](#network-security)
- [Computer Security](#computer-security)
  - [Information Security](#information-security)
  - [OAuth](#oauth)
- [Linux](#linux)
  - [Distributions](#distributions)
  - [Utilities](#utilities) 
- [Virtualization](#virtualization)
  - [OS-level virtualization](#os-level-virtualization)
- [Web Development](#web-development)
  - [Application Programming Interfaces](#application-programming-interfaces)
  - [Application Security](#application-security)

## Cloud Computing

### Amazon Web Services

### What is [Amazon Web Services](https://en.wikipedia.org/wiki/Amazon_Web_Services)?

*Amazon Web Services, Inc.* or 'AWS' is a subsidiary of Amazon that provides cloud computing platforms and APIs.

AWS comprises over 200 individual products and services.

### What is [Amazon Elastic Compute Cloud](https://en.wikipedia.org/wiki/Amazon_Elastic_Compute_Cloud)?

The *Elastic Compute Cloud* or 'EC2' is AWS's autoscaling machine virtualization platform.

In EC2, virtual machine instances are configurable using virtual appliances called "Amazon Machine Images" that includes:

- root volume template
- launch permissions
- block device mappings

### What is [Amazon S3](https://en.wikipedia.org/wiki/Amazon_S3)?

Amazon Simple Storage Service or 'S3' is an AWS service that provides object storage through a web service interface.

S3 objects are organized into buckets, wherein each object is identified by a unique, user-assigned key.

### Infrastructure-as-code

#### 1. What is [infrastructure-as-code](https://en.wikipedia.org/wiki/Infrastructure_as_code)?

Infrastructure-as-code or 'IaC' is the process of managing and provisioning data-center resources through machine-readable definition files.

The code may use either scripts or declarative definitions, but IaC more often employs declarative approaches.

#### 2. What is [Immutable infrastructure](https://www.hashicorp.com/resources/what-is-mutable-vs-immutable-infrastructure)?

"Immutable infrastructure" is an IaC paradigm wherein machine state is not upgraded or migrated in-place.

Instead, snapshot images are created and deployed to a virtualization platform and rerouted with a network switchover.

#### 3. What is [Terraform](https://github.com/hashicorp/terraform)?

Terraform by HashiCorp is a [source-available](https://en.wikipedia.org/wiki/Business_Source_License) IaC software used to deliver infrastructure with  the declarative configuration languages [HCL](https://github.com/hashicorp/hcl) or JSON.

Terraform manages external resources with programs called providers.

#### 4. What is [Continuous configuration automation](https://en.wikipedia.org/wiki/Continuous_configuration_automation)?

Continuous configuration automation or 'CCA' is the process of automating the deployment, configuration and orchestration of software.

'CCA' is an extension of infrastructure-as-code framework methodology.

#### 5. What is [Ansible](https://github.com/ansible/ansible)?

Ansible by Red Hat is an open-source IaC software that manages fleets through configurable host inventories.

Ansible requires network connectivity and for Python to be installed on machine targets.

### Kubernetes

#### 1. What is [Kubernetes](https://kubernetes.io/docs/concepts/overview/)?

*Kubernetes* is an open-source container orchestration platform that automates the deployment and management of workloads and services.

#### 2. List the [Kubernetes feature set](https://kubernetes.io/docs/concepts/overview/#why-you-need-kubernetes-and-what-can-it-do).

- Service discovery and load balancing
- Storage orchestration
- Automated rollouts and rollbacks
- Automatic bin packing
- Self-healing
- Secret and configuration management
- Batch execution
- Horizontal scaling
- IPv4/IPv6 dual-stack
- Designed for extensibility

#### 3. List k8s [control plane components](https://kubernetes.io/docs/concepts/overview/components/#control-plane-components)

- [kube-apiserver](https://kubernetes.io/docs/concepts/overview/components/#kube-apiserver) - the front end that exposes the k8s api.
- [etcd](https://kubernetes.io/docs/concepts/overview/components/#etcd) - the backing store for all cluster data.
- [kube-scheduler](https://kubernetes.io/docs/concepts/overview/components/#kube-scheduler) -  selects nodes for pods to run on.
- [kube-controller-manager](https://kubernetes.io/docs/concepts/overview/components/#kube-controller-manager) - runs controller processes.
- [cloud-controller-manager](https://kubernetes.io/docs/concepts/overview/components/#cloud-controller-manager) - runs controllers that are specific to cloud providers.

#### 4. List some k8s [controllers](https://kubernetes.io/docs/concepts/architecture/controller/).

- [Node controller](https://kubernetes.io/docs/concepts/architecture/nodes/#node-controller)
  - Assigns CIDR block to nodes on registration.
  - Checks cloud provider API for node availability.
- [Job controller](https://kubernetes.io/docs/concepts/architecture/controller/#control-via-api-server)
  - Tells the API server to create or remove Job Pods.
  - Updates Job objects to 'Finished'.
- [EndpointSlice controller](https://kubernetes.io/docs/concepts/services-networking/endpoint-slices/#management)
  - Populates endpoint slices to link services and pods.
- [ServiceAccount controller](https://kubernetes.io/docs/reference/access-authn-authz/service-accounts-admin/#serviceaccount-controller)
  - Manages the ServiceAccounts inside namespaces.
  - Ensures a ServiceAccount named "default" exists in every active namespace.

#### 5. List k8s [node components](https://kubernetes.io/docs/concepts/overview/components/#node-components).

- [kubelet](https://kubernetes.io/docs/concepts/overview/components/#kubelet) - manages pod specifications and health.
- [kube-proxy](https://kubernetes.io/docs/concepts/overview/components/#kube-proxy) - maintains network rules on nodes.
- [container runtime](https://kubernetes.io/docs/concepts/overview/components/#container-runtime) - manages the execution and lifecycle of containers.

#### 6. What are k8s [objects](https://kubernetes.io/docs/concepts/overview/working-with-objects/#kubernetes-objects)?
  
Kubernetes objects are persistent entities in the Kubernetes system, used to represent the state of the server.

Objects describe:
- What containerized applications are running, and on which nodes.
- The resources available to those applications.
- The policies around how those applications behave.

#### 7. What is a [pod](https://kubernetes.io/docs/concepts/workloads/pods/)?

A Pod is a group of one or more containers, with shared storage and network resources, and a specification for how to run the containers.

Pod can contain init containers that run during Pod startup. You can also inject ephemeral containers for debugging a running Pod.

#### 8. What is a [workload](https://kubernetes.io/docs/concepts/workloads/)?

A workload is an application running on Kubernetes, where workload resources are abstractions that manage a set of pods. 

Workload resources configure controllers to ensure that pods match the state you specified.

#### 9. List built-in workload resources.

- [ReplicaSet](https://kubernetes.io/docs/concepts/workloads/controllers/replicaset/) - maintains a stable set of replica Pods.
- [StatefulSet](https://kubernetes.io/docs/concepts/workloads/controllers/statefulset/) - runs a group of Pods and maintains a sticky identity for each. 
- [DaemonSet](https://kubernetes.io/docs/concepts/workloads/controllers/daemonset/) - defines pods that provide node-local facilities.
- [Deployment](https://kubernetes.io/docs/concepts/workloads/controllers/deployment/) - provides declarative updates for Pods and ReplicaSets.
- [Job](https://kubernetes.io/docs/concepts/workloads/controllers/job/) - runs pods to completion and then stops.
- [CronJob](https://kubernetes.io/docs/concepts/workloads/controllers/cron-jobs/) - creates jobs on a repeating schedule.

#### 10. What is the [k8s network model](https://kubernetes.io/docs/concepts/services-networking/#the-kubernetes-network-model)?

In the k8s network model, every Pod in a cluster gets its own unique cluster-wide IP address and Pods can be treated much like VMs or physical hosts from the perspectives of port allocation, naming, service discovery, load balancing, application configuration, and migration.

Kubernetes networking addresses the following concerns:

- Containers within a Pod use networking to communicate via loopback.
- Cluster networking provides communication between different Pods.
- The Service API lets you expose an application running in Pods to be reachable from inside or outside your cluster.

#### 11. List built-in network resources.

- [Service](https://kubernetes.io/docs/concepts/services-networking/service/)
  - Exposes an application behind a single outward-facing endpoint.
- [Ingress](https://kubernetes.io/docs/concepts/services-networking/ingress/)
  - Manages external access to the services in a cluster, typically HTTP.
  - May provide load balancing, SSL termination and name-based virtual hosting.
- [Ingress Controllers](https://kubernetes.io/docs/concepts/services-networking/ingress-controllers/)
  - Provides the software implementation for ingress resources (AWS, GCE, nginx, etc.)
- [Gateway API](https://kubernetes.io/docs/concepts/services-networking/gateway/)
  - A family of API kinds that provide dynamic infrastructure provisioning and advanced traffic routing.
- [Endpoint Slices](https://kubernetes.io/docs/concepts/services-networking/endpoint-slices/)
  - Provides a way to track network endpoints within a Kubernetes cluster.
  - The control plane automatically creates EndpointSlices for any service that has a selector specified.
- [Network Policies](https://kubernetes.io/docs/concepts/services-networking/network-policies/)
  - Allows one to specify rules for traffic flow within a cluster, between pods and the outside world.
  - The cluster must use a network plugin that supports NetworkPolicy enforcement.

#### 12. Lists k8s [configuration](https://kubernetes.io/docs/concepts/configuration/overview/) resources.

- [ConfigMaps](https://kubernetes.io/docs/concepts/configuration/configmap/)
  - Used to store non-confidential data in key-value pairs.
  - Pods can consume ConfigMaps as environment variables, command-line arguments, or as configuration files in a volume. 
- [Secrets](https://kubernetes.io/docs/concepts/configuration/secret/)
  - Used to store sensitive data such as passwords, tokens, or keys.
  - Secrets are similar to ConfigMaps but are specifically intended to hold confidential data.
- [Liveness Probe](https://kubernetes.io/docs/concepts/configuration/liveness-readiness-startup-probes/#liveness-probe)
  - Used to determine when to restart a container.
    Liveness probes can be used to catch deadlocks; when an application is running, but unable to make progress.
- [Readiness Probe](https://kubernetes.io/docs/concepts/configuration/liveness-readiness-startup-probes/#readiness-probe)
  - Used to determine when a container is ready to start accepting traffic.
  - Useful for applications with setup tasks, such as establishing network connections, loading files, and warming caches.
- [Startup Probe](https://kubernetes.io/docs/concepts/configuration/liveness-readiness-startup-probes/#startup-probe)
  - Verifies whether the application within a container is started. 
  - When a startup probe is configured, it disables liveness and readiness checks until it succeeds.
  - Startup probe are only executed at startup.
- [Requests and Limits](https://kubernetes.io/docs/concepts/configuration/manage-resources-containers/#requests-and-limits)
  - An optional specification to define how much of each resource a container needs.
  - Requests are used by the kube-scheduler to decide which node to place a pod on.
  - Requests and limits are used by the kubelet to enforce and reserve resource usage for running containers.

#### 13. What is Kubernetes [scheduling, preemption and eviction](https://kubernetes.io/docs/concepts/scheduling-eviction/)?

- 'Scheduling' refers to making sure that Pods are matched to Nodes so that the kubelet can run them.
- 'Preemption' is the process of terminating Pods with lower Priority so that Pods with higher Priority can schedule on Nodes.
- 'Eviction' is the process of proactively terminating one or more Pods on resource-starved Nodes.

#### 14. What are [node affinity, taints and tolerations](https://kubernetes.io/docs/concepts/scheduling-eviction/taint-and-toleration/)?

- [Node affinity](https://kubernetes.io/docs/concepts/scheduling-eviction/assign-pod-node/#affinity-and-anti-affinity)
  - a property of Pods that attracts them to a set of nodes
- [Taints and Tolerations](https://kubernetes.io/docs/concepts/scheduling-eviction/taint-and-toleration/)
  - Taints are labels used to allow a node to repel a set of pods.
  - Tolerations allow the scheduler to schedule pods with matching taints.
  - Taints and tolerations work together to ensure that pods are not scheduled onto inappropriate nodes

#### 15. List k8s [security mechanisms](https://kubernetes.io/docs/concepts/security/#security-mechanisms).

- [control plane protection](https://kubernetes.io/docs/concepts/security/#control-plane-protection) - control access to the Kubernetes API.
  - [transport security](https://kubernetes.io/docs/concepts/security/controlling-access/#transport-security) - protected with TLS.
  - [authentication](https://kubernetes.io/docs/concepts/security/controlling-access/#authentication) - run one or more authenticator modules.
  - [authorization](https://kubernetes.io/docs/concepts/security/controlling-access/#authorization) - policy-based action control.
- [secrets](https://kubernetes.io/docs/concepts/security/#secrets) - confidentiality protection for configuration values 
- [workload protection](https://kubernetes.io/docs/concepts/security/#workload-protection) - enforce network policies and pod security standards.
- [auditing](https://kubernetes.io/docs/concepts/security/#auditing) - security logging for users and applications.

### Microsoft Azure

#### 1. What is [Microsoft Azure](https://en.wikipedia.org/wiki/Microsoft_Azure)?

Microsoft Azure is the cloud computing platform developed by Microsoft Corporation.

Azure has over 600 services supporting both Microsoft-specific and third-party software systems.

### 2. What is [Azure Cosmos DB](https://en.wikipedia.org/wiki/Cosmos_DB)?

Azure Cosmos DB or 'Cosmos DB' is a globally distributed, multi-model database service designed for low-latency and high availability.

Cosmos offers fiveve different partial compatibility APIs, exposing protocol endpoints for MongoDB, Gremlin, Cassandra, Azure Table Storage, and etcd.

## Computer Networks

### Internet Protocol Suite

#### 1. What is the [Internet Protocol Suite](https://en.wikipedia.org/wiki/Internet_protocol_suite)?

The Internet Protocol Suite or 'TCP/IP' is a framework for organizing the set of communication protocols used in the Internet according to functional criteria.

The foundational protocols in the suite are the Transmission Control Protocol (TCP), the User Datagram Protocol (UDP), and the Internet Protocol (IP).

The suite is organized into four abstraction layers:
- [Link layer](https://en.wikipedia.org/wiki/Link_layer): protocols confined to the link to which a host is physically connected.
- [Internet layer](https://en.wikipedia.org/wiki/Internet_layer): internetworking protocols that connect networks through gateways.
- [Transport layer](https://en.wikipedia.org/wiki/Transport_layer): end-to-end communication services for applications.
- [Application layer](https://en.wikipedia.org/wiki/Application_layer): protocols used by hosts' process-to-process communications.

#### 1. What is the [Internet Protocol](https://datatracker.ietf.org/doc/html/rfc791)?

The Internet Protocol or 'IP' is a protocol designed for use in interconnected systems of packet-switched computer communication networks.

IP is responsible for addressing host interfaces, encapsulating data into datagrams and routing datagrams from a source to a destination.

#### 2. What is [IPv6](https://datatracker.ietf.org/doc/html/rfc8200)?

IP version 6 is the successor to IP version 4.

IPv6 implements the following change sets:

- Expanded Addressing Capabilities
- Header Format Simplification
- Improved Support for Extensions and Options
- Flow Labeling Capability
- Authentication and Privacy Capabilities

### 3. What is [subnetting](https://en.wikipedia.org/wiki/Subnet#Subnetting)?

Subnetting is the process of subdividing an IP network by designating some high-order bits from the host part as part of the network prefix and adjusting the subnet mask appropriately.

The following example shows the separation of the network prefix and the host identifier from an address (192.0.2.130) and its associated /24 subnet mask (255.255.255.0). The operation is visualized in a table using binary address formats.

Binary form	Dot-decimal notation
```
IP address	11000000.00000000.00000010.10000010	192.0.2.130
Subnet mask	11111111.11111111.11111111.00000000	255.255.255.0
Network prefix	11000000.00000000.00000010.00000000	192.0.2.0
Host identifier	00000000.00000000.00000000.10000010	0.0.0.130
```

The result of the bitwise AND operation of IP address and the subnet mask is the network prefix 192.0.2.0. The host part, which is 130, is derived by the bitwise AND operation of the address and the ones' complement of the subnet mask.

#### 4. What is [Transmission Control Protocol](https://en.wikipedia.org/wiki/Transmission_Control_Protocol)?

The Transmission Control Protocol or 'TCP' is one of the Internet protocol suite's main transport-layer protocols that originated with the original network implementation.

TCP provides reliable, ordered, and error-checked delivery of a stream of octets (bytes) between applications running on hosts communicating via an IP network.

TCP is connection-oriented, wherein the sender and receiver firstly establish a connection through a three-way handshake procedure.

#### 4. Describe the [TCP handshake](https://datatracker.ietf.org/doc/rfc793/).

For a connection to be established or initialized, the two TCPs must synchronize on each other's initial sequence numbers.  This is done in an exchange of connection establishing segments carrying a control bit called "SYN" (for synchronize) and the initial sequence numbers.

The synchronization requires each side to send it's own initial sequence number and to receive a confirmation of it in acknowledgment from the other side.  Each side must also receive the other side's initial sequence number and send a confirming acknowledgment.

```
    1) A --> B  SYN my sequence number is X
    2) A <-- B  ACK your sequence number is X
    3) A <-- B  SYN my sequence number is Y
    4) A --> B  ACK your sequence number is Y
```

#### 4. What is UDP?

Lorum ipsum.

#### 5. What is ICMP?

Lorum ipsum.

#### 6. What is traceroute?

Lorum ipsum.

#### 7. What is [DNS](https://datatracker.ietf.org/doc/html/rfc1034)?

The Domain Name System or 'DNS' is a hierarchical and distributed name service that provides a naming system for resources on Internet Protocol networks.

DNS delegates the responsibility of assigning domain names to Internet resources by designating authoritative name servers.

#### 8. What is [WHOIS](https://datatracker.ietf.org/doc/html/rfc3912)?

WHOIS, pronounced "who is", is a TCP-based transaction-oriented query/response protocol used to provide information services to Internet users.

WHOIS was originally used to provide information about registered domain names, current deployments cover a much broader range of information services.

The WHOIS protocol has not been internationalised and has no provisions for strong security.

#### 9. What is a [subnetting](https://en.wikipedia.org/wiki/Subnet)?

A subnetwork, or subnet, is a logical subdivision of an IP network.

Computers that belong to the same subnet are addressed with an identical group of its most-significant bits of their IP addresses.

### Network Security

#### 1. What is [TLS 1.3](https://datatracker.ietf.org/doc/rfc8446/)?

Transport Layer Security (TLS) is a cryptographic protocol that allows client/server applications to communicate over the Internet in a way that is designed to prevent eavesdropping, tampering, and message forgery.

Once the client and server have agreed to use TLS, they negotiate a stateful connection by using a handshaking procedure. The protocols use a handshake with an asymmetric cipher to establish cipher settings and a session-specific shared key with which further communication is encrypted using a symmetric cipher.

#### 2. What is [Public-key infrastructure](https://en.wikipedia.org/wiki/Public_key_infrastructure)?

PKI or 'Public-key infrastructure' is a set of roles, policies and procedures needed to manage public key certificates: electronic documents used to prove the validity of a public key.

#### 3. What is a Certificate Authority?

A CA or 'Certificate authority' is a root certificate issuer, usually a company that charges customers a fee to issue certificates for them.

A CA acts as a trusted third party—trusted both by the subject (owner) of the certificate and by the party relying upon the certificate.

#### 4. What is [X.509](https://www.itu.int/rec/T-REC-X.509)? 

X.509 is an International Telecommunication Union (ITU) framework for public-key certificates.

X.509 includes the specification of data objects, revocation notices and critical components of a public-key infrastructure.

## Linux

### linux Distributions

#### 1. What is [Linux](https://en.wikipedia.org/wiki/Linux)?

Linux is a family of open-source Unix-like operating systems based on the Linux kernel.

#### 2. List commercial enterprise distributions of Linux.

- [Amazon Linux 2](https://aws.amazon.com/amazon-linux-2)
- [Red Hat Enterprise Linux](https://www.redhat.com/en/technologies/linux-platforms/enterprise-linux)
- [SUSE Linux Enterprise](https://www.suse.com/products/server)

#### 3. List non-commercial enterprise distributions of Linux.
- [Alpine Linux](https://www.alpinelinux.org)
- [Debian](https://www.debian.org)
- [Rocky Linux](https://rockylinux.org/)
- [Ubuntu](https://ubuntu.com/)

#### 4. What is [POSIX.1-2017](https://pubs.opengroup.org/onlinepubs/9699919799/)?
The *Portable Operating System Interface* specifications are a standard created by the [IEEE Computer Society](https://www.computer.org/about) for maintaining compatibility between operating systems.

POSIX.1-2017 defines a standard operating system interface and environment, including a command interpreter (or “shell”), and common utility programs to support applications portability at the source code level.

#### 5. What is [LDAP](https://datatracker.ietf.org/doc/html/rfc4511)?

The Lightweight Directory Access Protocol or 'LDAP' is an directory services protocol for use over an Internet Protocol network.

Under LDAP, a directory user accesses the Directory through a Directory User Agent (DUA). The agent interacts with one or more Directory System Agents (DSA).

When an LDAP session is created, the authentication state of the session is set to anonymous. The BIND operation establishes the authentication state for a session.

#### 6. What is [gcc](https://gcc.gnu.org/)?

 The GNU Compiler Collection or 'GCC' is a collection of compilers from the GNU Project.

GCC includes front ends for C, C++, Objective-C, Fortran, Ada, Go, D and Modula-2 as well as libraries for these languages like `libstdc++`.

#### 7. What is [top](https://en.wikipedia.org/wiki/Top_(software))?

`top` is process monitor program that displays sorted information about CPU and memory utilization.

The Linux version of `top` is part of the `procps-ng` tools group.

#### 8. What is [lsof](https://en.wikipedia.org/wiki/Lsof)?

lsof is a command meaning "list open files", which reports a list of all open files and the processes that opened them.

Open files in the system include disk files, named pipes, network sockets and devices.

#### 9. What is [sysstat](https://en.wikipedia.org/wiki/Sysstat)?

`sysstat` or "system statistics" is a collection of Linux tools used to monitor system performance and usage activity.

The systat program `sar` is used to report on various system loads, including CPU activity, memory/paging, interrupts, device load, network and swap space utilization.

`sadc` is the system activity data collector and backend.

#### 10. What is [Bash](https://www.gnu.org/software/bash/)?

Bash or 'Bourne Again SHell' is the is the GNU Project's shell: a computer program that exposes OS services to users and programs.

Bash conforms to the IEEE POSIX P1003.2/ISO 9945.2 Shell and Tools standard and is `sh`-compatible.

#### 11. What is [systemd](https://systemd.io/)?

`systemd` is a system and service manager that runs as PID 1 and starts the rest of the system.

`systemd` supports SysV and LSB init scripts and works as a replacement for sysvinit.

Other parts include a logging daemon, and utilities to control basic system configuration.

#### 12. What is the [Linux Standard Base](https://wiki.linuxfoundation.org/lsb/about)?

The Linux Standard Base or 'LSB' is standard created by the Linux Foundation that describes the minimum set of APIs a Linux distribution must support.

The LSB working group also provides tools to test support.

### Utilities

Lorum Ipsum.

### Application Security

#### 5. What is [JSON Web Token](https://datatracker.ietf.org/doc/html/rfc7519)?

JSON Web Token or 'JWT' is a compact and URL-safe standard for representing claims to be transferred between two parties.

The claims in a JWT are encoded as a either:
- as a JSON object that is used as the payload of a JSON Web Signature
- as the plaintext of a JSON Web Encryption (JWE) structure

#### 6. What is an [injection exploit](https://en.wikipedia.org/wiki/Category:Injection_exploits)?

Injection exploits use data to subvert the intended operation of the system. Injection exploits leverage vulnerabilities resulting from insufficient validation of inputs.

#### 7. What is a [security token](https://en.wikipedia.org/wiki/Security_token)? 

A security token is a peripheral device used to gain access to a restricted resource in addition to, or in place of, a password.

## Application Programming Interfaces

### 1. What is an [Application Programming Interface](https://en.wikipedia.org/wiki/API)?

An application programming interface or 'API' is a connection between computer programs.

A document or standard that describes how to build such a connection or interface is called an API specification.

### 2. What is an [Application Binary Interface](https://en.wikipedia.org/wiki/Application_binary_interface)?

An Application binary interface or 'ABI' is an interface between two *binary* program modules. Often, one module is a library or OS facility, and the other is a program run by a user.

### 3. What is [gRPC](https://grpc.io/about/)?

gRPC is an open source Remote Procedure Call (RPC) framework originally created by Google.

### 4. List the [gRPC feature set](https://grpc.io/about/#core-features-that-make-it-awesome).

- Idiomatic client libraries
- simple service definition framework
- Bi-directional streaming with http/2 based transport
- Pluggable auth, tracing, load balancing and health checking

### 5. What is [gRPC-Web](https://grpc.io/docs/platforms/web/)?
A JavaScript implementation of gRPC for browser clients. 

gRPC-Web clients connect to gRPC services via a special proxy; by default, gRPC-web uses Envoy.

### 6. What is [GraphQL](https://graphql.org/learn/)?

GraphQL is a query language for your API, and a server-side runtime for executing queries using a type system.

GraphQL is typically served over HTTP via a single endpoint which expresses the full set of capabilities of the service.

### 7. What is [HTTP](https://datatracker.ietf.org/doc/html/rfc9112)?

The Hypertext Transfer Protocol (HTTP) is a stateless application-level request/response protocol for hypertext information systems.

HTTP is also designed for use as an intermediation protocol, wherein proxies and gateways can translate non-HTTP information systems into a generic interface.

### 8. What is [REST](https://ics.uci.edu/~fielding/pubs/dissertation/rest_arch_style.htm)?

Representation State Transfer or 'REST' is an architectural style for distributed hypermedia systems.

Under REST, no session state on the server component is allowed. Each request from client to server must contain all of the information necessary to understand the request, and stored context must be kept entirely on the client.

REST response data must be labeled as cacheable or non-cacheable. RESTful architecture may be layered such that each component cannot "see" beyond the immediate layer with which they are interacting.

### 9. What are [Multipurpose Internet Mail Extensions](https://www.ietf.org/rfc/rfc2045.txt)?

'MIME' is standard that extends the format of email messages to support text in character sets other than ASCII, as well as multi-media attachments, wherein message bodies can contain multiple parts.

While MIME was designed mainly for SMTP, MIME headers are also utilized in other communication protocols like HTTP.

## Information Security

### 1. What is the [CIA triad](https://www.nccoe.nist.gov/publication/1800-26/VolA/index.html)?

The "CIA" triad epresents the three pillars of information security:
- Confidentiality: preserving authorized restrictions on information access and disclosure.
- Integrity: guarding against improper information modification or destruction.
- Availability: ensuring timely and reliable access to and use of information.

### 2. What is the [Hashed Message Authentication Code](https://datatracker.ietf.org/doc/html/rfc2104)?

A hashed message authentication code or 'HMAC' is a MAC involving a cryptographic hash function and a secret cryptographic key.

HMAC can provide authentication using a shared secret instead of using digital signatures, by delegating the key exchange to the communicating parties, who are responsible for establishing and using a trusted channel.
## Microsoft .NET

### 1. What is [.NET](https://dotnet.microsoft.com/en-us/learn/dotnet/what-is-dotnet)?

.NET is a free and open-source application platform supported by Microsoft.

.NET is supported on Android, Apple, Linux, and Windows operating systems.

### 2. What is [NuGet](https://www.nuget.org/)?

NuGet is the package manager for .NET. The NuGet client tools provide the ability to produce and consume packages.

The NuGet Gallery is the central package repository used by all package authors and consumers.

### 2. What is [System.IDisposable](https://learn.microsoft.com/en-us/dotnet/fundamentals/runtime-libraries/system-idisposable)?

`System.IDisposable` is a system interface used to release unmanaged resources like window handles, or open files and streams.

A IDisposable object is disposed of using either a `Dispose` method in a try/finally block, or `using` statement.

## OAuth

### 1. What is the [OAuth 2.0 Authorization Framework](https://datatracker.ietf.org/doc/html/rfc6749)?

OAuth 2.0 is is an open standard for authorization and access delegation providing flows for web apps, desktop apps, mobile phones, and IoT devices.

### Describe the OAuth [Abstract Protocol Flow](https://datatracker.ietf.org/doc/html/rfc6749#section-1.2).

```
     +--------+                               +---------------+
     |        |--(A)- Authorization Request ->|   Resource    |
     |        |                               |     Owner     |
     |        |<-(B)-- Authorization Grant ---|               |
     |        |                               +---------------+
     |        |
     |        |                               +---------------+
     |        |--(C)-- Authorization Grant -->| Authorization |
     | Client |                               |     Server    |
     |        |<-(D)----- Access Token -------|               |
     |        |                               +---------------+
     |        |
     |        |                               +---------------+
     |        |--(E)----- Access Token ------>|    Resource   |
     |        |                               |     Server    |
     |        |<-(F)--- Protected Resource ---|               |
     +--------+                               +---------------+
```

A. The client requests authorization from the resource owner. The authorization request can be made directly to the resource owner or indirectly via the authorization server.

B. The client receives an authorization grant, which is a credential representing the resource owner's authorization, expressed using one of four grant types or using an extension grant type. The authorization grant type depends on the method used by the client to request authorization and the types supported by the authorization server.

C. The client requests an access token by authenticating with the authorization server and presenting the authorization grant.

D. The authorization server authenticates the client and validates the authorization grant, and if valid, issues an access token.

E. The client requests the protected resource from the resource server and authenticates by presenting the access token.

F. The resource server validates the access token, and if valid, serves the request.

### 2. 

```
     +----------+
     | Resource |
     |   Owner  |
     |          |
     +----------+
          ^
          |
         (B)
     +----|-----+          Client Identifier      +---------------+
     |         -+----(A)-- & Redirection URI ---->|               |
     |  User-   |                                 | Authorization |
     |  Agent  -+----(B)-- User authenticates --->|     Server    |
     |          |                                 |               |
     |         -+----(C)-- Authorization Code ---<|               |
     +-|----|---+                                 +---------------+
       |    |                                         ^      v
      (A)  (C)                                        |      |
       |    |                                         |      |
       ^    v                                         |      |
     +---------+                                      |      |
     |         |>---(D)-- Authorization Code ---------'      |
     |  Client |          & Redirection URI                  |
     |         |                                             |
     |         |<---(E)----- Access Token -------------------'
     +---------+       (w/ Optional Refresh Token)
```

### 3. What is OAuth scope?

Scope is a mechanism in OAuth 2.0 to limit an application's access to a user's account. An application can request one or more scopes and the access token issued to the application will be limited to the scopes granted.

### 4. How should one implement [OAuth 2.0 for Browser-Based Applications?](https://datatracker.ietf.org/doc/html/draft-ietf-oauth-browser-based-apps)

- Browser-based applications MUST implement the Proof Key for Code Exchange extension when obtaining an access token.
- Browser-based applications MUST prevent CSRF attacks against their redirect URI.
- Clients MUST register redirect URIs with the authorization server.

### 5. What is [Proof Key for Code Exchange](https://datatracker.ietf.org/doc/html/rfc7636)?

Proof Key for Code Exchange (abbreviated PKCE, pronounced “pixie”) is an extension to the authorization code flow to prevent CSRF and authorization code injection attacks.

The technique involves the client first creating a secret on each authorization request, and then using that secret again when exchanging the authorization code for an access token. This way if the code is intercepted, it will not be useful since the token request relies on the initial secret.

### 6. What is [OpenID Connect](https://www.openid.net/developers/how-connect-works/)?

OpenID Connect is an interoperable authentication protocol based on the OAuth 2.0 framework.

The specification suite is extensible to support a range of optional features such as encryption of identity data, discovery of OpenID Providers, and session logout.

## Object-oriented Programming

### 1. What is [Object-oriented programming](https://en.wikipedia.org/wiki/Object-oriented_programming)?

Object-oriented programming or 'OOP' is a programming paradigm based on the concept of objects, which contain data in the form of fields and code in the form of methods.

### 2. What is Inheritance?

Inheritance is an OOP code reuse and extensibility pattern, either class-based or protoype-based, implemented via dynamic dispatch.

### 3. What is data abstraction vs. encapsulation?

Data abstraction is a design pattern in which data are visible only to semantically related functions.

Encapsulation prevents external code from being concerned with the internal workings of an object.

## OS-level virtualization

### 1. What is [os-level virtualization](https://en.wikipedia.org/wiki/OS-level_virtualization)?

'OS-level virtualization' or 'containerization' is a virtualization paradigm in which the kernel allows the existence of multiple isolated user space instances called containers.

OS-level virtualization usually imposes less overhead than machine virtualization because programs use the operating system's normal system call interface.

### 2. What is the [Open Container Initiative](https://opencontainers.org/)?

The 'Open Container Initiative' is an open governance structure for the express purpose of creating open industry standards around container formats and runtimes.

The OCI contains three specifications:
- the Runtime Specification (runtime-spec)
- the Image Specification (image-spec)
- the Distribution Specification (distribution-spec)

### 3. What is [containerd](https://containerd.io/)?

'containerd' is an industry-standard container runtime with an emphasis on simplicity, robustness, and portability.

'containerd' is available as a daemon for Linux and Windows, which can manage the complete container lifecycle:
- image transfer and storage
- container execution and supervision
- low-level storage 
- network attachments, etc.

## 4. What is [Docker](https://docs.docker.com/get-started/docker-overview/)?

'Docker' is a freemium PaaS product suite used to deliver software packages as containers.

'Docker Engine' is an open source technology for building and containerizing applications, with the following components:
- A server with a long-running daemon process—`dockerd`
- APIs which specify interfaces that programs can use to instruct the Docker daemon.
- A command line interface (CLI) client—`docker`

## 5. What is a [Dockerfile](https://docs.docker.com/reference/dockerfile/)?

Docker builds images automatically by reading the instructions from a 'Dockerfile'.

A Dockerfile is a text document that contains all the commands to assemble an image.

## 6. List Dockerfile [instructions](https://docs.docker.com/reference/dockerfile/#overview).

| Instruction   | Description                                          |
|---------------|------------------------------------------------------|
| ADD           | Add local or remote files and directories.           |
| ARG           | Use build-time variables.                            |
| CMD           | Specify default commands.                           |
| COPY          | Copy files and directories.                         |
| ENTRYPOINT    | Specify default executable.                         |
| ENV           | Set environment variables.                          |
| EXPOSE        | Describe which ports your application is listening on. |
| FROM          | Create a new build stage from a base image.          |
| HEALTHCHECK   | Check a container's health on startup.              |
| LABEL         | Add metadata to an image.                           |
| MAINTAINER    | Specify the author of an image.                     |
| ONBUILD       | Specify instructions for when the image is used in a build. |
| RUN           | Execute build commands.                             |
| SHELL         | Set the default shell of an image.                  |
| STOPSIGNAL    | Specify the system call signal for exiting a container. |
| USER          | Set user and group ID.                              |
| VOLUME        | Create volume mounts.                               |
| WORKDIR       | Change working directory.                           |

## 7. What are Docker [multi-stage builds](https://docs.docker.com/build/building/multi-stage/)?

With multi-stage builds, multiple `FROM` statements are used in a Dockerfile.

Each `FROM` instruction can use a different base, and each of them begins a new stage of the build.

## 8. What are Docker [tags](https://docs.docker.com/reference/glossary/#tag)?

A 'tag' is a label applied to a Docker image in a repository.

Tags are [formatted](https://docs.docker.com/reference/cli/docker/image/tag/#description) with the following format:

`[HOST[:PORT_NUMBER]/]PATH` where `PATH` is composed of `[NAMESPACE/]REPOSITORY`.

Artifacts can be selectively copied from one stage to another, reducing the size of the final image.
