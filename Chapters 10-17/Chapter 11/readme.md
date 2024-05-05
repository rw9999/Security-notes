# Endpoint Security

Protecting endpoints in your organization is a significant portion of the daily tasks for many security professionals. For most organizations, endpoints significantly outnumber the servers and network devices, and since end users control or use them, they also have a wide variety of threats that they face that a server is unlikely to deal with.

## Protecting Endpoints

As a security professional, you'll be asked to recommend, implement, manage, or assess security solutions intended to protect desktops, mobile devices, servers, and a variety of other systems found in organizations. 

These devices are often called endpoints, meaning they're an end point of a network, whether that is a wired or wireless network.

With such a broad range of potential endpoints, the menu of security options is also very broad.

As a security practitioner, you need to know what options exist, where and how they are commonly deployed, and what considerations you need to take into account.

### Preserving Boot Integrity

Keeping an endpoint secure while it is running starts as it boots up. 

If untrusted or malicious components are inserted into the boot process, the system cannot be trusted. Security practitioners in high-security environments need a means of ensuring that the entire boot process is provably secure.

Fortunately, modern Unified Extensible Firmware Interface (UEFI) firmware (the replacement for the traditional Basic Input/Output System [BIOS]) can leverage two different techniques to ensure that the system is secure.

**Secure boot** ensures that the system boots using only software that the original equipment manufacturer (OEM) trusts.

To perform a secure boot operation, the system must have a signature database listing the secure signatures of trusted software and firmware for the boot process.

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/bdd4a075-009e-4a75-bc13-83d2901e2057)

The second security feature intended to help prevent boot-level malware is **measured boot**.

These boot processes measure each component, starting with the firmware and ending with the boot start drivers.

Measured boot does not validate against a known good list of signatures before booting; instead, it relies on the UEFI firmware to hash the firmware, bootloader, drivers, and anything else that is part of the boot process.

The data gathered is stored in the Trusted Platform Module (TPM), and the logs can be validated remotely to let security administrators know the boot state of the system. 

This boot attestation process allows comparison against known good states, and administrators can take action if the measured boot shows a difference from the accepted or secure known state. 

This process allows the remote server to make decisions about the state of the system based on the information it provides, allowing access control and quarantine options.

In both cases, boot integrity begins with the hardware root of trust.

The hardware root of trust for a system contains the cryptographic keys that secure the boot process.

This means that the system or device inherently trusts the hardware root of trust, and that it needs to be secure.

One common implementation of a hardware root of trust is the TPM chip built into many computers.

TPM chips are frequently used to provide built-in encryption, and they provide three major functions:

- Remote attestation, allowing hardware and software configurations to be verified

- Binding, which encrypts data

- Sealing, which encrypts data and sets requirements for the state of the TPM chip before decryption

TPM chips are one common solution; others include serial numbers that cannot be modified or cloned, and physically unclonable functions (PUFs), which are unique to the specific hardware device that provide a unique identifier or digital fingerprint for the device.

A physically unclonable function is based on the unique features of a microprocessor that are created when it is manufactured and is not intentionally created or replicated.

A related technology is hardware security modules (HSMs).

Hardware security modules are typically external devices or plug-in cards used to create, store, and manage digital keys for cryptographic functions and authentication, as well as to offload cryptographic processing. HSMs are often used in high-security environments and are normally certified to meet standards like Federal Information Processing Standards (FIPS) 140 or Common Criteria standards.

## Endpoint Security Tools

Once a system is running, ensuring that the system itself is secure is a complex task. Many types of security tools are available for endpoint systems, and the continuously evolving market for solutions means that traditional tool categories are often blurry.

### Antivirus and Antimalware

One of the most common security tools is antivirus and antimalware software. Although more advanced antidetection, obfuscation, and other defensive tools are always appearing in new malware packages, using antimalware packages in enterprise environments remains a useful defensive layer in many situations.

