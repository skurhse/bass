# 🐟 bass

`Bass` is a collection of hypertext [DevOps](https://en.wikipedia.org/wiki/DevOps) flashcards made to help reinforce comprehension.

Navigate bass using the GitHub [Table of Contents button](https://github.blog/changelog/2021-04-13-table-of-contents-support-in-markdown-files/) on the upper right (☰).

Card categories are listed in alphabetical order.

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

