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

- Built-in IPS or IDS functionality, which can analyze traffic for attacks and either take action or alert on it
- Antimalware and antivirus features that allow them to scan traffic for malware in addition to performing firewall operations
- Geo-IP and geolocation capability to match threats with realworld locations
- Proxying, which allows the device to intercept traffic and analyze it by sitting in the middle of encrypted web traffic
- Web application firewall capabilities designed to protect web applications
- Sandboxing

Features may also include the ability to integrate threat intelligence feeds, perform behavior analysis, perform network tasks like load balancing or reverse proxy services, and many other functions. 

In short, they are more akin to all-in-one security devices than just a more advanced firewall, but that means they are also deployed at the network layer rather than at the endpoint.

## Hardening Endpoints and Systems

### Hardening

Hardening a system or application involves changing settings on the system to increase its overall level of security and reduce its vulnerability to attack. The concept of a system's attack surface, or the places where it could be attacked, is important when performing system hardening. Hardening tools and scripts are a common way to perform basic hardening processes on systems.

Hardening may also include techniques like application security improvements, sometimes called binary hardening.

Application hardening focuses on techniques that can prevent buffer overflows and other application attack techniques; however this topic is not covered in the exam outline, which means you may learn about it for your job, but not for the test.

#

### Service Hardening

One of the fastest ways to decrease the attack surface of a system is to reduce the number of open ports and services that it provides. 

Port scanners are commonly used to quickly assess which ports are open on systems on a network, allowing security practitioners to identify and prioritize hardening targets.

The easy rule of thumb for hardening is that only services and ports that must be available to provide necessary services should be open, and that those ports and services should be limited to only the networks or systems that they need to interact with. Unfortunately for many servers, this may mean that the systems need to be open to the world.

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/476afec2-6186-4ba9-9480-30c8d761c346)

Although blocking a service using a firewall is a viable option, the best option for unneeded services is to disable them entirely.

Starting and stopping services in Linux requires knowing how your Linux distribution handles services. For an Ubuntu Linux system, checking which services are running can be accomplished by using the service –status-all command. Starting and stopping services can be done in a number of ways, but the service command is an easy method. Issuing the sudo service [service name] stop or start commands will start or stop a service simply by using the information provided by the service -status-all command to identify the service you want to shut down. Permanently stopping services, however, will require you to make other changes. For Ubuntu, the update-rc.d script is called, whereas RedHat and CentOS systems use chkconfig.

You should understand the concept of disabling services to reduce the attack surface of systems, and that ongoing review and maintenance is required to ensure that new services and applications do not appear over time

#

### Operating System Hardening

Hardening operating systems relies on changing settings to match the desired security stance for a given system. 

Popular benchmarks and configuration standards can be used as a base and modified to an organization's needs, allowing tools like the CIS benchmark to be used throughout an organization. Fortunately, tools and scripts exist that can help make applying those settings much easier as well.

Examples of the type of configuration settings recommended by the CIS benchmark for Windows 10 include the following:

- Setting the password history to remember 24 or more passwords
- Setting maximum passwords age to “60 or fewer days, but not 0,” preventing users from simply changing their passwords 24 times to get back to the same password while requiring password changes every 2 months
- Setting the minimum password length to 14 or more characters
- Requiring password complexity
- Disabling the storage of passwords using reversible encryption

Operating system hardening uses system settings to reduce the attack surface for your operating system, that tools and standards exist to help with that process, and that assessing, auditing, and maintaining OS hardening for your organization is part of the overall security management process.

#

### Hardening the Windows Registry

The Windows registry is the core of how Windows tracks what is going on.

The registry is thus an important target for attackers, who can use it to automatically start programs, gather information, or otherwise take malicious action on a target machine. 

Hardening the Windows registry involves configuring permissions for the registry, disallowing remote registry access if it isn't required for a specific need, and limiting access to registry tools like regedit so that attackers who do gain access to a system will be less likely to be able to change or view the registry.

#

### Configuration, Standards, and Schemas

To harden systems in an enterprise environment, you'll need to manage the configuration of systems through your organization.

In fact, configuration management tools are one of the most powerful options security professionals and system administrators have to ensure that the multitude of systems in their organizations have the right security settings and to help keep them safe.