Tools like these work to detect malicious software and applications through a variety of means. Here are the most common methods:

- **Signature-based detection**, which uses a hash or other signature generation method to identify files or components of the malware that have been previously observed. Traditional antimalware tools often relied on signature-based detection as the first line of defense for systems, but attackers have increasingly used methods like polymorphism that change the malware every time it is installed, as well as encryption and packing to make signatures less useful.

- **Heuristic**-, or **behavior-based detection**, looks at what actions the malicious software takes and matches them to profiles of unwanted activities. Heuristic-based detection systems can identify new malware based on what it is doing, rather than just looking for a match to a known fingerprint.

- **AI and machine learning systems** are increasingly common throughout the security tools space. They leverage large amounts of data to find ways to identify malware that may include heuristic, signature, and other detection capabilities.

- **Sandboxing** is used by some tools and by the antimalware vendors themselves to isolate and run sample malicious code. A sandbox is a protected environment where unknown, untrusted, potentially dangerous, or known malicious code can be run to observe it. Sandboxes are instrumented to allow all the actions taken by the software to be documented, providing the ability to perform in-depth analysis.

Antimalware tools can be installed on mobile devices, desktops, and other endpoints like the devices and systems that handle network traffic, email, and anywhere else that malicious software could attack or be detected.

Using an antimalware package has been a consistent recommendation from security professionals for years since it is a last line of defense against systems being infected or compromised.

That also means that attackers have focused on bypassing and defeating antimalware programs, including using the same tools as part of their testing for new malicious software.

As you consider deploying antimalware tools, it is important to keep a few key decisions in mind.

First, you need to determine what threats you are likely to face and where they are likely to be encountered. In many organizations, a majority of malicious software threats are encountered on individual workstations and laptops, or are sent and received via email. Antimalware product deployments are thus focused on those two areas.

Second, management, deployment, and monitoring for tools is critical in an enterprise environment. Antimalware tools that allow central visibility and reporting integrates with other security tools for an easy view of the state of your systems and devices.

Third, the detection capabilities you deploy and the overall likelihood of your antimalware product to detect, stop, and remove malicious software plays a major role in decision processes.

Since malware is a constantly evolving threat, many organizations choose to deploy more than one antimalware technology, hoping to increase the likelihood of detection.

#

### Allow Lists and Deny Lists

One way to prevent malicious software from being used on systems is to control the applications that can be installed or used.

That's where the use of allow list and deny or block list tools come in.

Allow list tools allow you to build a list of software, applications, and other system components that are allowed to exist and run on a system. If they are not on the list, they will be removed or disabled, or will not be able to be installed.

Block lists, or deny lists, are lists of software or applications that cannot be installed or run, rather than a list of what is allowed.

The choice between the solutions depends on what administrators and security professionals want to accomplish.

If a system requires extremely high levels of security, an allow list will provide greater security than a block or deny list, but if specific programs are considered undesirable, a block list is less likely to interfere with unknown or new applications or programs.

Although these tools may sound appealing, they do not see widespread deployment in most organizations because of the effort required to maintain the lists.

Limited deployments and specific uses are more common throughout organizations, and other versions of allow and block lists are implemented in the form of firewalls and similar protective technologies.

#

### Endpoint Detection and Response

When antimalware tools are not sufficient, endpoint detection and response (EDR) tools can be deployed.

EDR tools combine monitoring capabilities on endpoint device and systems using a client or software agent with network monitoring and log analysis capabilities to collect, correlate, and analyze events.

Key features of EDR systems are the ability to search and explore the collected data and to use it for investigations as well as the ability to detect suspicious data.

With the continued growth of security analytics tools, EDR systems tend to look for anomalies and indicators of compromise (IoCs) using automated rules and detection engines as well as allowing manual investigation.

The power of an EDR system comes in its ability to make this detection and reporting capability accessible and useful for organizations that are dealing with very large quantities of security data.

