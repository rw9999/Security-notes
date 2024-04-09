# Security Assessment and Testing

### Vulnerability Management

**Vulnerability management** programs play a crucial role in identifying, prioritizing, and remediating vulnerabilities in our environments

They use **vulnerability scanning** to detect new vulnerabilities as they arise and then implement a remediation workflow that addresses the highest-priority vulnerabilities.

##

### Identifying Scan Targets

Once an organization decides that it wishes to conduct vulnerability scanning and determines which, if any, regulatory requirements apply to their scans, they move on to the more detailed phases of the planning process.

The next step is to identify the systems that will be covered by the vulnerability scans. Some organizations choose to cover all systems in their scanning process, whereas others scan systems differently (or not at all) depending on the answers to many different questions, including

- What is the data classification of the information stored, processed, or transmitted by the system?

- Is the system exposed to the Internet or other public or semipublic networks?

- What services are offered by the system?

- Is the system a production, test, or development system?

Organizations also use automated techniques to identify the systems that may be covered by a scan. 

Cybersecurity professionals use scanning tools to search the network for connected systems, whether they were previously known or unknown, and to build an **asset inventory**.

Administrators may then supplement this inventory with additional information about the type of system and the information it handles. This information then helps make determinations about which systems are critical and which are non-critical.

Asset inventory and **asset criticality** information help guide decisions about the types of scans that are performed, the frequency of those scans, and the priority administrators should place on remediating vulnerabilities detected by the scan.

##

### Determining Scan Frequency

Vulnerability scanning tools allow the automated scheduling of scans to take the burden off administrators.

Administrators may designate a schedule that meets their security, compliance, and business requirements.

Administrators should configure these scans to provide automated alerting when they detect new vulnerabilities.

Many different factors influence how often an organization decides to conduct vulnerability scans against its systems:

- The organization's **risk appetite** is its willingness to tolerate risk within the environment. If an organization is extremely risk averse, it may choose to conduct scans more frequently to minimize the amount of time between when a vulnerability comes into existence and when it is detected by a scan.

- **Regulatory requirements**, such as those imposed by the Payment Card Industry Data Security Standard (PCI DSS) or the Federal Information Security Management Act (FISMA), may dictate a minimum frequency for vulnerability scans. These requirements may also come from corporate policies.

- **Technical constraints** may limit the frequency of scanning. The scanning system may only be capable of performing a certain number of scans per day, and organizations may need to adjust scan frequency to ensure that all scans complete successfully.
 
 - **Business constraints** may limit the organization from conducting resource-intensive vulnerability scans during periods of high business activity to avoid disruption of critical processes.

 - **Licensing limitations** may curtail the bandwidth consumed by the scanner or the number of scans that may be conducted simultaneously.

## Configuring Vulnerability Scans

Vulnerability management solutions provide administrators with the ability to configure many different parameters related to scans.

In addition to scheduling automated scans and producing reports, administrators may customize the types of checks performed by the scanner, provide credentials to access target servers, install scanning agents on target servers, and conduct scans from a variety of network perspectives.

It is important to conduct regular **configuration reviews** of vulnerability scanners to ensure that scan settings match current requirements.

##

### Scan Sensitivity Levels

Cybersecurity professionals configuring vulnerability scans should pay careful attention to the configuration settings related to the scan sensitivity level.

These settings determine the types of checks that the scanner will perform and should be customized to ensure that the scan meets its objectives while minimizing the possibility of disrupting the target environment.

Typically, administrators create a new scan by beginning with a template. As administrators create their own scan configurations, they should consider saving common configuration settings in templates to allow efficient reuse of their work, saving time and reducing errors when configuring future scans.

Administrators may also improve the efficiency of their scans by configuring the specific plug-ins that will run during each scan. Each plug-in performs a check for a specific vulnerability, and these plugins are often grouped into families based on the operating system, application, or device that they involve.

Disabling unnecessary plugins improves the speed of the scan by bypassing unnecessary checks and also may reduce the number of false positive results detected by the scanner.

