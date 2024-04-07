# Malicious Code

**Malware** - describes a wide range of software that is intentionally designed to cause harm to systems and devices, networks, or users

Malware comes in many forms, from ransomware and remote access Trojans to Trojans, bots, and the command-and-control infrastructures that allow attackers to run entire networks of compromised systems

Can gather information, provide illicit access, and take a broad range of actions that the legitimate owner of a system or network may not want to occur

## 

### Ransomware

Malware that takes over a computer and then demands a ransom

Many types of ransomware

Crypto-malware which encrypts files and then holds them hostage until a ransom is paid

Other ransomware techniques include threatening to report the user to law enforcement due to pirated software or pornography, or threatening to expose sensitive information or pictures from the victim's hard drive or device

One of the most important defenses against ransomware is an effective backup system that stores files in a separate location that will not be impacted if the system or device it backs up is infected and encrypted by ransomware

##

#### Trojans

Malware that is typically disguised as legitimate software

Rely on unsuspecting individuals running them, thus providing attackers with a path into a system or device

**Remote access Trojans (RATs)** - provide attackers with remote access to systems and monitoring of a system for attackers

Security practitioners often combat Trojans and RATs using a combination of security awareness—to encourage users to not download untrusted software—and antimalware tools that detect Trojan and RAT-like behavior and known malicious files

##

### Worms

Worms spread themselves and self-install, rather than requiring users to click on them

Spread via attacks on vulnerable services, email attachments, network file shares, or other methods

>[!NOTE]
2010 Stuxnet attack is generally recognized as the first implementation of a worm as a cyber weapon. The worm was aimed at the Iranian nuclear program and copied itself to thumb drives to bypass air-gapped (physically separated systems without a network connection) computers. Stuxnet took
advantage of a number of advanced techniques for its time, including using a trusted digital certificate, searching for specific industrial control systems that were known to be used by the Iranian nuclear program, and specific programming to attack and damage centrifuges while providing false monitoring data to controllers to ensure that the damage would not be noticed until it was too late.

##

### Rootkits

Malware that is specifically designed to allow attackers to access a system through a backdoor

Modern rootkits also include capabilities that work to conceal the rootkit from detection through any of a variety of techniques, ranging from leveraging filesystem drivers to ensure that users cannot see the rootkit files, to infecting startup code in the master boot record (MBR) of a disk, thus allowing attacks against full-disk encryption systems.

Rootkit detection can be challenging because a system infected with malware like this cannot be trusted. That means that the best way to detect a rootkit is to test the suspected system from a trusted system or device

In cases where that isn't possible, rootkit detection tools look for behaviors and signatures that are typical of rootkits. Techniques like integrity checking and data validation against expected responses can also be useful for rootkit detection, and anti-rootkit tools often use a combination of these techniques to detect complex rootkits

Once a rootkit is discovered, removal can be challenging. Although some antimalware and anti-rootkit tools are able to remove specific rootkits, the most common recommendation whenever possible is to rebuild the system or to restore it from a known good backup

The best ways to prevent rootkits are normal security practices, including patching, using secure configurations, and ensuring that privilege management is used. Tools like secure boot and techniques that can validate live systems and files can also be used to help prevent rootkits from being successfully installed or remaining resident

## 

### Backdoors

Methods or tools that provide access that bypass normal authentication and authorization procedures, allowing attackers access to systems, devices, or applications. Backdoors can be hardware or software-based

A malware infection may include multiple types of malware tools. Trojans and rootkits often include a backdoor so that attackers can access the systems that they have infected.

Backdoors are sometimes used by software and hardware manufacturers to provide ongoing access to systems and software. Manufacturer-installed backdoors are a concern since they may not be disclosed, and if they are discovered by attackers, they can provide access that you may not be aware of.

Detecting backdoors can sometimes be done by checking for unexpected open ports and services, but more complex backdoor tools may leverage existing services

i.e. 

- web-based backdoors that require a different URL under the existing web service

- backdoors that conceal their traffic by tunneling out to a remote control host using encrypted or obfuscated channels

##

### Bots

Remotely controlled systems or devices that have a malware infection

Groups of bots are known as **botnets**, and botnets are used by attackers who control them to perform various actions, ranging from additional compromises and infection to denial-of-service attacks or acting as spam relays.

Many botnet command and control (C&C) systems operate in a client-server mode
![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/204754cb-a794-4fce-89b2-e383b30d6424)

In this model, they will contact central control systems, which provide commands and updates, and track how many systems are in the botnet

Internet Relay Chat (IRC) was frequently used to manage client-server botnets in the past, but many modern botnets rely on secure HTTP (HTTPS) traffic to help hide C&C traffic and to prevent it from easily being monitored and analyzed by defenders

>[!NOTE]
>Command and control (C&C) servers are the core of a botnet. They allow attackers to manage the botnet and advanced C&C tools have a broad range of capabilities that can help attackers steal data, conduct distributed denial-of-service attacks on a massive scale, deploy and update additional malware capabilities, and respond to attempts by defenders to protect their networks

Peer-to-peer networks connect bots to each other, making it harder to take down a single central server or a handful of known C&C IP addresses or domains. Encrypted peer-to-peer traffic can be exceptionally difficult to identify, although ML tools that monitor network traffic for behavior-based patterns, as well as large, multiorganization datasets, can help.

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/3836b798-11bc-4e33-acc1-0f1c87d66038)

Many botnets use fast flux DNS, which uses many IP addresses that are used to answer queries for one or more fully qualified DNS names. Frequent updates (fast flux) mean that the many systems in the network of control hosts register and de-register their addresses, often every few minutes on an ongoing basis

More advanced techniques also perform similar rapid changes to the DNS server for the DNS zone, making it harder to take the network down. Techniques like that can be defeated in controlled networks by forcing DNS requests to organizationally controlled DNS servers rather than allowing outbound DNS requests.

Logging all DNS requests can also provide useful information when malware hunting because machine-generated DNS entries can frequently be easily spotted in logs

>[!NOTE]
>Taking down the domain name is the best way to defeat a fast flux DNS–based botnet or malware, but not every DNS registrar is helpful when a complaint is made.

Detecting botnets is often accomplished by analysis of bot traffic using network monitoring tools like IPSs and IDSs and other network traffic analysis systems. Additional data is gathered through reverse engineering and analysis of malware infections associated with the bot. The underlying malware can be detected using antivirus and antimalware tools, as well as tools like endpoint detection and response tools.

### Botnets and Distributed Denial-of-Service (DDoS) Attacks

Botnets can be used to attack services and applications, and distributed denial-of-service (DDoS) attacks against applications are one common application of botnets

Botnets rely on a combination of their size, which can overwhelm applications and services, and the number of systems that are in them, which makes it nearly impossible to identify which hosts are maliciously consuming resources or sending legitimate-appearing traffic with malicious intent.

Identifying a botnet-driven DDoS attack requires monitoring network traffic, trends, and sometimes upstream visibility from an Internet service provider.

The symptoms can be difficult to identify from a significant increase in legitimate traffic, meaning that security tools like security information and event management (SIEM) systems that can correlate data from multiple sources may be required. Behavior analysis tools can also help differentiate a DDoS from more typical traffic patterns.

##

### Keyloggers

Programs that capture keystrokes from keyboards

May also capture other inputs like mouse movement, touchscreen inputs, or credit card swipes from attached devices

Keyloggers work in a multitude of ways, ranging from tools that capture data from the kernel to APIs or scripts, or even directly from memory.


