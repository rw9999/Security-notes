# Network Security

Networks are at the core of our organizations, transferring data and supporting the services that we rely on to conduct business. That makes them a key target for attackers and a crucial layer in defensive architecture and design.

### Designing Secure Networks

As a security professional, you must understand and be able to implement key elements of design and architecture found in enterprise networks in order to properly secure them.

Security designs in most environments rely on the concept of **defense in depth**.

In other words, they are built around multiple controls design to ensure that a failure in a single control—or even multiple controls—is unlikely to cause a security breach.

With defense in depth in mind, it helps to understand that networks are also built in layers.

The Open Systems Interconnection (OSI) model is used to conceptually describe how devices and software operate together through networks. 

Beyond the conceptual level, designers will create security zones using devices that separate networks at trust boundaries and will deploy protections appropriate to both the threats and security requirements of each security zone.

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/fcf0b49e-18bd-49cc-ad44-bcef2c030dfb)

The OSI model is made up of seven layers, typically divided into two groups: the host layers and the media layers.

Layers 1–3, the Physical, Data Link, and Network layers, are considered media layers and are used to transmit the bits that make up network traffic, to transmit frames or logical groups of bits, and to make networks of systems or devices work properly using addressing, routing, and traffic control schemes.

Layers 4–7, the host layers, ensure that data transmission is reliable, that sessions can be managed, that encryption is handled and that translation of data from the application to the network and back works, and that APIs and other high-level tools work.

As you think about network design, remember that this is a logical model that can help you think about where network devices and security tools interact within the layers. You should also consider the layer at which a protocol or technology operates and what that means for what it can see and impact.

#

### Network Segmentation

Network segmentation divides a network up into logical or physical groupings that are frequently based on trust boundaries, functional requirements, or other reasons that help an organization apply controls or assist with functionality.

A number of technologies and concepts are used for segmentation, but one of the most common is the use of **virtual local area networks** (VLANs).

VLAN sets up a broadcast domain that is segmented at the Data Link layer. Switches or other devices are used to create a VLAN using VLAN tags, allowing different ports across multiple network devices like switches to all be part of the same VLAN without other systems plugged into those switches being in the same broadcast domain.

A **broadcast domain** is a segment of a network in which all the devices or systems can reach one another via packets sent as a broadcast at the Data Link layer.

Broadcasts are sent to all machines on a network, so limiting the broadcast domain makes networks less noisy by limiting the number of devices that are able to broadcast to one another. Broadcasts don't cross boundaries between networks—if your computer sends a broadcast, only those systems in the same broadcast domain will see it.

A number of network design concepts describe specific implementations of network segmentation:

- **DMZ**s, or demilitarized zones, are network zones that contain systems that are exposed to less trusted areas. DMZs are commonly used to contain web servers or other Internet-facing devices but can also describe internal purposes where trust levels are different.

- **Intranets** are internal networks set up to provide information to employees or other members of an organization, and they are typically protected from external access.

- **Extranets** are networks that are set up for external access, typically by partners or customers rather than the public at large.

Although many network designs used to presume that threats would come from outside of the security boundaries used to define network segments, the core concept of **zero-trust** networks is that nobody is trusted, regardless of whether they are an internal or an external person or system.

Therefore, zero-trust networks should include security between systems as well as at security boundaries.

You may hear the term “east-west” traffic used to describe traffic flow in a datacenter. It helps to picture a network diagram with systems side by side in a datacenter and network connections between zones or groupings at the top and bottom. Traffic between systems in the same security zone move left and right between them—thus “east and west” as you would see on a map.

This terminology is used to describe intersystem communications, and monitoring east-west traffic can be challenging.

Modern zero-trust networks don't assume that system-to-system traffic will be trusted or harmless, and designing security solutions that can handle east-west traffic is an important part of security within network segments.

#

### Network Access Control

Network segmentation helps divide networks into logical security zones, but protecting networks from unauthorized access is also important.

That's where **network access control** (NAC), sometimes called network admissions control, comes in. NAC technologies focus on determining whether a system or device should be allowed to connect to a network.

If it passes the requirements set for admission, NAC places it into an appropriate zone.

To accomplish this task, NAC can use a software agent that is installed on the computer to perform security checks. Or the process may be agentless and run from a browser or by another means without installing software locally.

Capabilities vary, and software agents typically have a greater ability to determine the security state of a machine by validating patch levels, security settings, antivirus versions, and other settings and details before admitting a system to the network. 

Some NAC solutions also track user behavior, allowing for systems to be removed from the network if they engage in suspect behaviors.

Since NAC has the ability to validate security status for systems, it can be an effective policy enforcement tool.

If a system does not meet security objectives, or if it has an issue, the system can be placed into a quarantine network. There the system can be remediated and rechecked, or it can simply be prohibited from connecting to the network.

NAC checks can occur before a device is allowed on the network (preadmission) or after it has connected (postadmission).

The combination of agent or agentless solutions and pre- or postadmission designs is driven by security objectives and the technical capabilities of an organization's selected tool.

Agent-based NAC requires installation and thus adds complexity and maintenance, but it provides greater insight and control.

Agentless installations are lightweight and easier to handle for users whose machines may not be centrally managed or who have devices that may not support the NAC agent. However, agentless installations provide less detail.

Preadmission NAC decisions keep potentially dangerous systems off a network; postadmission decisions can help with response and prevent failed NAC access attempts from stopping business.

#

### Port Security and Port-Level Protections

A number of protections focus on ensuring that the network itself is not endangered by traffic that is sent on it.

**Port security** is a capability that allows you to limit the number of MAC addresses that can be used on a single port.

This prevents a number of possible problems, including MAC (hardware) address spoofing, content-addressable memory (CAM) table overflows, and in some cases, plugging in additional network devices to extend the network.

Although port security implementations vary, most port security capabilities allow you to either dynamically lock the port by setting a maximum number of MAC addresses or statically lock the port to allow only specific MAC addresses. Although this type of MAC filtering is less nuanced and provides less information than NAC does, it remains useful.

Port security helps protect the CAM table, which maps MAC addresses to IP addresses, allowing a switch to send traffic to the correct port. If the CAM table doesn't have an entry, the switch will attempt to determine what port the address is on, broadcasting traffic to all ports if necessary. That means attackers who can fill a CAM table can make switches fail over to broadcasting traffic, making otherwise inaccessible traffic visible on their local port.

Since spoofing MAC addresses is relatively easy, port security shouldn't be relied on to prevent untrusted systems from connecting.

Despite this, configuring port security can help prevent attackers from easily connecting to a network if NAC is not available or not in use. It can also prevent CAM table overflow attacks that might otherwise be possible.

In addition to port security, protocol-level protections are an important security capability that switches and other network devices provide. These include the following:

- **Loop prevention** focuses on detecting loops and then disabling ports to prevent the loops from causing issues. Spanning Tree Protocol (STP) using bridge protocol data units, as well as anti-loop implementations like Cisco's loopback detection capability, send frames with a switch identifier that the switch then monitors to prevent loops.

Although a loop can be as simple as a cable with both ends plugged into the same switch, loops can also result from cables plugged into different switches, firewalls that are plugged in backward, devices with several network cards plugged into different portions of the same network, and other misconfigurations found in a network.

- **Broadcast storm prevention**, sometimes called storm control, prevents broadcast packets from being amplified as they traverse a network.

Preventing broadcast storms relies on several features such as offering loop protection on ports that will be connected to user devices, enabling STP on switches to make sure that loops are detected and disabled, and rate-limiting broadcast traffic.

A broadcast storm occurs when a loop in a network causes traffic amplification to occur as switches attempt to figure out where traffic should be sent.