**Intrusive plug-ins** perform tests that may disrupt activity on a production system or, in the worst case, damage content on those systems.

Administrators want to run these scans because they may identify problems that could be exploited by a malicious source.

At the same time, cybersecurity professionals don't want to cause problems on the organization's network and, as a result, may limit their scans to **nonintrusive plug-ins**.

One way around this problem is to maintain a test environment containing copies of the same systems running on the production network and run scans against those test systems first.

### Supplementing Network Scans

Basic vulnerability scans run over a network, probing a system from a distance. This provides a realistic view of the system's security by simulating what an attacker might see from another network vantage point

Intrusion prevention systems and other security controls that exist on the path between the scanner and the target server may affect the scan results, providing an inaccurate view of the server's security independent of those controls

Many security vulnerabilities are difficult to confirm using only a remote scan. Vulnerability scans that run over the network may detect the possibility that a vulnerability exists but be unable to confirm it with confidence, causing a false positive result that requires time-consuming administrator investigation

Modern vulnerability management solutions can supplement these remote scans with trusted information about server configurations

First, administrators can provide the scanner with credentials that allow the scanner to connect to the target server and retrieve configuration information. This information can then be used to determine whether a vulnerability exists, improving the scan's accuracy over noncredentialled alternatives. 

**Credentialed scans** may access operating systems, databases, and applications, among other sources. Credentialed scans typically only retrieve information from target servers and do not make changes to the server itself.

Typically only retrieve information from target servers and do not make changes to the server itself. Administrators should enforce the principle of least privilege by providing the scanner with a read-only account on the server

Some scanners supplement the traditional** server-based scanning** approach to vulnerability scanning with a complementary **agent-based scanning** approach

In this approach, administrators install small software agents on each target server. These agents conduct scans of the server configuration, providing an “inside-out” vulnerability scan, and then report information back to the vulnerability management platform for analysis and reporting

The agent may cause performance or stability issues. If you choose to use an agent-based approach to scanning, you should approach this concept conservatively, beginning with a small pilot deployment that builds confidence in the agent before proceeding with a more widespread deployment

##

### Scan Perspective

Conducts the scan from a different location on the network, providing a different view into vulnerabilities

An external scan is run from the Internet, giving administrators a view of what an attacker located outside the organization would see as potential vulnerabilities.

Internal scans might run from a scanner on the general corporate network, providing the view that a malicious insider might encounter

Scanners located inside the data center and agents located on the servers offer the most accurate view of the real state of the server by showing vulnerabilities that might be blocked by other security controls on the network

Controls that might affect scan results include the following: 

- Firewall settings
	
- Network segmentation 
	
- Intrusion detection systems (IDSs) 
	
- Intrusion prevention systems (IPSs)

Vulnerability management platforms have the ability to manage different scanners and provide a consolidated view of scan results, compiling data from different sources.

##

### Scanner Maintenance

Administrators should conduct regular maintenance of their vulnerability scanners to ensure that the scanning software and **vulnerability feeds** remain up-to-date.

Scanning systems do provide automatic updating capabilities that keep the scanner and its vulnerability feeds up-to-date.

It is always a good idea to check in once in a while and manually verify that the scanner is updating properly.

##

### Scanner Software

Scanning systems themselves aren't immune from vulnerabilities.

Regular patching of scanner software protects an organization against scanner-specific vulnerabilities and also provides important bug fixes and feature enhancements to improve scan quality.

##

### Vulnerability Plug-in Feeds

Security researchers discover new vulnerabilities every week, and vulnerability scanners can only be effective against these vulnerabilities if they receive frequent updates to their plug-ins. 

Administrators should configure their scanners to retrieve new plugins on a regular basis, preferably daily.

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/0b5146bf-db54-4b87-a202-16d41343556b)


## Vulnerability Scanning Tools

Vulnerability scanners are often leveraged for preventive scanning and testing and are also found in penetration testers' toolkits where they help identify systems that testers can exploit.

### Infrastructure Vulnerability Scanning

Network vulnerability scanners are capable of probing a wide range of network-connected devices for known vulnerabilities.

They reach out to any systems connected to the network, attempt to determine the type of device and its configuration, and then launch targeted tests designed to detect the presence of any known vulnerabilities on those devices.

- Nessus
- Qualys
- Nexpose
- OpenVAS

##

### Application Scanning

Web application scanners are specialized tools used to examine the security of web applications.

These tools test for web-specific vulnerabilities, such as SQL injection, cross-site scripting (XSS), and cross-site request forgery (CSRF) vulnerabilities.

They work by combining traditional network scans of web servers with detailed probing of web applications using such techniques as sending known malicious input sequences and fuzzing in attempts to break the application.

- Nikto
- Arachni

Most organizations do use web application scanners, but they choose to use commercial products that offer advanced capabilities and user-friendly interfaces.

##

### Reviewing and Interpreting Scan Reports

Vulnerability scan reports provide analysts with a significant amount of information that assists with the interpretation of the report

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/a65279bd-677e-4bb1-9ee4-e45763331fb1)

The **name of the vulnerability**, which offers a descriptive title, and the **overall severity** of the vulnerability, expressed as a general category, such as low, medium, high, or critical

The report provides a **detailed description** of the flaws in the SSL protocol and explains that SSL is no longer considered acceptable for use

The report provides a **solution** to the vulnerability. When possible, the scanner offers detailed information about how system administrators, security professionals, network engineers, and/or application developers may correct the vulnerability

The scanner provides **references** where administrators can find more details on the vulnerability described in the report

The **output** section of the report shows the detailed information returned by the remote system when probed for the vulnerability. This information can be extremely valuable to an analyst because it often provides the verbatim output returned by a command. Analysts can use this to better understand why the scanner is reporting a vulnerability, identify the location of a vulnerability, and potentially identify false positive reports

The **port/hosts** section provides details on the server(s) that contain the vulnerability as well as the specific services on that server that have the vulnerability

The **vulnerability information** section provides some miscellaneous information about the vulnerability

The **risk information** section includes useful information for assessing the severity of the vulnerability

Provides details on how the vulnerability rates when using the Common Vulnerability Scoring System (CVSS)

##

### Understanding CVSS

**Common Vulnerability Scoring System (CVSS)** is an industry standard for assessing the severity of security vulnerabilities.

It provides a technique for scoring each vulnerability on a variety of measures. Cybersecurity analysts often use CVSS ratings to prioritize response actions.

Analysts scoring a new vulnerability begin by rating the vulnerability on eight different measures. Each measure is given both a descriptive rating and a numeric score. The first four measures evaluate the exploitability of the vulnerability, whereas the last three evaluate the impact of the vulnerability. The eighth metric discusses the scope of the vulnerability.

##

### Attack Vector Metric

Describes how an attacker would exploit the vulnerability

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/2e3b0041-9bba-4b89-96e2-8378ec64c944)

##

### Attack Complexity Metric

Describes the difficulty of exploiting the vulnerability

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/86a4da6e-3281-4c6f-b64d-2efdfe0cfed0)

##

### Privileges Required Metric

Describes the type of account access that an attacker would need to exploit a vulnerability

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/8d685a40-ce5a-43e3-8dc5-dc04f5327822)

##

### User Interaction Metric

Describes whether the attacker needs to involve another human in the attack

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/33d2c96b-0cad-4c3e-bd52-9a4ae56bb391)

##

### Confidentiality Metric

Describes the type of information disclosure that might occur if an attacker successfully exploits the vulnerability

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/9e0cbf52-d92d-4a29-8484-638fb4836f9c)

##

### Integrity Metric

Describes the type of information alteration that might occur if an attacker successfully exploits the vulnerability

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/b7f4aa6e-9be4-4d28-9b65-3cd991108dd4)

##

### Availability Metric