A third-party configuration management system like Jamf Pro for macOS, a vendor-supplied tool like Configuration Manager for Windows, or even open source configuration management tools like CFEngine help enforce standards, manage systems, and report on areas where systems do not match expected settings.

Configuration management tools often start with **baseline configurations** for representative systems or operating system types throughout an organization.

Baseline configurations are an ideal starting place to build from to help reduce complexity and make configuration management and system hardening possible across multiple machines—even thousands of them.

In addition to configuration management standards and tools, documentation is an important part of configuration management. 

Diagrams, including architecture, network, and dataflow diagrams, are used to understand and document how an organization's technology and system are set up. 

Establishing an organizational habit of producing system and architecture diagrams, ensuring that they meet quality standards and that they are updated when things change, helps ensure that deployments meet organizational standards. 

The same diagrams are critical when performing incident response and disaster recovery operations because they allow responders to quickly understand how infrastructure and systems are configured, how they interconnect, where data flows, how it gets from place to place, and what dependencies exist in a system or application architecture. Diagrams and documentation can also be provided to auditors, providing a useful artifact for assessment of designs.

#

### Naming Standards and Addressing Schemas

Hardening endpoints involves knowing which systems you're managing and ensuring that the systems on your network are the systems that you expect to be there. Standards can help with that.

The Security+ exam calls out standard naming conventions as one option. Naming conventions play a number of roles:

- They can help you identify systems based on purpose, location, or other elements included in the naming convention. 
- They can be used to make systems more anonymous; examplecorp123 is less meaningful to an attacker than examplesqlserver or examplewebserver.
-  They make scripting and management easier because you can filter, sort, and take other actions more easily using a standard naming convention.

Using a standardized Internet Protocol (IP) schema is also useful. 

Segmenting systems based on purpose, location, or other factors and ensuring that you are managing the IP address space that your organization uses help you avoid address collisions, avoid running out of addresses in network segments, and identify systems that shouldn't be using a given address. 

This capability becomes even more important when you are designing a datacenter or a cloud infrastructure and assigning IP addresses. If you run out of addresses and have to re-address a datacenter, significant rework may be required to update firewall rules, infrastructure-as-code scripts and tools, or other places where you have made a significant time investment.

#

### Patch Management

Ensuring that systems and software are up to date helps ensure endpoint security by removing known vulnerabilities. 

Timely patching decreases how long exploits and flaws can be used against systems, but patching also has its own set of risks. Patches may introduce new flaws, or the patching process itself can sometimes cause issues.

The importance of patching, as well as the need to make sure that patching is controlled and managed, is where patch management comes in.

A significant proportion of modern software, including software, browsers, office suites, and many other packages, has built-in automatic update tools. These tools check for an update and either notify the user requesting permission to install the updates or automatically install the update. Although this model is useful for individual devices, an enterprise solution makes sense for organizations.

Patch management for operating systems can be done using tools like Microsoft's Endpoint Configuration Manager for Windows, but third-party tools provide support for patch management across a wide variety of software applications.

Tracking versions and patch status using a systems management tool can be important for organizational security, particularly because third-party updates for the large numbers of applications and packages that organizations are likely to have deployed can be a daunting task.

A common practice for many organizations is to delay the installation of a patch for a period of a few days from its release date. That allows the patch to be installed on systems around the world, hopefully providing insight into any issues the patch may create.

In cases where a known exploit exists, organizations have to choose between the risk of patching and the risk of not patching and having the exploit used against them. Testing can help, but many organizations don't have the resources to do extensive patch testing.

Managing software for mobile devices remains a challenge, but mobile device management tools also include the ability to validate software versions. These tools often have the ability to update applications and the device operating system in addition to controlling security settings.

As you consider endpoint security, think about how you will update your endpoint devices, the software and applications they run, and what information you would need to know that patching was consistent and up-to-date.

Key features like reporting, the ability to determine which systems or applications get updates and when, the ability to block an update, and of course being able to force updates to be installed are all critical to enterprise patch management over the many different types of devices in our organizations today.

#

### Disk Security and Sanitization

Keeping the contents of disks secure protects data in the event that a system or disk is lost or stolen. That's where disk encryption comes in.

**Full-disk encryption** (FDE) encrypts the disk and requires that the bootloader or a hardware device provide a decryption key and software or hardware to decrypt the drive for use. 