![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/652e39b4-d0e2-4c8c-a63c-cacf4051c75b)

The following graphic shows a loop with three switches, A, B, and C. Since traffic from host 1 could be coming through either switch B or switch C, when a broadcast is sent out to figure out where host 1 is, responses will be sent from both. As this repeats, amplification will occur, causing a storm.

- **Bridge Protocol Data Unit** (BPDU) guard protects STP by preventing ports that should not send BPDU messages from sending them.

It is typically applied to switch ports where user devices and servers will be plugged in. Ports where switches will be connected will not have BPDU turned on, because they may need to send BPDU messages that provide information about ports, addresses, priorities, and costs as part of the underlying management and control of the network.

- **Dynamic Host Configuration Protocol (DHCP) snooping** focuses on preventing rogue DHCP servers from handing out IP addresses to clients in a managed network.

DHCP snooping drops messages from any DHCP server that is not on a list of trusted servers, but it can also be configured with additional options such as the ability to block DHCP messages where the source MAC and the hardware MAC of a network card do not match.

A final security option is to drop messages releasing or declining a DHCP offer if the release or decline does not come from the same port that the request came from, preventing attackers from causing a DHCP offer or renewal to fail.

These protections may seem like obvious choices, but network administrators need to balance the administrative cost and time to implement them for each port in a network, as well as the potential for unexpected impacts if security settings affect services.

Implementation choices must take into account whether attacks are likely, how controlled the network segment or access to network ports is, and how difficult it will be to manage all the network ports that must be configured and maintained.

Central network management tools as well as dynamic and rules-based management capabilities can reduce the time needed for maintenance and configuration, but effort will still be required for initial setup and ongoing support.

#

### Port Spanning/Port Mirroring

A final port-level tool that security and network professionals rely on is the ability to use a **switch port analyzer (SPAN)**, or **port mirror**.

A port mirror sends a copy of all the traffic sent to one switch port to another switch port for monitoring.

A SPAN can do the same thing but can also combine traffic from multiple ports to a single port for analysis.

Both are very useful for troubleshooting and monitoring, including providing data for devices like intrusion detection systems that need to observe network traffic to identify attacks.

Taps, which are a hardware or software means of copying network traffic.

You can think of a tap like a network splitter that sends a copy of the traffic passing through a link to a second location without interfering with it.

Taps are thus useful for acquiring a complete copy of all data traveling over a network link, and they do not cause switch or router overhead as a port mirror or SPAN can.

#

### Virtual Private Network

A virtual private network (VPN) is a way to create a virtual network link across a public network that allows the endpoints to act as though they are on the same network.

Although it is easy to think about VPNs as an encrypted tunnel, encryption is not a requirement of a VPN tunnel.

There are two major VPN technologies in use in modern networks.

The first, IPSec VPNs, operate at layer 3, require a client, and can operate in either tunnel or transport mode.

In tunnel mode, entire packets of data sent to the other end of the VPN connection are protected.

In transport mode, the IP header is not protected but the IP payload is.

IPSec VPNs are often used for site-to-site VPNs, and for VPNs that need to transport more than just web and application traffic.

IPSec can be used with multiple protocols depending on needs and supported options.

Layer 2 Tunneling Protocol (L2TP) VPNs do not provide encryption on their own and instead simply provide tunnels. They are often combined with IPSec to provide that security.

The second common VPN technology is SSL VPNs (although they actually use TLS in current implementations—the common substitution of SSL for TLS continues here).

SSL VPNs can either use a portal-based approach (typically using HTML5), where users access it via a web page and then access services through that connection, or they can offer a tunnel mode like IPSec VPNs.

SSL VPNs are popular because they can be used without a client installed or specific endpoint configuration that is normally required for IPSec VPNs.

SSL VPNs also provide the ability to segment application access, allowing them to be more granular without additional complex configuration to create security segments using different VPN names or hosts, as most IPSec VPN tools would require.

In addition to the underlying technology that is used by VPNs, there are implementation decisions that are driven by how a VPN will be used and what traffic it needs to carry.

The first decision point for many VPN implementations is whether the VPN will be used for remote access or if it will be a **site-to-site VPN**.

Remote-access VPNs are commonly used for traveling staff and other remote workers, and site-to-site VPNs are used to create a secure network channel between two or more sites.

Since site-to-site VPNs are typically used to extend an organization's network, they are frequently always on VPNs, meaning that they are connected and available all of the time, and that if they experience a failure they will automatically attempt to reconnect.

Remote-access VPNs are most frequently used in an as-needed mode, with remote workers turning on the VPN when they need to connect to specific resources or systems, or when they need a trusted network connection.

The second important decision for VPN implementations is whether they will be a **split-tunnel VPN** or a **full-tunnel VPN**.

A full-tunnel VPN sends all network traffic through the VPN tunnel, keeping it secure as it goes to the remote trusted network.

A split-tunnel VPN only sends traffic intended for systems on the remote trusted network through the VPN tunnel.

Split tunnels offer the advantage of using less bandwidth for the hosting site, since network traffic that is not intended for that network will be sent out through whatever Internet service provider the VPN user is connected to. However, that means the traffic is not protected by the VPN and cannot be monitored.

A full-tunnel VPN is a great way to ensure that traffic sent through an untrusted network, such as those found at a coffee shop, hotel, or other location, remains secure. If the network you are sending traffic through cannot be trusted, a split-tunnel VPN may expose more information about your network traffic than you want it to.

#

### Network Appliances and Security Tools

There many different types of network appliances that you should consider as part of your network design. Special-purpose hardware devices, virtual machine and cloud-based software appliances, and hybrid models in both open source and proprietary commercial versions are used by organizations.

Hardware appliances can offer the advantage of being purpose-built, allowing very high-speed traffic handling capabilities or other capabilities.

Software and virtual machine appliances can be easily deployed and can be scaled based on needs, whereas cloud appliances can be dynamically created, scaled, and used as needed.

Regardless of the underlying system, appliances offer vendors a way to offer an integrated system or device that can be deployed and used in known ways, providing a more controlled experience than a software package or service deployed on a customer-owned server.

#

### Hardware, Software, and Vendor Choices

When you choose a network appliance, you must consider more than just the functionality.

If you're deploying a device, you also need to determine whether you need or want a hardware appliance or a software appliance that runs on an existing operating system, a virtual machine, or a cloud-based service or appliance. 

Drivers for that decision include the environment where you're deploying it, the capabilities you need, what your existing infrastructure is, upgradability, support, and the relative cost of the options. So, deciding that you need a DNS appliance isn't as simple as picking one off a vendor website.

You should also consider if open source or proprietary commercial options are the right fit for your organization. 

Open source options may be less expensive or faster to acquire in organizations with procurement and licensing restrictions. C

ommercial offerings may offer better support, additional proprietary features, certifications and training, or other desirable options as well. When you select a network appliance, make sure you take into account how you will deploy it— hardware, software, virtual, or cloud—and whether you want an open source or proprietary solution.

#

### Jump Servers and Jump Boxes

Administrators and other staff need ways to securely operate in security zones with different security levels.

**Jump servers**, sometimes called jump boxes, are a common solution.

A jump server is a secured and monitored system used to provide that access.

It is typically configured with the tools required for administrative work and is frequently accessed with SSH, RDP, or other remote desktop methods. Jump boxes should be configured to create and maintain a secure audit trail, with copies maintained in a separate environment to allow for incident and issue investigations.

#

### Load Balancing

Load balancers are used to distribute traffic to multiple systems, provide redundancy, and allow for ease of upgrades and patching.

They are commonly used for web service infrastructures, but other types of load balancers can also be found in use throughout many networks.

Load balancers typically present a **virtual IP (VIP)**, which clients send service requests to on a service port.

The load balancer then distributes those requests to servers in a pool or group.

Two major modes of operation are common for load balancers:

- **Active/active** load balancer designs distribute the load among multiple systems that are online and in use at the same time.

- **Active/passive** load balancer designs bring backup or secondary systems online when an active system is removed or fails to respond properly to a health check.

This type of environment is more likely to be found as part of disaster recovery or business continuity environments, and it may offer less capability from the passive system to ensure some functionality remains.

Load balancers rely on a variety of **scheduling** or load-balancing algorithms to choose where traffic is sent to. Here are a few of the most common options:

- **Round-robin** sends each request to servers by working through a list, with each server receiving traffic in turn.

- **Least connection** sends traffic to the server with the fewest number of active connections.

- **Agent-based** adaptive balancing monitors the load and other factors that impact a server's ability to respond and updates the load balancer's traffic distribution based on the agent's reports.

- **Source IP hashing** uses a hash of the source IP to assign traffic to servers. This is essentially a randomization algorithm using client-driven input.

In addition to these, weighted algorithms take into account a weighting or score. Weighted algorithms include the following:

- **Weighted least** connection uses a least connection algorithm combined with a predetermined weight value for each server.

- **Fixed weighted** relies on a preassigned weight for each server, often based on capability or capacity.

- **Weighted response time** combines the server's current response time with a weight value to assign it traffic.

Finally, load balancers may need to establish persistent sessions.

**Persistence** means that a client and a server continue to communicate throughout the duration of a session.

This helps servers provide a smoother experience, with consistent information maintained about the client, rather than requiring that the entire load-balanced pool be made aware of the client's session.

Of course, sticky sessions also mean that load will remain on the server that the session started with, which requires caution in case too many longrunning sessions run on a single server and a load-balancing algorithm is in use that doesn't watch this.

Factors such as the use of persistence, different server capabilities, or the use of scalable architectures can all drive choices for scheduling algorithms. Tracking server utilization by a method such as an agentbased adaptive balancing algorithm can be attractive but requires more infrastructure and overhead than a simple round-robin algorithm.

#

### Proxy Servers

Proxy servers accept and forward requests, centralizing the requests and allowing actions to be taken on the requests and responses.

They can filter or modify traffic and cache data, and since they centralize requests, they can be used to support access restrictions by IP address or similar requirements. 

There are two types of proxy servers:

- **Forward proxies** are placed between clients and servers, and they accept requests from clients and send them forward to servers. Since forward proxies conceal the original client, they can anonymize traffic or provide access to resources that might be blocked by IP address or geographic location. They are also frequently used to allow access to resources such as those that libraries subscribe to

- **Reverse proxies** are placed between servers and clients, and they are used to help with load balancing and caching of content. Clients can thus query a single system but have traffic load spread to multiple systems or sites.

#

### Network Address Translation Gateways

Network address translation (NAT) allows a pool of addresses to be translated to one or more external addresses.

Typically, NAT is used to allow many private IP addresses to use a single public IP address to access the Internet.

A NAT gateway is a device that provides the network address translation and tracks which packets should be sent to each device as they transit through it.

**NAT gateways** are a common network tool—in fact, they're in many homes in the form of the Internet router that provides a pool of private IP addresses and uses NAT to allow a single external public IP to serve many devices behind the router.

NAT gateways are frequently used for cloud infrastructure as a service environment where private addresses are used for internal networking.

A NAT gateway service can be used to allow systems to connect to the Internet. Since NAT gateways do not allow external systems to initiate inbound connections unless rules are specifically put in place to allow it, they can allow secure outbound access without creating additional risks to the systems behind the gateway.

NAT isn't a firewall, but it has some firewall-like properties. Since a NAT gateway doesn't allow inbound access by default, it can act like a firewall with a default deny rule for inbound access.

#

### Content/URL Filters

**Content filters** are devices or software that allow or block traffic based on content rules.

These can be as simple as blocking specific URLs, domains, or hosts, or they may be complex, with pattern matching, IP reputation, and other elements built into the filtering rules.

Like other technologies, they can be configured with allow or deny lists as well as rules that operate on the content or traffic they filter.

Proxies frequently have content filtering capabilities, but content filtering and URL filtering can also be part of other network devices and appliances such as firewalls, network security appliances, IPSs, and others.

#

### Data Protection

Ensuring that data isn't extracted or inadvertently sent from a network is where a data loss prevention (DLP) solution comes into play.

DLP solutions frequently pair agents on systems with filtering capabilities at the network border, email servers, and other likely exfiltration points.

When an organization has concerns about sensitive, proprietary, or other data being lost or exposed, a DLP solution is a common option.

DLP systems can use pattern-matching capabilities or can rely on tagging, including the use of metadata to identify data that should be flagged.

Actions taken by DLP systems can include blocking traffic, sending notifications, or forcing identified data to be encrypted or otherwise securely transferred rather than being sent by an unencrypted or unsecure mode.

#

### Intrusion Detection and Intrusion Prevention Systems

Network-based intrusion detection systems (IDSs) and intrusion prevention systems (IPSs) are used to detect threats and, in the case of IPS, to block them.

They rely on one or more of three different detection methods to identify unwanted and potentially malicious traffic:

- **Signature-based** detections rely on a known hash or signature matching to detect a threat.

- **Heuristic**, or **behavior-based**, detections look for specific patterns or sets of actions that match threat behaviors.

- **Anomaly-based** detection establishes a baseline for an organization or network and then flags when out-of-theordinary behavior occurs.

Although an IPS needs to be deployed in line where it can interact with the flow of traffic to stop threats, both IDSs and IPSs can be deployed in a passive mode as well.

Passive modes can detect threats but cannot take action—which means that an IPS placed in a passive deployment is effectively an IDS.

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/3a7ed78e-e798-4fa2-bd36-319b9cf33c22)

Like many of the other appliances covered in this chapter, IDS and IPS deployments can be hardware appliances, software-based, virtual machines, or cloud instances.

Key decision points for selecting them include their throughput, detection methods, availability of detection rules and updates, the ability to create custom filters and detections, and their detection rates for threats in testing.

#

### Hardware Security Modules

Hardware security modules (HSMs) can be deployed as network appliances, and they are used to generate, securely store, and manage cryptographic keys.

They can also handle cryptographic processing, allowing servers to offload CPU-intensive tasks to dedicated cryptographic hardware. 

In addition to being available as hardware appliances, HSMs are widely available as part of cloud infrastructure as service offerings in both dedicated and virtual options.

#

### Data Collection

Many components of datacenters rely on network appliances to acquire data.

Hardware and software appliances can act as sensors, gathering data about the physical environment, network traffic, or other information that centralized services and management need to ensure the continued operations of the organization.

Since the sheer amount of data acquired from sensors can be enormous, a tiered design using data collection collectors and aggregators that centralize subsets of data is also common.

Collectors and aggregators can also provide preprocessing, de-duplication, or other information management services to ensure that the central management and analysis servers to which they provide data are not overwhelmed.

#

### Firewalls

Firewalls are one of the most common components in network design. 

They are deployed as network appliances or on individual devices, and many systems implement a simple firewall or firewalllike capabilities.

There are two basic types of firewalls included in the Security+ exam outline:

- **Stateless firewalls** (sometimes called packet filters) filter every packet based on data such as the source and destination IP and port, the protocol, and other information that can be gleaned from the packet's headers. They are the most basic type of firewall.