Describes the type of disruption that might occur if an attacker successfully exploits the vulnerability

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/ecca4b49-7084-4ba1-a539-908bebc59eb3)

##

### Scope Metric

Describes whether the vulnerability can affect system components beyond the scope of the vulnerability

The scope metric table does not contain score information. The value of the scope metric is reflected in the values for the privileges required metric.

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/2997f9c6-b332-485a-9b5f-4f9cf450f63e)

##

### Interpreting the CVSS Vector

The CVSS vector uses a single-line format to convey the ratings of a vulnerability on all six of the metrics described in the preceding sections.

    CVSS:3.0/AV:N/AC:L/PR:N/UI:N/S:U/C:H/I:N/A:N

This vector contains nine components. The first section, “CVSS:3.0,” simply informs the reader (human or system) that the vector was composed using CVSS version 3.

The next eight sections correspond to each of the eight CVSS metrics.

- Attack Vector: Network (score: 0.85)
- Attack Complexity: Low (score: 0.77)
- Privileges Required: None (score: 0.85)
- User Interaction: None (score: 0.85)
- Scope: Unchanged
- Confidentiality: High (score: 0.56)
- Integrity: None (score: 0.00)
- Availability: None (score: 0.00)

### Summarizing CVSS Scores

The CVSS vector provides good detailed information on the nature of the risk posed by a vulnerability, but the complexity of the vector makes it difficult to use in prioritization exercises

For this reason, analysts can calculate the **CVSS base score**, which is a single number representing the overall risk posed by the vulnerability. Arriving at the base score requires first calculating some other CVSS component scores.

##

### CALCULATING THE IMPACT SUB-SCORE (ISS)

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/5920d9ce-327e-405b-8702-4984fe2f2121)

##

### CALCULATING THE IMPACT SCORE

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/49ed5291-706c-41a5-ae80-4ce3ec7fa239)

##

### CALCULATING THE EXPLOITABILITY SCORE

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/963258eb-8c85-4538-a23c-d29afc5b0fb0)
![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/697b8bf1-b4f2-4835-b8b1-6be056bed160)

##

### CALCULATING THE BASE SCORE

determine the CVSS base score using the following rules: 

- If the impact is 0, the base score is 0.
- If the scope metric is Unchanged, calculate the base score by adding together the impact and exploitability scores. 
- If the scope metric is Changed, calculate the base score by adding together the impact and exploitability scores and multiplying the result by 1.08. The highest possible base score is 10.
- If the calculated value is greater than 10, set the base score to 10.

Add Impact score and exploitability score to get the base score

##

### CATEGORIZING CVSS BASE SCORES

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/381467b4-095b-409f-b54a-1788d1088e15)

## Validating Scan Results

Cybersecurity analysts interpreting reports often perform their own investigations to confirm the presence and severity of vulnerabilities. These investigations may include the use of external data sources that supply additional information valuable to the analysis.

### False Positives

When a scanner reports a vulnerability that does not exist, this is known as a **false positive error**B

The scanner might not have sufficient access to the target system to confirm a vulnerability, or it might simply have an error in a plug-in that generates an erroneous vulnerability report

When a vulnerability scanner reports a vulnerability, this is known as a **positive report**. This report may either be accurate (a **true positive** report) or inaccurate (a **false positive** report)

when a scanner reports that a vulnerability is not present, this is a **negative report**. The negative report may either be accurate (a **true negative** report) or inaccurate (a **false negative** report)

Cybersecurity analysts should confirm each vulnerability reported by a scanner

Analysts should draw on their own expertise as well as the subject matter expertise of others throughout the organization

##

### Reconciling Scan Results with Other Data Sources

Cybersecurity analysts interpreting these reports should also turn to other sources of security information as they perform their analysis.

Valuable information sources for this process include the following:

- **Log reviews** from servers, applications, network devices, and other sources that might contain information about possible attempts to exploit detected vulnerabilities
- **Security information and event management (SIEM)** systems that correlate log entries from multiple sources and provide actionable intelligence
- **Configuration management systems** that provide information on the operating system and applications installed on a system

