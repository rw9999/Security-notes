# Cloud and Virtualization Security

Organizations of all sizes are drawn to the agility, flexibility, cost-effectiveness, and scalability of cloud computing solutions and are quickly integrating them into their technology environment, if not shifting completely to the cloud.

New businesses are taking a “born in the cloud” approach that allows them to run their entire businesses without operating a single server.

### Exploring the Cloud

Cloud computings fundamental idea is straightforward: cloud service providers deliver computing services to their customers over the Internet.

This can be as simple as Google providing their Gmail service to customers in a web browser or Amazon Web Services (AWS) providing virtualized servers to corporate clients who use them to build out their own technology environment.

In each of these cases, the provider builds an IT service and uses the Internet to deliver that service to its customers.

Here's a more formal definition of cloud computing from the National Institute of Standards and Technology:

Cloud computing is a model for enabling ubiquitous, convenient, on-demand network access to a shared pool of configurable computing resources (e.g., networks, servers, storage, applications, and services) that can be rapidly provisioned and released with minimal management effort or service provider 
interaction.

Cloud computing is ubiquitous and convenient. The resources provided by the cloud are available to customers wherever they may be. If you have access to the Internet, you can access the cloud. It doesn't matter whether you're sitting in your office or on the beach. 

Cloud computing is also on-demand. In most cases, you can provision and de-provision cloud resources in a few minutes with a few clicks. You can acquire new cloud resources almost immediately when you need them and you can turn them off quickly (and stop paying for them) when they are no longer required.

Many of the key benefits of the cloud derive from the fact that it uses a shared pool of resources that may be configured for different purposes by different users.

This sharing allows **oversubscription** because not everyone will use all their resources at the same time and it achieves economies of scale.

The fact that many different users share resources in the same cloud infrastructure is known as **multitenancy**. 

In a multitenant environment, the same physical hardware might support the workloads and storage needs of many different customers, all of whom operate without any knowledge of or interaction with their fellow customers.

The cloud offers a variety of configurable computing resources. You can acquire infrastructure components, platforms, or entire applications through cloud service providers and then configure them to meet your needs.

The rapid provisioning and releasing of cloud services also takes place with minimal management effort and service provider interaction.

Unlike on-premises hardware acquisition, you can provision cloud services yourself without dealing with account representatives and order processing times.

If you need a new cloud server, you don't need to call up Microsoft, Amazon, or Google. You just click a few buttons on their website and you're good to go. From the perspective of most users, the cloud presents seemingly infinite capacity.

#

### Benefits of the Cloud

As organizations consider the appropriate role for the cloud in their technology infrastructure, the key issue they seek to address is the appropriate balance of on-premises versus cloud/off-premises resources.

Understanding some of the key benefits provided by the cloud is helpful to finding that correct balance:
 
- **On-demand self-service computing**. Cloud resources are available when and where you need them. This provides developers and technologists with incredible agility, reducing cycle times and increasing the speed of deployment.

- **Scalability**. As the demand for a cloud-based service increases, customers can manually or automatically increase the capacity of their operations.

In some cloud environments, the cloud service provider may do this in a manner that is completely transparent to the customer, scaling resources behind the scenes. Cloud providers achieve scalability in two ways:

- **Vertical scaling** increases the capacity of existing servers. For example, you might change the number of CPU cores or the amount of memory assigned to a server. In the physical world, this means opening up a server and adding physical hardware. In the cloud, you can just click a few buttons and add memory or compute capacity.

- **Horizontal scaling** adds more servers to a pool of clustered servers. If you run a website that supports 2,000 concurrent users with two servers, you might add a new server every time your typical usage increases another 1,000 users. Cloud computing makes this quite easy, as you can just replicate your existing server with a few clicks.

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/14bf872d-94fc-49e3-a7fe-544ca860cf13)

- **Elasticity**. Elasticity and scalability are closely related. Scalability is focused on rapidly increasing capacity. Elasticity says that capacity should expand and **contract** as needs change to optimize costs. If your website starts to experience a burst in activity, elasticity allows you to automatically add servers until that capacity is met and then remove those servers when the capacity is no longer needed.

- **Measured service**. Everything you do in the cloud is measured by the provider. Providers track the number of seconds of processing time you consume, the amount of storage you occupy, the number of log entries that you generate, and many other measures. They use this information to be able to assess charges based on your usage. You pay for exactly what you use— no more and no less.

- **Agility and flexibility**. The speed to provision cloud resources and the ability to use them for short periods of time lends tremendous agility and flexibility to technology organizations. Developers and engineers who wish to try a new idea can rapidly spin up a test environment, evaluate the approach, and decide whether to move it into production with minimal effort and cost.

#

### Cloud Roles

In any cloud computing environment, different organizations take on different roles. There are five key roles in the cloud:

- **Cloud service providers** are the firms that offer cloud computing services to their customers. They may build their own datacenters or work hand in hand with other cloud providers to deliver their service, but their defining characteristic is they offer a cloud service for sale.

- **Cloud consumers** are the organizations and individuals who purchase cloud services from cloud service providers. They use these services to meet their own business requirements.

- **Cloud partners** (or cloud brokers) are organizations that offer ancillary products or services that support or integrate with the offerings of a cloud service provider. Cloud partners may offer training or consulting to help customers make use of a cloud service, provide software development and integration services, or perform any other service that facilitates the use of a cloud offering.

- **Cloud auditors** are independent organizations that provide third-party assessments of cloud services and operations. Depending on the scope of the audit engagement, they may provide a general assessment of a cloud environment or focus on security controls for a narrow scope of operations.

- **Cloud carriers** serve as the intermediaries that provide the connectivity that allows the delivery of cloud services from providers to consumers.

The same organization may take on multiple roles. For example, if an organization purchases cloud infrastructure components from a cloud service provider, they are a cloud consumer. If they use those infrastructure components to build a cloud software application that they offer to their own customers, then they are also a cloud service provider themselves.

#

### Cloud Service Models

We categorize the types of services offered by cloud service providers into several buckets based upon the nature of the offering. 

The wide variety of services available in the cloud are often described as “anything as a service,” or the acronym XaaS, where X indicates the nature of the specific service. 

Although there are many different types of cloud service, we often describe them using three major service models: infrastructure as a service (IaaS), software as a service (SaaS), and platform as a service (PaaS).

#

### Infrastructure as a Service (IaaS)

Infrastructure as a service (IaaS) offerings allow customers to purchase and interact with the basic building blocks of a technology infrastructure. These include computing, storage, and networks.

Customers then have the flexibility to configure and manage those services in any way they like to meet their own business needs. The customer doesn't need to worry about the management of the underlying hardware, but they do have the ability to customize components to meet their needs.

In the IaaS model, the cloud service provider is responsible for managing the physical facilities and the underlying hardware. The provider must also implement security controls that prevent customers from eavesdropping on each other or interfering with each other's use of the infrastructure environment.

Although there are dozens of IaaS providers in the marketplace today, the market is currently dominated by three major players: Amazon Web Services (AWS), Microsoft Azure, and Google Cloud Platform (GCP).

These three providers serve the vast majority of IaaS customers and offer a wide breadth of compute, storage, and networking products, as well as supplementary services that reside higher in the stack, such as security monitoring, content delivery networks, and application streaming.

#

### Software as a Service (SaaS)

Software as a service (SaaS) offerings provide customers with access to a fully managed application running in the cloud.

The provider is responsible for everything from the operation of the physical datacenters to the performance management of the application itself, although some of these tasks may be outsourced to other cloud service providers.

In the SaaS model, the customer is only responsible for limited configuration of the application itself, the selection of what data they wish to use with the cloud solution, and the use of application-provided access controls to limit access to that data.

The SaaS model is widely used to deliver applications ranging from web-based email to enterprise resource planning (ERP) and customer relationship management (CRM) suites. 

Customers enjoy continued access to cutting-edge software and typically pay for SaaS services using a subscription model. Users of the product normally access the application through a standard web browser and may even use a thin client device, such as the Google Chromebook.

#

### Platform as a Service (PaaS)

Platform as a service (PaaS) offerings fit into a middle ground between SaaS and IaaS solutions.