One of the most common implementations of this type of encryption is transparent encryption (sometimes called on-the-fly, or real-time, encryption). Transparent encryption implementations are largely invisible to the user, with the drive appearing to be unencrypted during use. This also means that the simplest attack against a system that uses transparent FDE is to gain access to the system while the drive is unlocked.

Volume encryption (sometimes called filesystem-level encryption) protects specific volumes of the drive, allowing different trust levels and additional security beyond that provided by encrypting the entire disk with a single key. 

File and folder encryption methods can also be used to protect specific data, again allowing for different trust levels, as well as transfer of data in secure ways.

The Opal Storage Specification is a standard published by the Trusted Computing Group's Storage Workgroup. It specifies both how devices must protect data when they are outside of their owners' control, and how to ensure that devices produced by various vendors can all interoperate successfully.

Full-disk encryption can be implemented at the hardware level using a **self-encrypting drive** (SED).

Self-encrypting drives implement encryption capabilities in their hardware and firmware.

Systems equipped with a self-encrypting drive require a key to boot from the drive, which may be entered manually or provided by a hardware token or device. 

Since this is a form of full-disk encryption, the same sort of attack methods work—simply find a logged-in system or one that is in sleep mode.

Disk encryption does bring potential downfalls. If the encryption key is lost, the data on the drive will likely be unrecoverable since the same strong encryption that protects it will make it very unlikely that you will be able to brute-force the key and acquire the data.

Technical support can be more challenging, and data corruption or other issues can have a larger impact, resulting in unrecoverable data. 

Despite these potential downfalls, the significant advantage of full-disk encryption is that a lost or stolen system with a fully encrypted drive can often be handled as a loss of the system, instead of a loss or breach of the data that system contained.

#

### Sanitization

Ensuring that a disk is securely wiped when it is no longer needed and is being retired or when it will be reused is an important part of the lifespan for drives.

Sanitizing drives or media involves one of two processes: wiping the data or destroying the media.

Tapes and similar magnetic media have often been wiped using a degausser, which exposes the magnetic media to very strong electromagnetic fields, scrambling the patterns of bits written to the drive. Degaussers are a relatively quick way to destroy the data on magnetic media. SSDs, optical media and drives, and flash drives, however, require different handling.

Wiping media overwrites or discards the data in a nonrecoverable way. 

For hard drives and other magnetic media, this may be accomplished with a series of writes, typically of 1s or 0s, to every storage location (bit) on the drive. 

Various tools like Darik's Boot and Nuke (DBAN) will perform multiple passes over an entire disk to attempt to ensure that no data remains.

In fact, data remanence, or data that is still on a disk after the fact, is a significant concern, particularly with SSD and other flash media that uses wear-leveling algorithms to spread wear and tear on the drive over more space than the listed capacity.

Wiping SSDs using a traditional drive wipe utility that writes to all accessible locations will miss sections of the disk where copies of data may remain due to the wear-leveling process.

Fortunately, tools that can use the built-in secure Erase command for drives like these can help make sure remnant data is not an issue.

An even better solution in many cases is to use full-disk encryption for the full life of a drive and then simply discard the encryption key when the data is ready to be retired. Unless your organization faces advanced threats, this approach is likely to keep the data from being recoverable by even reasonably advanced malicious actors.

Since wiping drives can have problems, destroying drives is a popular option for organizations that want to eliminate the risk of data loss or exposure. Shredding, pulverizing, or incinerating drives so that no data could possibly be recovered is an option, and third-party vendors specialize in providing services like these with a documented trail for each asset (drive or system) that is destroyed.

Although this does cause a loss of some potential recoverable value, the remaining value of older drives is much less than the cost of a single breach in the risk equations for organizations that make this decision.

#

### File Manipulation and Other Useful Command-Line Tools

The ability to quickly gather information from a file, to manipulate it, to change its permissions, or simply to search through it can make the difference between successfully handling an incident, identifying an issue, or making operational tasks go faster. 

The Security+ exam focuses on six command-line tools:

- head is a command that shows you the first part of a file. By default, it will show you the first 10 lines of a file, making it a handy tool to quickly see what a file contains. You can change the number of lines shown by using the -n flag, and you can show lines from multiple files by including them on the command line.

- tail is very similar to the head command, but it displays the last 10 lines of a file by default. tail is often used to view recent log entries or other data in a file that is changing. As with head, you can add the -n flag to show an arbitrary number of lines, but the most useful mode in many cases is the -f flag, which follows changes. Using tail -f will show you the file as it changes. As with head, you can also monitor multiple files at a time.

- cat, short for concatenate, can be used to output files to standard output (your console) or to append files to other files.

- grep is a search tool that allows you to search for patterns that match provided text or regular expressions.The grep command has a number of handy capabilities, such as the -A and -B options, which when provided with a number as input, will print that many lines after or before the matching pattern. This makes grep an ideal tool for quickly searching through logs and other text files, looking for specific information.

- chmod lets you set permissions on files and directories, using either a symbol or a numeric representation of the permissions that you want to set.

- logger is the most obscure of the commands that the Security+ exam includes. The logger command will append whatever information you provide as input to the/var/log/syslog file on the system. logger can also be used to add information from other commands or files to the syslog file by calling that command or file via logger.

#

### Scripting, Secure Transport, and Shells

Another useful set of tools in your endpoint security toolkit are shells and scripting languages.

The ability to connect to a command-line interface, or to use one on a local system, and then to execute commands like the file manipulation commands we just explored provides a powerful ability to control and manage systems.

Secure Shell, or SSH, is an encrypted protocol used to connect to systems, typically via the command line. SSH is also the name of a client that uses the SSH protocol to create that connection. Once you're connected via SSH, you can issue commands in whatever shell environment the system you're using runs.

Windows systems have a built-in management, automation, and scripting language tool called PowerShell. PowerShell scripts and commands allow management and configuration of Windows systems from the command line.

PowerShell can report on the current state of the system, make changes both locally and to remote systems, and has many other features that make it a favorite tool for both attackers and defenders.

Scripting languages like Python are also used for both systems management and maintenance tasks as well as to provide a powerful way for users to tackle complex tasks by automating them. Although Python has become increasingly common, Perl and other languages also remain in use for scripting and as part of software packages, particularly for Linux and Unix-based systems.

OpenSSL isn't a shell, and it isn't a scripting language. 

Instead, much like SSH, OpenSSL is an implementation of the TLS protocol and is often used to protect other services.

OpenSSL's TLS implementation is used for HTTPS traffic; any time traffic needs to be sent across a network in a protected way that isn't a good match for tunneling via SSH or a VPN connection, OpenSSL is likely to be a reasonable alternative. As a security professional, you need to be aware that 

OpenSSL is frequently used to wrap this traffic and thus you will encounter it embedded in many places.

That means you need to understand why it might be used, and know the features that it brings that help improve the security of communications for your organization. 

One of the key elements of the TLS protocol is that it provides for ephemeral RSA key exchange to create perfect forward secrecy. In other words, conversations can be decrypted only when the key is known, and a temporary key is generated as part of the start of communications between two systems. 

Thus, using OpenSSL and TLS is an ideal solution when two systems that may not have ever communicated before need to communicate securely. 

Websites use TLS for this purpose all the time, and your security assessment of systems that host websites or other services where systems may need to communicate securely without having additional configuration or prior communication should identify OpenSSL and TLS as a secure option

Misconfigured or improperly configured OpenSSL installations will allow the use of weak encryption suites, possibly permitting downgrade attacks that can result in data exposure.

Consider whether OpenSSL's allowed set of encryption options matches your organization's needs, even if OpenSSL is configured for a web or other service that you are reviewing.

OpenSSL isn't used to assess security, but assessing OpenSSL, whether it should be deployed, and how it is deployed is a part of security assessments.

## Securing Embedded and Specialized Systems

Security practitioners encounter traditional computers and servers every day, but as smart devices, embedded systems, and other specialized systems continue to be built into everything from appliances, to buildings, to vehicles, and even clothing, the attack surface for organizations is growing in new ways. 

Wherever these systems appear, they need to be considered as part of an organization's overall security posture.

### Embedded Systems

Embedded systems are computer systems that are built into other devices.

Industrial machinery, appliances, and cars are all places where you may have encountered embedded systems. 

Embedded systems are often highly specialized, running customized operating systems and with very specific functions and interfaces that they expose to users. In a growing number of cases, however, they may embed a relatively capable system with Wi-Fi, cellular, or other wireless access that runs Linux or a similar, more familiar operating system.

Many embedded systems use a **real-time operating system** (RTOS).

A RTOS is an operating system that is used when priority needs to be placed on processing data as it comes in, rather than using interrupts for the operating system or waiting for tasks being processed to be handled before data is processed. 

Since embedded systems are widely used for industrial processes where responses must be quick, real-time operating systems are used to minimize the amount of variance in how quickly the OS accepts data and handles tasks.

**Raspberry Pi**s are single-board computers, which means that they have all the features of a computer system on a single board, including network connectivity, storage, video output, input, CPU and memory.

Raspberry Pi devices provide a relatively capable computational platform, and they can run a variety of operating systems, including Linux and Windows. Raspberry Pi devices are more likely to be found used for personal development or small-scale custom use rather than in broader deployment as the core of industrial or commercial embedded systems.

Arduinos, unlike the Raspberry Pi, are not considered single-board computers. Instead, they belong to a class of computer known as a **microcontroller**. 

They include a lower-power CPU with a small amount of memory and storage, and they provide input and output capabilities. They are often used for prototyping devices that interface with sensors, motors, lighting, and similar basic capabilities.

Unlike the Raspberry Pi, Arduinos do not have a wireless or wired network connection built into them, thus reducing their attack surface because they lack direct physical access.

Field-programmable gate array (FPGA)s are a type of computer chip that can be programmed to redesign how it works, allowing it to be a customizable chip. 

A manufacturer that chooses to use an FPGA can program it to perform specific tasks with greater efficiency than a traditional purpose-built chip. 

An FPGA alone is not an embedded system, however. Systems may integrate FPGAs as a component in an embedded system or as the program processor inside of one. If an embedded system integrates an FPGA, you need to be aware that it could potentially be reprogrammed.

Embedded systems come in many flavors and can be so fully embedded that you may not realize that there is a system embedded in the device you are looking at.

As a security professional, you need to be able to assess embedded system security and identify ways to ensure that they remain secure and usable for their intended purpose without causing the system itself to malfunction or suffer from unacceptable degradations in performance.

Assessing embedded systems can be approached much as you would a traditional computer system:

1. Identify the manufacturer or type of embedded system and acquire documentation or other materials about it.
2. Determine how the embedded system interfaces with the world: does it connect to a network, to other embedded devices, or does it only have a keyboard or other physical interface?
3. If the device does provide a network connection, identify any services or access to it provided through that network connection, and how you can secure those services or the connection itself.
4. Learn about how the device is updated, if patches are available, and how and when those patches should be installed; then ensure a patching cycle is in place that matches the device's threat model and usage requirements.
5. Document what your organization would do in the event that the device had a security issue or compromise. Could you return to normal? What would happen if the device were taken offline due to that issue? Are there critical health, safety, or operational issues that might occur if the device failed or needed to be removed from service?
6. Document your findings, and ensure that appropriate practices are included in your organization's operational procedures.

#

### SCADA and ICS

Industrial and manufacturing systems are often described using one of two terms.

Industrial controls systems (ICSs) is a broad term for industrial automation, and Supervisory Control and Data Acquisition (SCADA) often refers to large systems that run power and water distribution or other systems that cover large areas.

Since the terms overlap, they are often used interchangeably.

SCADA is a type of system architecture that combines data acquisition and control devices, computers, communications capabilities, and an interface to control and monitor the entire architecture. 

SCADA systems are commonly found running complex manufacturing and industrial processes, where the ability to monitor, adjust, and control the entire process is critical to success.

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/8ad6a8a4-9838-4004-b072-aad850a80e17)

You'll see that there are remote telemetry units (RTUs) that collect data from sensors and programmable logic controllers (PLCs) that control and collect data from industrial devices like machines or robots.

Data is sent to the system control and monitoring controls, allowing operators to see what is going on and to manage the SCADA system. 

These capabilities mean that SCADA systems are in common use in industrial and manufacturing environments, as well as in the energy industry to monitor plants and even in the logistics industry tracking packages and complex sorting and handling systems.

ICS and SCADA can also be used to control and manage facilities, particularly when the facility requires management of things like heating, ventilation, and air-conditioning (HVAC) systems to ensure that the processes or systems are at the proper temperature and humidity.

Since ICS and SCADA systems combine general-purpose computers running commodity operating systems with industrial devices with embedded systems and sensors, they present a complex security profile for security professionals to assess. 

In many cases, they must be addressed as individual components to identify their unique security needs, including things like customized industrial communication protocols and proprietary interfaces. 

Once those individual components are mapped and understood, their interactions and security models for the system as a whole or as major components can be designed and managed. 

A key thing to remember when securing complex systems like this is that they are often designed without security in mind. That means that adding security may interfere with their function or that security devices may not be practical to add to the environment.

In some cases, isolating and protecting ICS, SCADA, and embedded systems is one of the most effective security models that you can adopt.

#

### Securing the Internet of Things

The Internet of Things (IoT) is a broad term that describes network-connected devices that are used for automation, sensors, security, and similar tasks. 

IoT devices are typically a type of embedded system, but many leverage technologies like machine learning, AI, cloud services, and similar capabilities to provide “smart” features.

IoT devices bring a number of security and privacy concerns, and security analysts must be aware of these common issues:

- Poor security practices, including weak default settings, lack of network security (firewalls), exposed or vulnerable services, lack of encryption for data transfer, weak authentication, use of embedded credentials, insecure data storage, and a wide range of other poor practices.

- Short support lifespans—IoT devices may not be patched or updated, leaving them potentially vulnerable for most of their deployed lifespan.

- Vendor data-handling practice issues, including licensing and data ownership concerns, as well as the potential to reveal data to both employees and partners of the vendor and to government and other agencies without the device owner being aware.

Despite these security concerns, IoT devices like sensors, building and facility automation devices, wearables, and other smart devices continue to grow in popularity. 

Security professionals must account for both the IoT devices that their organization procures and that staff and visitors in their facilities may bring with them.

#

### Specialized Systems

The final category of embedded systems that you need to consider for the Security+ exam is specialized systems:

- Medical systems, including devices found in hospitals and at doctor offices, may be network-connected or have embedded systems. Medical devices like pacemakers, insulin pumps, and other external or implantable systems can also be attacked, with exploits for pacemakers via Bluetooth already existing in the wild.

- Smart meters are deployed to track utility usage, and bring with them a wireless control network managed by the utility. Since the meters are now remotely accessible and controllable, they provide a new attack surface that could interfere with power, water, or other utilities, or that could provide information about the facility or building.

- Vehicles ranging from cars to aircraft and even ships at sea are now network connected, and frequently are directly Internet connected. If they are not properly secured, or if the backend servers and infrastructure that support them is vulnerable, attackers can take control, monitor, or otherwise seriously impact them.

- Drones and autonomous vehicles (AVs), as well as similar vehicles may be controlled from the Internet or through wireless command channels. Encrypting their command-and-control channels and ensuring that they have appropriate controls if they are Internet or network connected are critical to their security.

- VoIP systems include both backend servers as well as the VoIP phones and devices that are deployed to desks and work locations throughout an organization. The phones themselves are a form of embedded system, with an operating system that can be targeted and may be vulnerable to attack. Some phones also provide interfaces that allow direct remote login or management, making them vulnerable to attack from VoIP networks. Segmenting networks to protect potentially vulnerable VoIP devices, updating them regularly, and applying baseline security standards for the device help keep VoIP systems secure.

- Printers, including multifunction printers (MFPs), frequently have network connectivity built in. Wireless and wired network interfaces provide direct access to the printers, and many printers have poor security models. Printers have been used as access points to protected networks, to reflect and amplify attacks, and as a means of gathering information. In fact, MFPs, copiers, and other devices that scan and potentially store information from faxes, printouts, and copies make these devices a potentially significant data leakage risk in addition to the risk they can create as vulnerable networked devices that can act as reflectors and amplifiers in attacks, or as pivot points for attackers.

- Surveillance systems like camera systems and related devices that are used for security but that are also networked can provide attackers with a view of what is occurring inside a facility or organization. Cameras provide embedded interfaces that are commonly accessible via a web interface.

- Default configurations, vulnerabilities, lack of patching, and similar issues are common with specialized systems, much the same as with other embedded systems. When you assess specialized systems, consider both how to limit the impact of these potential problems and the management, administration, and incident response processes that you would need to deal with them for your organization.

#

### Communication Considerations