## Security Vulnerabilities

Each vulnerability scanning system contains plug-ins able to detect thousands of possible vulnerabilities, ranging from major SQL injection flaws in web applications to more mundane information disclosure issues with network devices

Applying security patches to systems should be one of the core practices of any information security program, but this routine task is often neglected due to a lack of resources for preventive maintenance

One of the most common alerts from a vulnerability scan is that one or more systems on the network are running an outdated version of an operating system or application and require security patches

the importance of operating a **patch management** program that routinely patches security issues

##

### Patch Management

Applying security patches to systems should be one of the core practices of any information security program, but this routine task is often neglected due to a lack of resources for preventive maintenance.

One of the most common alerts from a vulnerability scan is that one or more systems on the network are running an outdated version of an operating system or application and require security patches.

##

### Legacy Platforms

Once they announce the final end of support for a product, organizations that continue running the outdated software put themselves at a significant risk of attack.

The vendor simply will not investigate or correct security flaws that arise in the product after that date. Organizations continuing to run the unsupported product are on their own from a security perspective, and unless you happen to maintain a team of operating system developers, that's not a good situation to find yourself in. 

The solution for organizations running unsupported operating systems is simple in its phrasing but complex in implementation.

In cases where the organization simply must continue using an unsupported operating system, best practice dictates isolating the system as much as possible, preferably not connecting it to any network, and applying as many compensating security controls as possible, such as increased monitoring and implementing strict network firewall rules.

## 

### Weak Configurations

- The use of default settings that pose a security risk, such as administrative setup pages that are meant to be disabled before moving a system to production.

- The presence of unsecured accounts, including both normal user account and unsecured root accounts with administrative privileges. Accounts may be considered unsecured when they either lack strong authentication or use default passwords.

- Open ports and services that are not necessary to support normal system operations. This will vary based on the function of a server or device but, in general, a system should expose only the minimum number of services necessary to carry out its function.

- Open permissions that allow users access that violates the principle of least privilege.

##

### Error Messages

Many application development platforms support debug modes that give developers crucial error information needed to troubleshoot applications in the development process.

Debug mode typically provides detailed information on the inner workings of an application and server, as well as supporting databases.

It can inadvertently assist an attacker seeking to gain information about the structure of a database, authentication mechanisms used by an application, or other details.

Vulnerability scans do alert on the presence of debug mode on scanned servers.

Solving this issue requires the cooperation of developers and disabling debug modes on systems with public exposure.

Software development should always take place in a dedicated development environment that is only accessible from private networks.

## 

### Insecure Protocols

Many of the older protocols used on networks in the early days of the Internet were designed without security in mind. 

They often failed to use encryption to protect usernames, passwords, and the content sent over an open network, exposing the users of the protocol to eavesdropping attacks

The solution for this issue is to simply switch to a more secure protocol

##

### Weak Encryption

Encryption is a crucial security control used in every cybersecurity program to protect stored data and data in transit over networks.

When you implement encryption, you have two important choices to make:

- The algorithm to use to perform encryption and decryption
- The encryption key to use with that algorithm

## Penetration Testing

Seeks to bridge the gap between the rote use of technical tools to test an organization's security and the power of those tools when placed in the hands of a skilled and determined attacker

Authorized, legal attempts to defeat an organization's security controls and perform unauthorized activities

Time-consuming and require staff who are equally skilled and determined as the real-world attackers that will attempt to compromise the organization

Most effective way for an organization to gain a complete picture of their security vulnerability

Penetration testing provides us with knowledge that we can't obtain elsewhere

We learn whether an attacker with the same knowledge, skills, and information as our testers would likely be able to penetrate our defenses

In the event that attackers are successful, penetration testing provides us with an important blueprint for remediation

Cybersecurity professionals can trace the actions of the testers as they progressed through the different stages of the attack and close the series of open doors that the testers passed through

Penetration tests can provide us with essential, focused information on specific attack targets

These focused tests can drill into the defenses around a specific target and provide actionable insight that can prevent a vulnerability from initial exposure

##

### Adopting the Hacker Mindset

Think like the adversary who might attack the system in the real world

You might build a system of security controls that seeks to prevent those threats from materializing. 

These controls might include the following:

- Security cameras in high-risk areas
- Auditing of cash register receipts
- Theft detectors at the main entrance/exit to the store
- Exit alarms on emergency exits
- Burglar alarm wired to detect the opening of doors outside business hours

Examine each one of these security controls and assess its ability to prevent each of the threats identified in your initial risk assessment. You'd also look for gaps in the existing security controls that might require supplementation

Cybersecurity professionals need to win every time; attackers need to win only once

##

### Reasons for Penetration Testing

Provides us with visibility into the organization's security posture that simply isn't available by other means.

Penetration testers bring their unique skills and perspective to the table and can take the output of security tools and place them within the attacker's mindset, asking the question, “If I were an attacker, how could I use this information to my advantage?”

##

### Benefits of Penetration Testing

Penetration testing provides us with knowledge that we can't obtain elsewhere. By conducting thorough penetration tests, we learn whether an attacker with the same knowledge, skills,and information as our testers would likely be able to penetrate our defenses.

If they can't gain a foothold, we can then be reasonably confident that our networks are secure against attack by an equivalently talented attacker under the present circumstances.

In the event that attackers are successful, penetration testing provides us with an important blueprint for remediation.

penetration tests can provide us with essential, focused information on specific attack targets.

Focused tests can drill into the defenses around a specific target and provide actionable insight that can prevent a vulnerability from initial exposure.

##

### Threat Hunting 

Search the organization's technology infrastructure for the artifacts of a successful attack

“Presumption of compromise” - assumes that attackers have already successfully breached an organization and searches out the evidence of successful attacks

When threat hunters discover a potential compromise, incident handling mode, seeking to contain, eradicate, and recover from the compromise.

Conduct a postmortem analysis of the factors that contributed to the compromise in an effort to remediate deficiencies. This post-event remediation is another similarity between penetration testing and threat hunting: organizations leverage the output of both processes in similar ways

Threat hunters work with a variety of intelligence sources, using the concept of intelligence fusion to combine information from threat feeds, security advisories and bulletins, and other sources

##

### Penetration Test Types

Three typical classifications are used to describe this:

- White-Box Tests, known environment tests, tests performed with full knowledge of the underlying technology, configurations, and settings that make up the target

Testers will typically have such information as network diagrams, lists of systems and IP network ranges, and even credentials to the systems they are testing 

Allow for effective testing of systems without requiring testers to spend time identifying targets and determining which may be a way in often more complete, since testers can get to every system, service, or other target that is in scope, and will have credentials and other materials that will allow them to be tested
	
May not provide an accurate view of what an external attacker would see, and controls that would have been effective against most attackers may be bypassed

- Black-Box Tests, unknown environment tests, intended to replicate what an attacker would encounter

Testers are not provided with access to or information about an environment, and instead, they must gather information, discover vulnerabilities, and make their way through an infrastructure or systems like an attacker would can be time-consuming, but it can help provide a reasonably accurate assessment of how secure the target is against an attacker of similar or lesser skill. If the threat actor you expect to target your organization is more capable, a black-box tester can't provide you with a realistic view of what they could do
	
- Gray-box tests, partially known environment, test may provide some information about the environment to the penetration testers without giving full access, credentials, or configuration detail.

Can help focus penetration testers time and effort while also providing a more accurate view of what an attacker would actually encounter

##

### Rules of Engagement

Key elements include the following:

- The timeline for the engagement and when testing can be conducted

Some assessments will intentionally be scheduled for noncritical timeframes to minimize the impact of potential service outages, whereas others may be scheduled during normal business hours to help test the organization's reaction to attacks
	
- What locations, systems, applications, or other potential targets are included or excluded

includes discussions about third-party service providers that may be impacted by the test, such as Internet services providers, software-as-a-service or other cloud service providers, or outsourced security monitoring services
	
- Data handling requirements for information gathered during the penetration test

Important when engagements cover sensitive organizational data or systems. Requirements for handling often include confidentiality requirements for the findings, such as encrypting data during and after the test, and contractual requirements for disposing of the penetration test data and results after the engagement is over
	
- What behaviors to expect from the target. Defensive behaviors like shunning, blacklisting, or other active defenses may limit the value of a penetration test

If the test is meant to evaluate defenses, this may be useful. If the test is meant to test a complete infrastructure, shunning or blocking the penetration testing team's efforts can waste time and resources
	
- What resources are committed to the test

In white- and gray-box testing scenarios, time commitments from the administrators, developers, and other experts on the targets of the test are not only useful, they can be necessary for an effective test
	
- Legal concerns should also be addressed, including a review of the laws that cover the target organization, any remote locations, and any service providers who will be in scope
	
- When and how communications will occur

Should the engagement include daily or weekly updates regardless of progress, or will the penetration testers simply report when they are done with their work? How should the testers respond if they discover evidence of a current compromise?
	
Problem handling and resolution is another key element of the rules of engagement

Having a clearly defined communication, notification, and escalation path on both sides of the engagement can help minimize downtime and other issues for the target organization

Penetration testers should carefully document their responsibilities and limitations of liability, and ensure that clients know what could go wrong and that both sides agree on how it should be handled

## 

### Reconnaissance

Passive reconnaissance techniques seek to gather information without directly engaging with the target.

Active reconnaissance techniques directly engage the target in intelligence gathering. These techniques include the use of port scanning to identify open ports on systems, **footprinting** to identify the operating systems and applications in use, and vulnerability scanning to identify exploitable vulnerabilities.

Testers use a technique called **war driving**, where they drive by facilities in a car equipped with high-end antennas and attempt to eavesdrop on or connect to wireless networks

Recently, testers have expanded this approach to the use of drones and unmanned aerial vehicles (UAVs) in a technique known as **war flying**

##

### Running the Test

Initial access occurs when the attacker exploits a vulnerability to gain access to the organization's network.

Privilege escalation uses hacking techniques to shift from the initial access gained by the attacker to more advanced privileges, such as root access on the same system.

Pivoting, or lateral movement, occurs as the attacker uses the initial system compromise to gain access to other systems on the target network.

Attackers establish persistence on compromised networks by installing backdoors and using other mechanisms that will allow them to regain access to the network, even if the initial vulnerability is patched.

Exploitation frameworks, such as Metasploit, simplify the use of vulnerabilities by providing a modular approach to configuring and deploying vulnerability exploits.

##

### Cleaning Up

The testers conduct close-out activities that include presenting their results to management and cleaning up the traces of their work. 

Testers should remove any tools that they installed on systems as well as any persistence mechanisms that they put in place. 

The close-out report should provide the target with details on the vulnerabilities discovered during the test and advice on improving the organization's cybersecurity posture.

##

### Training and Exercises

When conducting an exercise, participants are often divided into
three teams:

- Red team members are the attackers who attempt to gain access to systems.

- Blue team members are the defenders who must secure systems and networks from attack. The blue team also monitors the environment during the exercise, conducting active defense techniques. The blue team commonly gets a head start with some time to secure systems before the attack phase of the exercise begins.

- White team members are the observers and judges. They serve as referees to settle disputes over the rules and watch the exercise to document lessons learned from the test. The white team is able to observe the activities of both the red and blue teams and is also responsible for ensuring that the exercise does not cause production issues.

- Purple Teaming is a combination of knowledge from the red and blue teams. bring the red and the blue teams together to share information about tactics and lessons learned. Each team walks the other through their role in the exercise, helping everyone learn from the process.

**Tabletop exercises** simply gather participants in the same room to walk through their response to a fictitious exercise scenario.
