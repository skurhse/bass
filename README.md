# 🐟 bass

`bass` is a collection of hypertext [DevOps](https://en.wikipedia.org/wiki/DevOps) flashcards made to reinforce comprehension.

- Navigate bass using Table of Contents or the GitHub [outline button](https://github.blog/changelog/2021-04-13-table-of-contents-support-in-markdown-files/) on the upper right (☰).
- Card categories are listed in alphabetical order; cards within categories are listed in logical order.
- Card categories contain one or more 'What is?'-style questions.

## Table of Contents

- [Agile Software Development](#agile-software-development)
- [Application Programming Interfaces](#application-programming-interfaces)
- [Application Security](#application-security)
- [Governance, Risk and Compliance](#governance-risk-and-compliance)
- [Kubernetes](#kubernetes)
- [Information Security](#information-security)
- [Network Engineering](#network-engineering)
- [Network Security](#network-security)
- [Object-oriented Programming](#object-oriented-programming)
- [Site Reliability Engineering](#site-reliability-engineering)
- [Software-as-a-service](#software-as-a-service)
- [Windows Server](#windows-server)

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

### 6. What is [JSON Web Token](https://datatracker.ietf.org/doc/html/rfc7519)?

JSON Web Token or 'JWT' is a compact and URL-safe standard for representing claims to be transferred between two parties.

The claims in a JWT are encoded as a either:
- as a JSON object that is used as the payload of a JSON Web Signature
- as the plaintext of a JSON Web Encryption (JWE) structure

### 7. What is an [injection exploit](https://en.wikipedia.org/wiki/Category:Injection_exploits)?

Injection exploits use data to subvert the intended operation of the system. Injection exploits leverage vulnerabilities resulting from insufficient validation of inputs.

### 8. What is a [security token](https://en.wikipedia.org/wiki/Security_token)? 

A security token is a peripheral device used to gain access to a restricted resource in addition to, or in place of, a password.

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

### 5. What is [HTTP](https://datatracker.ietf.org/doc/html/rfc9112)?

The Hypertext Transfer Protocol (HTTP) is a stateless application-level request/response protocol for hypertext information systems.

HTTP is also designed for use as an intermediation protocol, wherein proxies and gateways can translate non-HTTP information systems into a generic interface.

### 6. What is [REST](https://ics.uci.edu/~fielding/pubs/dissertation/rest_arch_style.htm)?

Representation State Transfer or 'REST' is an architectural style for distributed hypermedia systems.

Under REST, no session state on the server component is allowed. Each request from client to server must contain all of the information necessary to understand the request, and stored context must be kept entirely on the client.

REST response data must be labeled as cacheable or non-cacheable. RESTful architecture may be layered such that each component cannot "see" beyond the immediate layer with which they are interacting.

### 7. What are [Multipurpose Internet Mail Extensions](https://www.ietf.org/rfc/rfc2045.txt)?

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

### 3. List k8s [control plane components](https://kubernetes.io/docs/concepts/overview/components/#control-plane-components)

- [kube-apiserver](https://kubernetes.io/docs/concepts/overview/components/#kube-apiserver) - the front end that exposes the k8s api.
- [etcd](https://kubernetes.io/docs/concepts/overview/components/#etcd) - the backing store for all cluster data.
- [kube-scheduler](https://kubernetes.io/docs/concepts/overview/components/#kube-scheduler) -  selects nodes for pods to run on.
- [kube-controller-manager](https://kubernetes.io/docs/concepts/overview/components/#kube-controller-manager) - runs controller processes.
- [cloud-controller-manager](https://kubernetes.io/docs/concepts/overview/components/#cloud-controller-manager) - runs controllers that are specific to cloud providers.

### 4. List k8s [node components](https://kubernetes.io/docs/concepts/overview/components/#node-components).

- [kubelet](https://kubernetes.io/docs/concepts/overview/components/#kubelet) - manages pod specifications and health.
- [kube-proxy](https://kubernetes.io/docs/concepts/overview/components/#kube-proxy) - maintains network rules on nodes.
- [container runtime](https://kubernetes.io/docs/concepts/overview/components/#container-runtime) - manages the execution and lifecycle of containers.

### 5. List k8s [security mechanisms](https://kubernetes.io/docs/concepts/security/#security-mechanisms)

- [control plane protection](https://kubernetes.io/docs/concepts/security/#control-plane-protection) - control access to the Kubernetes API.
  - [transport security](https://kubernetes.io/docs/concepts/security/controlling-access/#transport-security) - protected with TLS.
  - [authentication](https://kubernetes.io/docs/concepts/security/controlling-access/#authentication) - run one or more authenticator modules.
  - [authorization](https://kubernetes.io/docs/concepts/security/controlling-access/#authorization) - policy-based action control.
- [secrets](https://kubernetes.io/docs/concepts/security/#secrets) - confidentiality protection for configuration values 
- [workload protection](https://kubernetes.io/docs/concepts/security/#workload-protection) - enforce network policies and pod security standards.
- [auditing](https://kubernetes.io/docs/concepts/security/#auditing) - security logging for users and applications.

## Governance, Risk and Compliance

### 1. What is the [Payment Card Industry Data Security Standard](https://docs-prv.pcisecuritystandards.org/PCI%20DSS/Standard/PCI-DSS-v4_0_1.pdf)?

The Payment Card Industry Data Security Standard or 'PCI DSS' is an information security standard used to handle credit cards from major card brands.

PCI DSS is required by brands and created to better control cardholder data and reduce credit card fraud.

### 2. List the six [PCI DSS control objectives](https://docs-prv.pcisecuritystandards.org/PCI%20DSS/Supporting%20Document/PCI_DSS-QRG-v4_0.pdf).

- Build and maintain a secure network and systems.
- Protect cardholder data.
- Maintain a vulnerability management program.
- Implement strong access-control measures.
- Regularly monitor and test networks.
- Maintain an information security policy.

### 3. What are [System & Organization Controls](https://www.aicpa-cima.com/resources/landing/system-and-organization-controls-soc-suite-of-services)?

System and Organization Controls or 'SOC' is a suite of service offerings certified public accounts may provide in connection with system-level controls of a service organization.

### 3. What is General Data Protection Regulation?

General Data Protection Regulation or 'GDPR' is a European Union regulation on information privacy in the European Union and the European Economic Area.

The GDPR's goals are to enhance individuals' control and rights over their personal information and to simplify the regulations for international business.

### 4. What are the [Federal Information Processing Standards](https://www.nist.gov/standardsgov/compliance-faqs-federal-information-processing-standards-fips)?

The Federal Information Processing Standards of the United States or 'FIPS' are a set of publicly announced standards that the National Institute of Standards and Technology developed for use in computer situs of non-military United States government agencies and contractors.

FIPS standards establish requirements for computer security and are intended for cases in which industry standards are non pre-existent.

### 5. What is the [Family Educational Rights and Privacy Act](https://studentprivacy.ed.gov/faq/what-ferpa)?

The Family Educational Rights and Privacy Act or 'FERPA' is a federal law that affords parents the right to have access, amend, and control disclosure of their children’s education records.

When a student turns 18 years old or enters a postsecondary institution, the rights under FERPA transfer from the parents to the student.

### 6. What is a [Chief Information Security Officer](https://en.wikipedia.org/wiki/Chief_information_security_officer)

A chief information security officer or 'CISO' is an executive within an organization responsible for establishing the enterprise program to ensure information assets and technologies are adequately protected.

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

### 5. What is [LDAP](https://datatracker.ietf.org/doc/html/rfc4511)?

The Lightweight Directory Access Protocol or 'LDAP' is an directory services protocol for use over an Internet Protocol network.

Under LDAP, a directory user accesses the Directory through a Directory User Agent (DUA). The agent interacts with one or more Directory System Agents (DSA).

When an LDAP session is created, the authentication state of the session is set to anonymous. The BIND operation establishes the authentication state for a session.

### 6. What is [gcc](https://gcc.gnu.org/)?

 The GNU Compiler Collection or 'GCC' is a collection of compilers from the GNU Project.

GCC includes front ends for C, C++, Objective-C, Fortran, Ada, Go, D and Modula-2 as well as libraries for these languages like `libstdc++`.

### 7. What is [top](https://en.wikipedia.org/wiki/Top_(software))?

`top` is process monitor program that displays sorted information about CPU and memory utilization.

The Linux version of `top` is part of the `procps-ng` tools group.

### 8. What is [lsof](https://en.wikipedia.org/wiki/Lsof)?

lsof is a command meaning "list open files", which reports a list of all open files and the processes that opened them.

Open files in the system include disk files, named pipes, network sockets and devices.

### 9. What is [sysstat](https://en.wikipedia.org/wiki/Sysstat)?

`sysstat` or "system statistics" is a collection of Linux tools used to monitor system performance and usage activity.

The systat program `sar` is used to report on various system loads, including CPU activity, memory/paging, interrupts, device load, network and swap space utilization.

`sadc` is the system activity data collector and backend.

### 10. What is [Bash](https://www.gnu.org/software/bash/)?

Bash or 'Bourne Again SHell' is the is the GNU Project's shell: a computer program that exposes OS services to users and programs.

Bash conforms to the IEEE POSIX P1003.2/ISO 9945.2 Shell and Tools standard and is `sh`-compatible.

### 11. What is [systemd](https://systemd.io/)?

`systemd` is a system and service manager that runs as PID 1 and starts the rest of the system.

`systemd` supports SysV and LSB init scripts and works as a replacement for sysvinit.

Other parts include a logging daemon, and utilities to control basic system configuration.

### 12. What is the [Linux Standard Base](https://wiki.linuxfoundation.org/lsb/about)?

The Linux Standard Base or 'LSB' is standard created by the Linux Foundation that describes the minimum set of APIs a Linux distribution must support.

The LSB working group also provides tools to test support.

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

## Network Engineering

### 1. What is the IETF?

Lorum ipsum.

### 2. What is the [Internet Protocol](https://datatracker.ietf.org/doc/html/rfc791)?

The Internet Protocol or 'IP' is a protocol designed for use in interconnected systems of packet-switched computer communication networks.

IP is responsible for addressing host interfaces, encapsulating data into datagrams and routing datagrams from a source to a destination.

### 3. What is [IPv6](https://datatracker.ietf.org/doc/html/rfc8200)?

IP version 6 is the successor to IP version 4.

IPv6 implements the following change set 

### 4. What is TCP?

Lorum ipsum.

### 5. What is UDP?

Lorum ipsum.

### 6. What is ICMP?

Lorum ipsum.

### 7. What is traceroute?

Lorum ipsum.

### 8. What is [DNS](https://datatracker.ietf.org/doc/html/rfc1034)?

The Domain Name System or 'DNS' is a hierarchical and distributed name service that provides a naming system for resources on Internet Protocol networks.

DNS delegates the responsibility of assigning domain names to Internet resources by designating authoritative name servers.

### 9. What is [WHOIS](https://datatracker.ietf.org/doc/html/rfc3912)?

WHOIS, pronounced "who is", is a TCP-based transaction-oriented query/response protocol used to provide information services to Internet users.

WHOIS was originally used to provide information about registered domain names, current deployments cover a much broader range of information services.

The WHOIS protocol has not been internationalised and has no provisions for strong security.

### 10. What is a [subnetting](https://en.wikipedia.org/wiki/Subnet)?

A subnetwork, or subnet, is a logical subdivision of an IP network.

Computers that belong to the same subnet are addressed with an identical group of its most-significant bits of their IP addresses.

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

## Site Reliability Engineering

### 1. What is a [Recovery Time Objective](https://en.wikipedia.org/wiki/IT_disaster_recovery#Recovery_Time_Objective)?

Recovery Time Objective or 'RTO' is the targeted duration of time within which a business process must be restored after a disruption

### 2. What is a [Recovery Point Objective](https://en.wikipedia.org/wiki/IT_disaster_recovery#Recovery_Point_Objective)

A Recovery Point Objective or 'RPO' is the maximum acceptable interval during which transactional data is lost from an IT service.

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

## Windows Server

### 1. What is [Windows Server](https://learn.microsoft.com/en-us/windows-server/get-started/get-started-with-windows-server)?

Windows Server is a group of server operating systems developed by Microsoft with the latest long-term service channel release being Windows Server 2022.

Windows Server is used to build infrastructure for connected applications, networks, and web services. It bridges on-premises environments with Azure.

### 2. What is the [Windows Registry](https://learn.microsoft.com/en-us/troubleshoot/windows-server/performance/windows-registry-advanced-users#description-of-the-registry)?

The Windows Registry is a central hierarchical database used to store configurations for users, applications, and hardware devices.

### 3. List Windows Registry [predefined keys](https://learn.microsoft.com/en-us/windows/win32/sysinfo/predefined-keys).

- HKEY_CURRENT_USER
- HKEY_USERS
- HKEY_LOCAL_MACHINE
- HKEY_CLASSES_ROOT
- HKEY_CURRENT_CONFIG	

