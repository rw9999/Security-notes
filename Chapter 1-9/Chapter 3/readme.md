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

Preventing software keylogging typically focuses on normal security best practices to ensure that malware containing a keylogger is not installed, including patching and systems management, as well as the use of antimalware tools. 

The use of multifactor authentication (MFA) can help limit the impact of a keylogger, even if it cannot defeat the keylogger itself.

In more complex security environments where underlying systems cannot be trusted, the use of bootable USB drives can prevent the use of a potentially compromised underlying operating system

##

### Logic Bombs

Not independent malicious programs, they are functions or code that are placed inside other programs that will activate when set conditions are met

Relatively rare compared to other types of malware, logic bombs are a consideration in software development and systems management, and they can have a significant impact if they successfully activate

##

### Viruses

Malicious programs that self-copy and self-replicate

Require one or more infection mechanisms that they use to spread themselves, typically paired with some form of search capability to find new places to spread to.

Typically have both a **trigger**, which sets the conditions for when the virus will execute, and a **payload**, which is what the virus does, delivers, or the actions it performs.

Viruses come in many varieties, including:

- Memory-resident viruses, which remain in memory while the system of the device is running
- Non-memory-resident viruses, which execute, spread, and then shut down
- Boot sector viruses, which reside inside the boot sector of a drive or storage media
- Macro viruses, which use macros or code inside word processing software or other tools to spread
- Email viruses, which spread via email either as attachments or as part of the email itself using flaws within email clients

##

### Fileless Viruses

Similar to traditional viruses. They spread via methods like spam email and malicious websites, and they exploit flaws in browser plug-ins and web browsers themselves.

Once they successfully find a way into a system, they inject themselves into memory and conduct further malicious activity, including adding the ability to reinfect the system by the same process at reboot through a registry entry or other technique

At no point do they require local file storage, because they remain memory resident throughout their entire active life.

The only stored artifact of many fileless attacks would be the artifacts of their persistence techniques.

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/dca985a4-8c4d-4092-8ab9-1645261a313c)

Ensuring that browsers, plug-ins, and other software that might be exploited by attackers are up-to-date and protected can prevent most attacks

Using antimalware tools that can detect unexpected behavior from scripting tools like PowerShell can also help stop fileless viruses.

Network-level defenses like IPSs, as well as reputation-based protection systems, can prevent potentially vulnerable systems from browsing known malicious sites

##

### Spyware

Designed to obtain information about an individual, organization, or system.

Many spyware packages track users' browsing habits, installed software, or similar information and report it back to central servers. Some spyware is relatively innocuous, but malicious spyware exists that targets sensitive data allows remote access to web cameras, or otherwise provides illicit or undesirable access to the systems it is installed on

Associated with identity theft and fraud, advertising and redirection of traffic, digital rights management (DRM) monitoring

**Stalkerware** is a type of spyware used to illicitly monitor partners in relationships.

Spyware is most frequently combated using antimalware tools, although user awareness can help prevent the installation of spyware that is included in installers for software (thus acting as a form of Trojan)

##

### Potentially Unwanted Programs (PUPs) 

>[!NOTE]
>PUPs are not technically malicious—they're annoying, they can be privacy risks, and they can slow a system down or otherwise cause problems but they aren't malware

Programs that may not be wanted by the user but are not as dangerous as other types of malware. Typically installed without the user's awareness or as part of a software bundle or other installation.

PUPs include adware, browser toolbars, web browser–tracking programs, and others.

Can be detected and removed by most antivirus and antimalware programs, and organizations may limit user rights to prevent the installation of additional software or to limit which software can be installed to prevent the installation of PUPs and other unwanted applications on their organizationally owned PCs

If you do see a report of a PUP on a system, bear in mind that you shouldn't immediately presume the system has been compromised.

##

### Malicious Code

Scripts and custom-built code that isn't malware can both be used by malicious actors

These attacks can happen locally or remotely via a network connection, and they often leverage built-in tools like Windows PowerShell and Visual Basic, or Bash and Python on Linux systems. Macros like those built into Microsoft's Office Suite can be leveraged by attackers.

PowerShell, the built-in Windows scripting language, is a popular target for malicious actors because due to its powerful capabilities. PowerShell allows remote and local execution, network access, and many other capabilities. Since it is available by default on Windows systems and is often not carefully monitored, attackers can leverage it in many different ways, including for fileless malware attacks

Defenses against PowerShell attacks include using Constrained Language Mode, which limits sensitive commands in PowerShell, and using Windows Defender's built-in Application Control tool or AppLocker to validate scripts and to limit which modules and plugins can be run. 

It's a good idea to turn on logging for PowerShell as well as Windows command-line auditing.

Microsoft Office disables macros by default. This means that the primary defense against macro-based malware is educating users to not enable macros on unknown or untrusted documents, and to provide appropriate scanning of any Office documents that are received by the organization via email or other means

Linux systems are also targeted. Attackers may leverage common languages and tools like Python, Perl, and Bash as part of their attack process. Languages like these can be used to create persistent remote access using bind or reverse shells, as well as a multitude of other useful exploit tools. Metasploit, a popular exploit tool, include  rootkits that leverage each of these languages

Preventing the use of built-in or preexisting tools like programming languages and shells can be difficult because they are an important part of how users interact with and use the systems they exist on.

That makes security that prevents attackers from gaining access to the systems through vulnerabilities, compromised accounts, and other means one of the most important layers of defense.

There are existing tools to search for rootkits like chkrootkit and rkhunter, which can help defenders search for and identify rootkits. Behavior-based security tools can also monitor system logs and network traffic to help defenders identify compromised systems

##

### Adversarial Artificial Intelligence

A developing field where artificial intelligence (AI) is used by attackers for malicious purposes

The focus of adversarial AI attacks currently tends to deal with data poisoning, providing security and analytic AI and ML algorithms with adversarial input that serves the attacker's purposes, or attacks against privacy.

**Artificial intelligence** - which focuses on accomplishing “smart” tasks by combining ML, deep learning, and related techniques that are intended to emulate human intelligence

**Machine learning** - a subset of AI, ML systems modify themselves as they evolve to become better at the task that they are set to accomplish

AI and ML continue to become increasingly common in security toolsets and enterprise analytics tools, the danger of training data that drives machine learning systems being intentionally or unintentionally tainted and thus providing incorrect responses continues to grow.

Tainted training data for machine learning algorithms will be a target and the security of machine learning algorithms themselves will be increasingly important.

New attack and defense techniques will be developed in response to the increase in the use of ML tools and techniques. As a security analyst, you can take some basic steps now:

- Understand the quality and security of source data.
- Work with AI and ML developers to ensure that they are working in secure environments and that data sources, systems, and tools are maintained in a secure manner.
- Ensure that changes to AI and ML algorithms are reviewed, tested, and documented.
- Encourage reviews to prevent intentional or unintentional bias in algorithms.
- Engage domain experts wherever possible.