Many embedded and specialized systems operate in environments where traditional wired and wireless networks aren't available. As a security professional, you may need to account for different types of connectivity that are used for embedded systems.

Cellular connectivity, including both existing LTE and other fourthgeneration technologies as well as newer 5G network connectivity, can provide high-bandwidth access to embedded systems in many locations where a Wi-Fi network wouldn't work.

Since third-party cellular providers are responsible for connectivity, embedded systems that use cellular connectivity need to be secured so that the cellular network does not pose a threat to their operation.

Ensuring that they do not expose vulnerable services or applications via their cellular connections is critical to their security.

Building in protections to prevent network exploits from traversing internal security boundaries such as those between wireless connectivity and local control buses is also a needed design feature.

Physically securing the subscriber identity module (SIM) built into cellular-enabled devices can be surprisingly important.

Documented examples of SIMs being removed and repurposed, including running up significant bills for data use after they were acquired, appear regularly in the media.

SIM cloning attacks can also allow attackers to present themselves as the embedded system, allowing them to both send and receive information as a trusted system.

Embedded systems may also take advantage of radio frequency protocols specifically designed for them.

Zigbee is one example of a network protocol that is designed for personal area networks like those found in houses for home automation. Protocols like Zigbee and Z-wave provide low-power, peer-to-peer communications for devices that don't need the bandwidth and added features provided by Wi-Fi and Bluetooth.

That means that they have limitations on range and how much data they can transfer and that since they are designed for home automation and similar uses they do not have strong security models.

As a security practitioner, you should be aware that devices that communicate using protocols like Zigbee may be deployed as part of building monitoring or other uses and are unlikely to have enterprise management, monitoring, or security capabilities.

Radiofrequency systems like Zigbee can be narrowband or wideband.

Narrowband radio systems generally have less noise and thus better range and sensitivity, whereas wideband radios can transfer more data because they have more wireless spectrum to use.

Baseband radio is a type of signal that includes frequencies near zero.

Broadband uses wide bandwidth to send data, often using multiple signals and different traffic types. Broadband is not limited to wireless and can be used in optical, coaxial, or twisted-pair wired networks as well.

#

### Security Constraints of Embedded Systems

Embedded systems have a number of constraints that security solutions need to take into account.

Since embedded systems may have limited capabilities, differing deployment and management options, and extended lifecycles, they required additional thought to secure.

When you consider security for embedded systems, you should take the following into account:

- The overall computational power and capacity of embedded systems is usually much lower than a traditional PC or mobile device. Although this may vary, embedded systems may use a low-power processor, have less memory, and have very limited storage space. That means that the compute power needed for cryptographic processing may not exist, or it may have to be balanced with other needs for CPU cycles. At the same time, limited memory and storage capacity mean that there may not be capacity to run additional security tools like a firewall, antimalware tools, or other security tools you're used to including in a design.

- Embedded systems may not connect to a network. They may have no network connectivity, or they may have it but due to environmental, operational, or security concerns it may not be enabled or used. In fact, since many embedded systems are deployed outside of traditional networks, or in areas where connectivity may be limited, even if they have a built-in wireless network capability, they may not have the effective range to connect to a viable network. Thus, you may encounter an inability to patch, monitor, or maintain the devices remotely. Embedded devices may need to be secured as an independent unit.

- Without network connectivity, CPU and memory capacity, and other elements, authentication is also likely to be impossible. In fact, authenticating to an embedded system may not be desirable due to safety or usability factors. Many of the devices you will encounter that use embedded systems are built into industrial machinery, sensors and monitoring systems, or even household appliances. Without authentication, other security models need to be identified to ensure that changes to the embedded system are authorized.

- Embedded systems may be very low cost, but many are effectively very high cost because they are a component in a larger industrial or specialized device. So, simply replacing a vulnerable device can be impossible, requiring compensating controls or special design decisions to be made to ensure that the devices remain secure and do not create issues for their home organization.

Because of all these limitations, embedded devices may rely on implied trust. 

They presume that operators and those who interact with them will be doing so because they are trusted, and that physical access to the device means that the user is authorized to use and potentially change settings, update the device, or otherwisemodify it.

The implied trust model that goes with physical access for embedded devices makes them a potential vulnerability for organizations, and one that must be reviewed and designed for before they are deployed.