- **Stateful firewalls** (sometimes called dynamic packet filters) pay attention to the state of traffic between systems. They can make a decision about a conversation and allow it to continue once it has been approved rather than reviewing every packet. They track this information in a state table, and use the information they gather to allow them to see entire traffic flows instead of each packet, providing them with more context to make security decisions.

**Next-generation firewall(NGFW)** devices are far more than simple firewalls. In fact, they might be more accurately described as all-in-one network security devices in many cases. The general term has been used to describe network security devices that include a range of capabilities such as deep packet inspection, IDS/IPS functionality, antivirus and antimalware, and other functions.

Finally, **web application firewalls** (WAFs) are security devices that are designed to intercept, analyze, and apply rules to web traffic, including tools such as database queries, APIs, and other web application tools.

In many ways, a WAF is easier to understand if you think of it as a firewall combined with an intrusion prevention system.

They provide deeper inspection of the traffic sent to web servers looking for attacks and attack patterns, and then apply rules based on what they see. This allows them to block attacks in real time, or even modify traffic sent to web servers to remote potentially dangerous elements in a query or request.

#

### Unified Threat Management

Unified threat management (UTM) devices frequently include firewall, IDS/IPS, antimalware, URL and email filtering and security, data loss prevention, VPN, and security monitoring and analytics capabilities.

The line between UTM and NGFW devices can be confusing, and the market continues to narrow the gaps between devices as each side offers additional features

UTM appliances are frequently deployed at network boundaries, particularly for an entire organization or division.

Since they have a wide range of security functionality, they can replace several security devices while providing a single interface to manage and monitor them.

They also typically provide a management capability that can handle multiple UTM devices at once, allowing organizations with several sites or divisions to deploy UTM appliances to protect each area while still managing and monitoring them centrally.

## Network Security, Services, and Management

Managing your network in a secure way and using the security tools and capabilities built into your network devices is another key element in designing a secure network.

Whether it is prioritizing traffic via QoS, providing route security, or implementing secure protocols on top of your existing network fabric, network devices and systems provide a multitude of options.

### Out-of-Band Management

Access to the management interface for a network appliance or device needs to be protected so that attackers can't seize control of it and to ensure that administrators can reliably gain access when they need to.

Whenever possible, network designs must include a way to do secure out-of-band management.

A separate means of accessing the administrative interface should exist.

Since most devices are now managed through a network connection, modern implementations use a separate management VLAN or an entirely separate physical network for administration.

Physical access to administrative interfaces is another option for out-of-band management, but in most cases physical access is reserved for emergencies because traveling to the network device to plug into it and manage it via USB, serial, or other interfaces is time consuming and far less useful for administrators than a network-based management plane.

#

### Access Control Lists

The first thing that may come to mind when you think of access control is firewalls with firewall rules, but many network devices and appliances support some form of access control lists (ACLs) too.

ACLs are a set of rules used to filter or control network traffic.

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/0fb114de-ca99-4baa-aaf2-6e4c1a04b262)

Cloud services also provide network ACLs. VPCs and other services provide firewall-like rules that can restrict or allow traffic between systems and services. Like firewall rules, these can typically be grouped, tagged, and managed using security groups or other methods.

#

### Quality of Service

The ability to ensure that an application, service, or network traffic is prioritized and able to meet its designed purposes is handled by quality of service (QoS) capabilities.

QoS protocols like 802.11E for Wi-Fi networks and 802.1Q (or Dot1Q) for wired networks define how traffic can be tagged and prioritized, and thus how quality of service can be managed.

Quality of service considers a variety of important elements of network performance: the bandwidth available and in use, the latency of traffic, how much the latency varies (jitter), and the rate at which errors are occurring.

These help provide QoS metrics, allowing traffic to be prioritized and managed according to QoS rules that apply based on applications, users, ports, protocols, or IP addresses.

QoS offers support for bandwidth and traffic management as well as queuing to handle packets that are lower priority and need to wait. They can also provide either proportional or guaranteed bandwidth to prioritized traffic.