If you are considering an EDR deployment, you will want to pay attention to organizational needs like the ability to respond to incidents; the ability to handle threats from a variety of sources, ranging from malware to data breaches; and the ability to filter and review large quantities of endpoint data in the broader context of your 
organizations.

#

### Data Loss Prevention

Protecting organizational data from both theft and inadvertent exposure drives the use of data loss prevention (DLP) tools.

DLP tools may be deployed to endpoints in the form of clients or applications.

These tools also commonly have network and server resident components to ensure that data is managed throughout its lifecycle and various handling processes.

Key elements of DLP systems include the ability to classify data so that organizations know which data should be protected; data labeling or tagging functions, to support classification and management practices; policy management and enforcement functions used to manage data to the standards set by the organization; and monitoring and reporting capabilities, to quickly notify administrators or security practitioners about issues or potential problems.

Some DLP systems also provide additional functions that encrypt data when it is sent outside of protected zones. 

In addition, they may include capabilities intended to allow sharing of data without creating potential exposure, either tokenizing, wiping, or otherwise modifying data to permit its use without violation of the data policies set in the DLP environment.

Mapping your organization's data, and then applying appropriate controls based on a data classification system or policy, is critical to success with a DLP system.

Much like antimalware and EDR systems, some DLP systems also track user behaviors to identify questionable behavior or common mistakes like assigning overly broad permissions on a file or sharing a sensitive document via email or a cloud file service.

Of course, even with DLP in place there are likely to be ways around the system.

Taking a picture of a screen, cutting and pasting, or printing sensitive data can all allow malicious or careless users to extract data from an environment even if effective and well-managed data loss prevention tools are in place. 

Thus, DLP systems are part of a layered security infrastructure that combines technical and administrative solutions such as data loss prevention with policies, awareness, and other controls based on the risks that the organization and its data face.

#

### Network Defenses

Protecting endpoints from network attacks can be done with a host-based firewall that can stop unwanted traffic.

Host-based firewalls are built into most modern operating systems and are typically enabled by default. Of course, host-based firewalls don't provide much insight into the traffic they are filtering since they often simply block or allow specific applications, services, ports, or protocols.

More advanced filtering requires greater insight into what the traffic being analyzed is, and that's where a host intrusion prevention or intrusion detection system comes in.

A host intrusion prevention system (HIPS) analyzes traffic before services or applications on the host process it.

A HIPS can take action on that traffic, including filtering out malicious traffic or blocking specific elements of the data that is received. A HIPS will look at traffic that is split across multiple packets or throughout an entire series of communications, allowing it to catch malicious activity that may be spread out or complex. 

Since a HIPS can actively block traffic, misidentification of traffic as malicious, misconfiguration, or other issues can cause legitimate traffic to be blocked, potentially causing an outage. If you choose to deploy a HIPS or any other tool that can actively block traffic, you need to consider what would happen if something did go wrong.

A host intrusion detection system (HIDS) performs similar functions but, like a traditional intrusion detection system (IDS) it cannot take action to block traffic. 

Instead, a HIDS can only report and alert on issues. Therefore, a HIDS has limited use for real-time security, but it has a much lower likelihood of causing issues.

Before deploying and managing host-based firewalls, HIPSs, or HIDSs, determine how you will manage them, how complex the individual configurations will be, and what would happen if the host-based protections had problems. 

Granular controls are an important part of a zero-trust design, and armoring hosts helps ensure that a compromised system behind a security boundary does not result in broader issues fo organizations.

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/8f7cf204-e6ec-4c33-a7d1-4eb46e21f33f)

Host firewalls and IPS systems vs. network firewalls and IPS systems

#

### Next-Generation Firewalls

Next-generation firewall is largely a marketing term for network security devices that include additional features beyond traditional firewalling capabilities.

That means that there isn't a single consistent definition of what they are and can do.

Fortunately, there are a few common features that are consistent among many firewall devices that claim the title of next-generation firewalls:

