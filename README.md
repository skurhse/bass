# 🐟 bass

`Bass` is a collection of hypertext [DevOps](https://en.wikipedia.org/wiki/DevOps) flashcards made to reinforce comprehension.

Navigate bass using the GitHub [Table of Contents button](https://github.blog/changelog/2021-04-13-table-of-contents-support-in-markdown-files/) on the upper right (☰).

Card categories are listed in alphabetical order. Sections contain one or more 'What is?'-style question to establish foundational terms.

## Agile Software Development

### 1. Recite the [Agile Manifesto](https://en.wikipedia.org/wiki/Agile_software_development).

We are uncovering better ways of developing software by doing it and helping others do it.

Through this work we have come to value:

- Individuals and interactions over processes and tools
- Working software over comprehensive documentation
- Customer collaboration over contract negotiation
- Responding to change over following a plan

That is, while there is value in the items on the right, we value the items on the left more.

### 2. List the [twelve principles of Agile Software](https://agilemanifesto.org/principles.html).

- Our highest priority is to satisfy the customer through early and continuous delivery of valuable software.
- Welcome changing requirements, even late in development. Agile processes harness change for the customer's competitive advantage.
- Deliver working software frequently, from a couple of weeks to a couple of months, with a preference to the shorter timescale.
- Business people and developers must work together daily throughout the project.
- Build projects around motivated individuals. Give them the environment and support they need, and trust them to get the job done.
- The most efficient and effective method of conveying information to and within a development team is face-to-face conversation.
- Working software is the primary measure of progress.
- Agile processes promote sustainable development. The sponsors, developers, and users should be able to maintain a constant pace indefinitely.
- Continuous attention to technical excellence and good design enhances agility.
- Simplicity--the art of maximizing the amount of work not done--is essential.
- The best architectures, requirements, and designs emerge from self-organizing teams.
- At regular intervals, the team reflects on how to become more effective, then tunes and adjusts its behavior accordingly.

## Application Security

### 1. What is the [OAuth 2.0 Authorization Framework](https://datatracker.ietf.org/doc/html/rfc6749)?

OAuth 2.0 is is an open standard for authorization and access delegation providing flows for web apps, desktop apps, mobile phones, and IoT devices.

### 2. What is OAuth scope?

Scope is a mechanism in OAuth 2.0 to limit an application's access to a user's account. An application can request one or more scopes and the access token issued to the application will be limited to the scopes granted.

### 3. How should one implement [OAuth 2.0 for Browser-Based Applications?](https://datatracker.ietf.org/doc/html/draft-ietf-oauth-browser-based-apps)

- Browser-based applications MUST implement the Proof Key for Code Exchange extension when obtaining an access token.
- Browser-based applications MUST prevent CSRF attacks against their redirect URI.
- Clients MUST register redirect URIs with the authorization server.

### 4. What is [Proof Key for Code Exchange](https://datatracker.ietf.org/doc/html/rfc7636)?

Proof Key for Code Exchange (abbreviated PKCE, pronounced “pixie”) is an extension to the authorization code flow to prevent CSRF and authorization code injection attacks.

The technique involves the client first creating a secret on each authorization request, and then using that secret again when exchanging the authorization code for an access token. This way if the code is intercepted, it will not be useful since the token request relies on the initial secret.

### 5. What is [OpenID Connect](https://www.openid.net/developers/how-connect-works/)?

OpenID Connect is an interoperable authentication protocol based on the OAuth 2.0 framework.

The specification suite is extensible to support a range of optional features such as encryption of identity data, discovery of OpenID Providers, and session logout.

## Application Programming Interfaces

### 1. What is [gRPC](https://grpc.io/about/)?
gRPC is an open source Remote Procedure Call (RPC) framework originally created by Google.

### 2. List the [gRPC feature set](https://grpc.io/about/#core-features-that-make-it-awesome).

- Idiomatic client libraries
- simple service definition framework
- Bi-directional streaming with http/2 based transport
- Pluggable auth, tracing, load balancing and health checking

### 3. What is [gRPC-Web](https://grpc.io/docs/platforms/web/)?
A JavaScript implementation of gRPC for browser clients. 

gRPC-Web clients connect to gRPC services via a special proxy; by default, gRPC-web uses Envoy.

### 4. What is [GraphQL](https://graphql.org/learn/)?

GraphQL is a query language for your API, and a server-side runtime for executing queries using a type system.

GraphQL is typically served over HTTP via a single endpoint which expresses the full set of capabilities of the service.

## Kubernetes

### 1. What is [Kubernetes](https://kubernetes.io/docs/concepts/overview/)?

Kubernetes is an open-source container orchestration platform that automates the deployment and management of workloads and services.

### 2. List the [Kubernetes feature set](https://kubernetes.io/docs/concepts/overview/#why-you-need-kubernetes-and-what-can-it-do).

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

## Linux

### 1. What is [Linux](https://en.wikipedia.org/wiki/Linux)?

Linux is a family of open-source Unix-like operating systems based on the Linux kernel.

### 2. List commercial enterprise distributions of Linux.

- [Amazon Linux 2](https://aws.amazon.com/amazon-linux-2)
- [Red Hat Enterprise Linux](https://www.redhat.com/en/technologies/linux-platforms/enterprise-linux)
- [SUSE Linux Enterprise](https://www.suse.com/products/server)

### 3. List non-commercial enterprise distributions of Linux.
- [Alpine Linux](https://www.alpinelinux.org)
- [Debian](https://www.debian.org)
- [Rocky Linux](https://rockylinux.org/)
- [Ubuntu](https://ubuntu.com/)

### 4. What is [POSIX.1-2017](https://pubs.opengroup.org/onlinepubs/9699919799/)?
The *Portable Operating System Interface* specifications are a standard created by the [IEEE Computer Society](https://www.computer.org/about) for maintaining compatibility between operating systems.

POSIX.1-2017 defines a standard operating system interface and environment, including a command interpreter (or “shell”), and common utility programs to support applications portability at the source code level.

### 5. What is [top](https://en.wikipedia.org/wiki/Top_(software))?

`top` is process monitor program that displays sorted information about CPU and memory utilization.

The Linux version of `top` is part of the `procps-ng` tools group.

### 6. What is [lsof](https://en.wikipedia.org/wiki/Lsof)?

lsof is a command meaning "list open files", which reports a list of all open files and the processes that opened them.

Open files in the system include disk files, named pipes, network sockets and devices.

### 7. What is [sysstat](https://en.wikipedia.org/wiki/Sysstat)?

`sysstat` or "system statistics" is a collection of Linux tools used to monitor system performance and usage activity.

The systat program `sar` is used to report on various system loads, including CPU activity, memory/paging, interrupts, device load, network and swap space utilization.

`sadc` is the system activity data collector and backend.

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

## Network Security

### 1. What is [TLS 1.3](https://datatracker.ietf.org/doc/rfc8446/)?

Transport Layer Security (TLS) is a cryptographic protocol that allows client/server applications to communicate over the Internet in a way that is designed to prevent eavesdropping, tampering, and message forgery.

Once the client and server have agreed to use TLS, they negotiate a stateful connection by using a handshaking procedure. The protocols use a handshake with an asymmetric cipher to establish cipher settings and a session-specific shared key with which further communication is encrypted using a symmetric cipher.

### 2. What is [Public-key infrastructure](https://en.wikipedia.org/wiki/Public_key_infrastructure)?

PKI or 'Public-key infrastructure' is a set of roles, policies and procedures needed to manage public key certificates: electronic documents used to prove the validity of a public key.

### 3. What is a Certificate Authority?

A CA or 'Certificate authority' is a root certificate issuer, usually a company that charges customers a fee to issue certificates for them.

A CA acts as a trusted third party—trusted both by the subject (owner) of the certificate and by the party relying upon the certificate.

### 4. What is [X.509](https://www.itu.int/rec/T-REC-X.509)? 

X.509 is an International Telecommunication Union (ITU) framework for public-key certificates.

X.509 includes the specification of data objects, revocation notices and critical components of a public-key infrastructure. 

## Object-oriented Programming

### 1. What is [Object-oriented programming](https://en.wikipedia.org/wiki/Object-oriented_programming)?

Object-oriented programming or 'OOP' is a programming paradigm based on the concept of objects, which contain data in the form of fields and code in the form of methods.

### 2. What is Inheritance?

Inheritance is an OOP code reuse and extensibility pattern, either class-based or protoype-based, implemented via dynamic dispatch.

### 3. What is data abstraction vs. encapsulation?

Data abstraction is a design pattern in which data are visible only to semantically related functions.

Encapsulation prevents external code from being concerned with the internal workings of an object.

## Software as a Service

### 1. What is [SaaS](https://en.wikipedia.org/wiki/Software_as_a_service)?

Software-as-a-service (/sæs/) is a form of cloud computing in which the provider manages all the physical and software resources used by the application.

SaaS differs from other software delivery models in that it separates the possession and ownership of software from its use.

### 2. What is the ['Twelve Factor App'](https://12factor.net/)?

The twelve-factor app is a methodology for building software-as-a-service apps that:

- Use declarative formats for setup automation.
- Have a clean contract with the underlying operating system.
- Are suitable for deployment on modern cloud platforms.
- Minimize divergence between development and production.
- Can scale up without significant changes.

### 3. List the twelve factors of a twelve factor application.

1. [Codebase](https://12factor.net/codebase): One codebase tracked in revision control, many deploys.
2. [Dependencies](https://12factor.net/dependencies): Explicitly declare and isolate dependencies.
3. [Config](https://12factor.net/config): Store config in the environment.
4. [Backing services](https://12factor.net/backing-services): Treat backing services as attached resources.
5. [Build, release, run](https://12factor.net/build-release-run): Strictly separate build and run stages.
6. [Processes](https://12factor.net/processes): Execute the app as one or more stateless processes.
7. [Port binding](https://12factor.net/port-binding): Export services via port binding.
8. [Concurrency](https://12factor.net/concurrency): Scale out via the process model.
9. [Disposability](https://12factor.net/disposability): Maximize robustness with fast startup and graceful shutdown.
10. [Dev/prod parity](https://12factor.net/dev-prod-parity): Keep development, staging, and production as similar as possible.
11. [Logs](https://12factor.net/logs): Treat logs as event streams.
12. [Admin processes](https://12factor.net/admin-processes): Run admin/management tasks as one-off processes.