In a PaaS offering, the service provider offers a platform where customers may run applications that they have developed themselves.

The cloud service provider builds and manages the infrastructure and offers customers an execution environment, which may include code libraries, services, and tools that facilitate code execution.

**Function as a service** (FaaS) platforms are an example of PaaS computing.

This approach allows customers to upload their own code functions to the provider and then the provider will execute those functions on a scheduled basis, in response to events, and/or on demand.

The AWS Lambda service is an example of a FaaS/PaaS offering. Lambda allows customers to write code in Python, Java, C+, PowerShell, Node.js, Ruby, Go, and other programming languages. The Lambda function is a Python function designed to read the current temperature from an Internet of Things (IoT) temperature sensor.

Because FaaS environments do not expose customers to the actual server instances executing their code, they are often referred to as **serverless computing** environments.

However, this is somewhat of a misnomer, since FaaS environments most certainly do have servers running the code, but they do so in a manner that is transparent to the FaaS customer.

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/79a4f998-83bb-4f78-b134-8543bb28c5d5)

#

### Managed Services

Organizations may also choose to outsource some or all of the management of their technology infrastructure.

**Managed service providers** (MSPs) are services organizations that provide information technology as a service to their customers. MSPs may handle an organization's IT needs completely, or they may offer focused services such as network design and implementation, application monitoring, or cloud cost management.

MSPs are not necessarily cloud service providers themselves (although they may be both MSP and CSP). They are typically capable of working across a customer's total environment, including both cloud and on-premises deployments.

When MSPs offer security services, they are commonly referred to as managed security service providers (MSSPs). Services offered by MSSPs include security monitoring, vulnerability management, incident response, and firewall management.

## Cloud Deployment Models

Cloud deployment models describe how a cloud service is delivered to customers and whether the resources used to offer services to one customer are shared with other customers.

### Public Cloud

When we think of “the cloud,” we commonly first think of public cloud offerings.

Public cloud service providers deploy infrastructure and then make it accessible to any customers who wish to take advantage of it in a multitenant model. A single customer may be running workloads on servers spread throughout one or more datacenters, and those servers may be running workloads for many different customers simultaneously.

The public cloud supports all cloud service models. Public cloud providers may offer IaaS, PaaS, SaaS, and FaaS services to their customers.

The key distinction is that those services do not run on infrastructure dedicated to a single customer but rather on infrastructure that is available to the general public. AWS, Microsoft Azure, and Google Compute Platform all use the public cloud model.

#

### Private Cloud

The term private cloud is used to describe any cloud infrastructure that is provisioned for use by a single customer.

This infrastructure may be built and managed by the organization that will be using the infrastructure, or it may be built and managed by a third party. The key distinction here is that only one customer uses the environment.

For this reason, private cloud services tend to have excess unused capacity to support peak demand and, as a result, are not as costefficient as public cloud services.

#

### Community Cloud

A community cloud service shares characteristics of both the public and private models.

Community cloud services do run in a multitenant environment, but the tenants are limited to members of a specifically designed community. Community membership is normally defined based on shared mission, similar security and compliance requirements, or other commonalities.

The HathiTrust digital library is an example of community cloud in action. Academic research libraries joined together to form a consortium that provides access to their collections of books. Students and faculty at HathiTrust member institutions may log into the community cloud service to access resources.

#

### Hybrid Cloud

Hybrid cloud is a catch-all term used to describe cloud deployments that blend public, private, and/or community cloud services together.

It is not simply purchasing both public and private cloud services and using them together. Hybrid clouds require the use of technology that unifies the different cloud offerings into a single coherent platform. For example, a firm might operate their own private cloud for the majority of their workloads and then leverage public cloud capacity when demand exceeds the capacity of their private cloud infrastructure. This approach is known as public **cloud bursting**.

AWS Outposts are examples of hybrid cloud computing. Customers of this service receive a rack of computing equipment that they install in their own datacenters. The equipment in the rack is maintained by AWS but provisioned by the customer in the same manner as their AWS public cloud resources. This approach qualifies as hybrid cloud because customers can manage both their on-premises AWS Outposts private cloud deployment and their public cloud AWS services through the same management platform.

#

### Shared Responsibility Model

In some ways, cybersecurity work in a cloud-centric environment is quite similar to on-premises cybersecurity. 

No matter where our systems are hosted, we still need to think about the confidentiality, integrity, and availability of our data and implement strong access controls and other mechanisms that protect those primary objectives.

However, cloud security operations also differ significantly from on-premises environments because cloud customers must divide responsibilities between one or more service providers and the customers' own cybersecurity teams.

This type of operating environment is known as the shared responsibility model.

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/d2dad6c7-86aa-4b9b-b871-58ff229e2631)

In some cases, this division of responsibility is straightforward. Cloud providers, by their nature, are always responsible for the security of both hardware and the physical data center environment. If the customer were handling either of these items, the solution would not fit the definition of cloud computing.

The differences in responsibility come higher up in the stack and vary depending on the nature of the cloud service being used.

In an IaaS environment, the customer takes over security responsibility for everything that isn't infrastructure—the operating system, applications, and data that they run in the IaaS environment.

In a PaaS solution, the vendor also takes on responsibility for the operating system, whereas the customer retains responsibility for the data being placed into the environment and configuring its security.

Responsibility for the application layer is shared between the service provider and the customer, and the exact division of responsibilities shifts based on the nature of the service.

For example, if the PaaS platform provides runtime interpreters for customer code, the cloud provider is responsible for the security of those interpreters.

In a SaaS environment, the provider takes on almost all security responsibility.

The customer retains some shared control over the data that they place in the SaaS environment and the configuration of access controls around that data, but the SaaS provider is being paid to take on the burden of most operational tasks, including cybersecurity.

#

### Cloud Standards and Guidelines

The cybersecurity community offers a variety of reference documents to help organizations come to a common understanding of the cloud and cloud security issues.

The Cloud Reference Architecture, published by the National Institute for Standards and Technology (NIST) in their SP 500-292, offers a high-level taxonomy for cloud services.

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/059fc9a1-912f-43f5-ae8c-7a85f498a295)

The Cloud Security Alliance (CSA) is an industry organization focused on developing and promoting best practices in cloud security.

They developed the Cloud Controls Matrix (CCM) as a reference document designed to help organizations understand the appropriate use of cloud security controls and map those controls to various regulatory standards.

#

### Edge Computing

Many of the applications of the Internet of Things occur out of sight in manufacturing plants, agricultural fields, and even in outer space.

In situations where sensors are in remote locations with poor network connectivity, the traditional cloud model of shipping data back to the cloud for processing doesn't always work well.

Instead, it may make more sense to perform some processing close to the sensor to aggregate and minimize the data transferred back to the cloud.

**Edge computing** approaches seek to address this issue by placing some processing power on the remote sensors, allowing them to preprocess data before shipping it back to the cloud.

This model takes its name from the fact that the computing is being pushed out to sensors that are located on the “edge” of the network.

**Fog computing** is a related concept that uses IoT gateway devices that are located in close physical proximity to the sensors. The sensors themselves don't necessarily have processing power, but they send data to their local gateway that performs preprocessing before sending the results to the cloud.

#

### Virtualization

Cloud computing providers, as well as most other modern datacenter operators, make extensive use of virtualization technology to allow multiple guest systems to share the same underlying hardware.

In a virtualized datacenter, the virtual host hardware runs a special operating system known as a hypervisor that mediates access to the underlying hardware resources.

Virtual machines then run on top of this virtual infrastructure provided by the hypervisor, running standard operating systems such as Windows and Linux variants. The virtual machines may not be aware that they are running in a virtualized environment because the hypervisor tricks them into thinking that they have normal access to the underlying hardware when, in reality, that hardware is shared with other systems.

#

### Hypervisors

The primary responsibility of the hypervisor is enforcing **isolation** between virtual machines.

This means that the hypervisor must present each virtual machine with the illusion of a completely separate physical environment dedicated for use by that virtual machine.

From an operational perspective, isolation ensures that virtual machines do not interfere with each other's operations. 

From a security perspective, it means that virtual machines are not able to access or alter information or resources assigned to another virtual machine.

There are two primary types of hypervisors:

- **Type I hypervisors**, also known as **bare metal hypervisors**, operate directly on top of the underlying hardware.

The hypervisor then supports guest operating systems for each virtual machine.

This is the model most commonly used in datacenter virtualization because it is highly efficient.

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/97d9a1aa-4df6-4d4b-92a2-5b6f53f821e7)

- **Type II hypervisors** run as an application on top of an existing operating system

In this approach, the operating system supports the hypervisor and the hypervisor requests resources for each guest operating system from the host operating system.

In this approach, the operating system supports the hypervisor and the hypervisor requests resources for each guest operating system from the host operating system. 

This model is commonly used to provide virtualization environments on personal computers for developers, technologists, and others who have the need to run their own virtual machines. 

It is less efficient than bare-metal virtualization because the host operating system introduces a layer of inefficiency that consumes resources.

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/36b4686f-c859-4852-a7c8-b645c65e1adf)

## Cloud Infrastructure Components

IaaS computing environments provide organizations with access to a wide variety of computing resources, including compute capacity, storage, and networking. These resources are available in a flexible manner and typically may be used immediately upon request.

### Cloud Compute Resources

Computing capacity is one of the primary needs of organizations moving to the cloud.

As they seek to augment or replace the servers running in their own datacenters, they look to the cloud for virtualized servers and other means of providing compute capacity. 

All of these technologies benefit from the cloud's dynamic resource allocation, allowing administrators to add and remove resources (automatically or manually) as needs change.

#

### Virtualized Servers

Virtual machines are the basic building block of compute capacity in the cloud.

Organizations may provision servers running most common operating systems with the specific number of CPU cores, amount of RAM, and storage capacity that is necessary to meet business requirements.

The cost of a server instance normally accrues based upon an hourly rate and that rate varies based on the compute, memory, and storage resources consumed by the server.

Once you've provisioned a virtualized server, you may interact with it in the same manner as you would a server running in your own datacenter.

#

### Containers

Containers provide application-level virtualization.

Instead of creating complex virtual machines that require their own operating systems, containers package applications and allow them to be treated as units of virtualization that become portable across operating systems and hardware platforms.

Organizations implementing containerization run containerization platforms, such as Docker, that provide standardized interfaces to operating system resources. This interface remains consistent, regardless of the underlying operating system or hardware, and the consistency of the interface allows containers to shift between systems as needed.

Containerization platforms share many of the same security considerations as virtualization platforms. They must enforce isolation between containers to prevent operational and security issues that might occur if an application running in one container is able to accidentally or intentionally interact with resources assigned to another container.

#

### Cloud Storage Resources

Infrastructure providers also offer their customers storage resources, both storage that is coupled with their computing offerings and independent storage offerings for use in building out other cloud architectures. 

These storage offerings come in two major categories:

- **Block storage** allocates large volumes of storage for use by virtual server instance(s). These volumes are then formatted as virtual disks by the operating system on those server instances and used as they would a physical drive. AWS offers block storage through their Elastic Block Storage (EBS) service.

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/d1c5b601-3e7c-44c0-b714-3574b5f93b8e)


- **Object storage** provides customers with the ability to place files in buckets and treat each file as an independent entity that may be accessed over the web or through the provider's API. Object storage hides the storage details from the end user, who does not know or care about the underlying disks. The AWS Simple Storage Service (S3) is an example of object storage.

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/dc3e48cb-dd15-4999-8544-5ef0cc84ef9b)

Block and object storage incur costs in different ways.

Block storage is preallocated by the cloud provider, and you pay for the capacity that you allocated, regardless of whether you actually store data on that volume. If you allocate a 1 TB drive, you will pay for 1 TB of storage even if you are storing only 500 GB of data on the drive.

Object storage is not preallocated, and you pay for the storage that you use. 

Block storage is also significantly more expensive than object storage. As of this writing, block storage charges at major cloud providers were three to ten times higher than object storage charges.

As you work with cloud storage, be certain that you keep three key security considerations top-of-mind:

- **Set permissions properly**. Make sure that you pay careful attention to the access policies you place on storage. This is especially true for object storage, where a few wayward clicks can inadvertently publish a sensitive file on the web.

