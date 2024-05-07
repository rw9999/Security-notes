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