- **Consider high availability and durability options**. Cloud providers hide the implementation details from users, but that doesn't mean they are immune from hardware failures. Use the provider's replication capabilities or implement your own to accommodate availability and integrity requirements.

- **Use encryption to protect sensitive data**. You may either apply your own encryption to individual files stored in the cloud or use the full-disk encryption options offered by the provider.

## Cloud Networking

Cloud networking follows the same virtualization model as other cloud infrastructure resources. Cloud consumers are provided access to networking resources to connect their other infrastructure components and are able to provision bandwidth as needed to meet their needs.

Cloud networking supports the **software-defined networking** (SDN) movement by allowing engineers to interact with and modify cloud resources through their APIs. Similarly, they provide cybersecurity professionals with **software-defined visibility** (SDV) that offers insight into the traffic on their virtual networks.

### Security Groups

Security professionals use firewalls on their physical networks to limit the types of network traffic that are allowed to enter the organization's secured perimeter. 

Cloud service providers implement firewalls as well, but they do not provide customers with direct access to those firewalls, because doing so would violate the isolation principle by potentially allowing one customer to make changes to the firewall that would impact other customers

Instead, cloud service providers meet the need for firewalls through the use of **security groups** that define permissible network traffic. These security groups consist of a set of rules for network traffic that are substantially the same as a firewall ruleset.


![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/6c56e15a-2730-4261-8a55-7f5c83cfdce0)

Security groups function at the network layer of the OSI model, similar to a traditional firewall. Cloud service providers also offer web application firewall capabilities that operate at higher levels of the OSI model.

Security groups are normally considered a feature of a provider's virtual servers and, as such, do not incur additional costs.

#

### Virtual Private Cloud (VPC)

**Segmentation** is one of the core concepts of network security.

Segmentation allows network engineers to place systems of differing security levels and functions on different network subnets. Similarly grouped systems are able to communicate with each other while remaining isolated from systems on other network segments.

On a physical network, networking and security professionals use virtual LAN (VLAN) technology to achieve segmentation.

In cloud environments, **virtual private clouds** (VPCs) serve the same purpose.

Using VPCs, teams can group systems into subnets and designate those subnets as public or private, depending on whether access to them is permitted from the Internet.

Cloud providers also offer **VPC endpoints** that allow the connection of VPCs to each other using the cloud provider's secure network backbone.

Cloud **transit gateways** extend this model even further, allowing the direct interconnection of cloud VPCs with on-premises VLANs for hybrid cloud operations.

#

### DevOps and Cloud Automation

Traditional approaches to organizing and running technology teams focused on building silos of expertise centered on technology roles. In particular, software development and technology operations were often viewed as quite disconnected.

Developers worked on creating the software applications that the business desired and had their own processes for specifying requirements, designing interfaces, writing code, testing applications, and maintaining the code base. 

When they completed testing of a new version of an application, they then handed it off to the technology operations team, who managed the servers and other infrastructure supporting the application.

Separating the development and operations worlds provides technologists with a comfortable working environment where they have their tasks clearly defined and are surrounded by a community of their peers. 

It also, however, brings significant disadvantages, including the following:

- Isolating operations teams from the development process inhibits their understanding of business requirements.

- Isolating developers from operational considerations leads to designs that are wasteful in terms of processor, memory, and network consumption.

- Requiring clear hand-offs from development to operations reduces agility and flexibility by requiring a lengthy transition phase

- Increasing the overhead associated with transitions encourages combining many small fixes and enhancements into one major release, increasing the time to requirement satisfaction.

Recognizing the inherent disadvantages of separating development and operational teams, many organizations now embrace a DevOps approach to technology management.

This approach brings together development and operations teams in a unified process where they work together in an agile approach to software development.

The software testing and release process becomes highly automated and collaborative, enabling organizations to move from lengthy release management processes to a world where they might release dozens of updates on a daily basis.

**Infrastructure as code** (IaC) is one of the key enabling technologies behind the DevOps movement and is also a crucial advantage of cloud computing services integration.

IaC is the process of automating the provisioning, management, and deprovisioning of infrastructure services through scripted code rather than human intervention. IaC is one of the key features of all major IaaS environments, including AWS, Microsoft Azure, and Google Cloud Platform.

IaC takes many forms and may be either a feature offered by a cloud service provider or a functionality enabled by a third-party cloud management platform.

In most cases, the same actions available to operations teams through the cloud provider's web interface are also available for implementation in code.

AWS offers a service called CloudFormation that allows developers to specify their infrastructure requirements in several formats, including JavaScript Object Notation (JSON) and Yet Another Markup Language (YAML).

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/9cf93153-45c7-4a86-9a86-17ee1b449050)

Infrastructure as code approaches depend on the use of **application programming interfaces** (APIs) offered by cloud providers. 

Developers can use cloud provider APIs to programmatically provision, configure, modify, and deprovision cloud resources. API integration is particularly helpful in cloud environments that embrace microservices, cloud service offerings that provide very granular functions to other services, often through a function-as-aservice model. These microservices are designed to communicate with each other in response to events that take place in the environment.

## Cloud Security Issues

### Availability

One of the major advantages of the cloud is that cloud providers may operate in many different geographic regions, and they often provide simple mechanisms for backing up data across those regions and/or operating in a high availability mode across diverse zones.

For example, a company operating a web server cluster in the cloud may choose to place servers on each major continent to serve customers in those regions and also to provide geographic diversity in the event of a large-scale issue in a particular geographic region.

#

### Data Sovereignty

The distributed nature of cloud computing involves the use of geographically distant facilities to achieve high availability and to place content in close proximity to users. 

This may mean that a customer's data is stored and processed in datacenters across many different countries, either with or without explicit notification.

Unless customers understand how their data is stored, this could introduce legal concerns.

**Data sovereignty** is a principle that states that data is subject to the legal restrictions of any jurisdiction where it is collected, stored, or processed.

Under this principle, a customer might wind up subject to the legal requirements of a jurisdiction where they have no involvement other than the fact that one of their cloud providers operates a data center within that jurisdiction.

Security professionals responsible for managing cloud services should be certain that they understand how their data is stored, processed, and transmitted across jurisdictions.

They may also choose to encrypt data using keys that remain outside the providers control to ensure that they maintain sole control over their data.

Some cloud providers offer explicit control over the use of resources in specific regions.

#

### Virtualization Security

**Virtual machine escape** vulnerabilities are the most serious issue that can exist in a virtualized environment, particularly when a virtual host runs systems of differing security levels.

In an escape attack, the attacker has access to a single virtual host and then manages to leverage that access to intrude upon the resources assigned to a different virtual machine.

The hypervisor is supposed to prevent this type of access by restricting a virtual machine's access to only those resources assigned to that machine.

Escape attacks allow a process running on the virtual machine to “escape” those hypervisor restrictions.

**Virtual machine sprawl** occurs when IaaS users create virtual service instances and then forget about them or abandon them, leaving them to accrue costs and accumulate security issues over time. Organizations should maintain instance awareness to avoid VM sprawl issues.

#

### Application Security

Cloud applications suffer from many of the same security concerns as any other application.

Cloud applications depend heavily upon the use of application programming interfaces (APIs) to provide service integration and interoperability.

Security analysts responsible for API-based applications should implement API inspection technology that scrutinizes API requests for security issues. These capabilities are often found in web application firewall solutions.

**Secure web gateways** (SWG) also provide a layer of application security for cloud-dependent organizations.

SWGs monitor web requests made by internal users and evaluate them against the organization's security policy, blocking requests that run afoul of these requirements.

SWGs are commonly used to block access to potentially malicious content but may also be used to enforce content filtering restrictions.

#

### Governance and Auditing

Technology governance efforts guide the work of IT organizations and ensure that they are consistent with organizational strategy and policy. 

These efforts also should guide the establishment and maintenance of cloud vendor relationships. Cloud governance efforts assist with the following:

- Vetting vendors being considered for cloud partnerships

- Managing vendor relationships and monitoring for early warning signs of vendor stability issues

- Overseeing an organization's portfolio of cloud activities 

**Auditability** is an important component of cloud governance. 

Cloud computing contracts should include language guaranteeing the right of the customer to audit cloud service providers. 

They may choose to perform these audits themselves or engage a third party to perform an independent audit. 

The use of auditing is essential to providing customers with the assurance that the provider is operating in a secure manner and meeting its contractual data protection obligations.

## Cloud Security Controls

Cloud providers and third-party organizations offer a variety of solutions that help organizations achieve their security objectives in the cloud.

Organizations may choose to adopt cloud-native controls offered by their cloud service provider, third-party solutions, or a combination of the two.

Controls offered by cloud service providers have the advantage of direct integration with the provider's offerings, often making them cost-effective and user-friendly.

Third-party solutions are often more costly, but they bring the advantage of integrating with a variety of cloud providers, facilitating the management of multicloud environments.

### Cloud Access Security Brokers

Most organizations use a variety of cloud service providers for different purposes. It's not unusual to find that a large organization purchases cloud services from dozens, or even hundreds, of different providers. This is especially true when organizations use highly
specialized SaaS products. 

Managing security policies consistently across these services poses a major challenge for cybersecurity analysts.

**Cloud access security brokers** (CASBs) are software tools that serve as intermediaries between cloud service users and cloud service providers.

This positioning allows them to monitor user activity and enforce policy requirements. CASBs operate using two different approaches:

- Inline CASB solutions physically or logically reside in the connection path between the user and the service. They may do this through a hardware appliance or an endpoint agent that routes requests through the CASB. This approach requires configuration of the network and/or endpoint devices.

It provides the advantage of seeing requests before they are sent to the cloud service, allowing the CASB to block requests that violate policy.

- API-based CASB solutions do not interact directly with the user but rather interact directly with the cloud provider through the provider's API. This approach provides direct access to the cloud service and does not require any user device configuration.

However, it also does not allow the CASB to block requests that violate policy. API-based CASBs are limited to monitoring user activity and reporting on or correcting policy violations after the fact.

#

### Resource Policies

Cloud providers offer resource policies that customers may use to limit the actions that users of their accounts may take.

Implementing resource policies is a good security practice to limit the damage caused by an accidental command, a compromised account, or a malicious insider.

Here is an example of a service control policy written in JSON that restricts access to cloud resources:

    {
         "Statement": [
             {
                 "Sid": "DenyAllOutsideUSEastEUWest1",
                 "Effect": "Deny",
                 "NotAction": [
                     "iam:*",
                     "organizations:*",
                     "route53:*",
                     "budgets:*",
                     "waf:*",
                     "cloudfront:*",
                     "globalaccelerator:*",
                     "importexport:*",
                     "support:*"
                 ],
                 "Resource": "*",
                 "Condition": {
                     "StringNotEquals": {
                         "aws:RequestedRegion": [
                              "us-east-1",
                              "us-east-2",
                              "eu-west-1"
                         ]
                     }
                 }
            },
            {
                 "Condition": {
                     "ForAnyValue:StringNotLike": {
                         "ec2:InstanceType": [
                             "*.micro",
                             "*.small",
                             "*.nano"
                         ]
                     }
                  },
                  "Action": [
                      "ec2:RunInstances",
                      "ec2:ModifyInstanceAttribute"
                  ],
                  "Resource": "arn:aws:ec2:*:*:instance/*",
                  "Effect": "Deny",
                  "Sid": "DenyLargeInstances"
               }
          ]
    }

This policy prohibits affected users from using any resources outside of the US-East and EU-West regions and prohibits them from using some services (such as Identity and Access Management) in any region. It also limits users to only launching smaller server instances in an effort to control costs.

#

### Secrets Management

**Hardware security modules** (HSMs) are special-purpose computing devices that manage encryption keys and also perform cryptographic operations in a highly efficient manner.

HSMs are expensive to purchase and operate, but they provide an extremely high level of security when configured properly.

One of their core benefits is that they can create and manage encryption keys without exposing them to a single human being, dramatically reducing the likelihood that they will be compromised.

Cloud service providers often use HSMs internally for the management of their own encryption keys and also offer HSM services to their customers as a secure method for managing customer keys without exposing them to the provider.
