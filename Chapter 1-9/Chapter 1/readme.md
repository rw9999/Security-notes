# Chapter 1
### CIA Triad

_Main goals of Cybersecurity_

**Confidentiality** - ensures that unauthorized individuals are not able to gain access to sensitive information

&emsp;&emsp;i.e. firewalls, access control lists, and encryption

**Integrity** - ensures that there are no unauthorized modifications to information or systems

&emsp;&emsp;i.e. hashing and monitoring solutions

**Availability** - ensures that information and system are ready to meet the needs of legitimate users at the time those users request them

&emsp;&emsp;i.e fault tolerance, clustering, and backup

##

### DAD Triad

_Key Threats to Cybersecurity_

**Disclosure** - the exposure of sensitive information to unauthorized individuals, known as **_data loss_**

&emsp;&emsp;i.e. Attackers who gain access to sensitive information and remove it from the organization are said to be performing data exfiltration 

**Alteration** - the unauthorized modification of information

&emsp;&emsp;i.e. Attackers may seek to modify records contained in a system for financial gain, such as adding fraudulent transactions to a financial account. Alteration may occur as the result of natural activity, such as a power surge causing a “bit flip” that modifies stored data. Accidental alteration is also a possibility if users unintentionally modify information stored in a critical system as the result of a typo or other unintended activity.

**Denial** - the unintended disruption of an authorized user's legitimate access to information

&emsp;&emsp;i.e. availability loss may be intentional, such as when an attacker launches a distributed denial-of-service (DDoS) attack against a website. Denial may also occur as the result of accidental activity, such as the failure of a critical server, or as the result of natural activity, such as a natural disaster impacting a communications circuit

##

### Breach Impact

**_Security incidents_** occur when an organization experiences a breach of the confidentiality, integrity, and/or availability of information or information systems. Security professionals are responsible for understanding these risks and implementing controls designed to manage those risks to an acceptable level. They must understand the effects that a breach might have on the organization and the impact it might have on an ongoing basis

**Financial Risk** - the risk of monetary damage to the organization as the result of a data breach

**Reputational Risk** - occurs when the negative publicity surrounding a security breach causes the loss of goodwill among customers, employees, suppliers, and other stakeholders

**Strategic Risk** - the risk that an organization will become less effective in meeting its major goals and objectives as a result of the breach

**Operational Risk** - risk to the organization's ability to carry out its day-to-day functions

**Compliance Risk** - occurs when a security breach causes an organization to run afoul of legal or regulatory requirements

>[!NOTE]
Risks can often cross categories

##

### Security Control Categories

**Technical Controls** - enforce confidentiality, integrity, and availability in the digital space

&emsp;&emsp;i.e. firewall rules, access control lists, intrusion prevention systems, and encryption

**Operational Controls** - the processes that we put in place to manage technology in a secure manner

&emsp;&emsp;i.e. access reviews, log monitoring, and vulnerability management

**Managerial controls** - procedural mechanisms that focus on the mechanics of the risk management process

&emsp;&emsp;i.e. periodic risk assessments, security planning exercises, and the incorporation of security into the organization's change management, service acquisition, and project management practices

##

### Security Control Types

**Preventitive Controls** - intend to stop a security issue before it occurs 

&emsp;&emsp;i.e. firewalls and encryption

**Detective Controls** - identify security events that have already occurred

&emsp;&emsp;i.e. intrusion detection systems (ids)

**Corrective controls** - remediate security issues that have already occurred

&emsp;&emsp;i.e. restoring backups after a ransomware attack

**Deterrent controls** - seek to prevent an attacker from attempting to violate security policies

&emsp;&emsp;i.e. vicious guard dogs and barbed wire fences

**Physical controls** - security controls that impact the physical world

&emsp;&emsp;i.e. fences, perimeter lighting, locks, fire suppression systems, and burglar alarms

**Compensating controls** - controls designed to mitigate the risk associated with exceptions made to a security policy

##

### Data Protection

**Data at rest** - stored data that resides on hard drives, tapes, in the cloud, or on other storage media

**Data in motion** - data that is in transit over a network

**Data in processing** - data that is actively in use by a computer system. includes the data stored in memory while processing takes place

<ins>Data Encryption<ins>

**Encryption** technology uses mathematical algorithms to protect information from prying eyes, both while it is in transit over a network and while it resides in systems

##

### Data Loss Prevention

Data loss prevention (DLP) systems help organizations enforce information handling policies and procedures to prevent data loss and theft. They search systems for stores of sensitive information that might be unsecured and monitor network traffic for potential attempts to remove sensitive information from the organization. They can act quickly to block the transmission before damage is done and alert administrators to the attempted breach

**Host-based DLP** - uses software agents installed on systems that search those systems for the presence of sensitive information. Detecting the presence of stored sensitive information allows security professionals to take prompt action to either remove it or secure it with encryption

can also monitor system configuration and user actions, blocking undesirable actions

**Network DLP** - dedicated devices that sit on the network and monitor outbound network traffic, watching for any transmissions that contain unencrypted sensitive information. They can then block those transmissions, preventing the unsecured loss of sensitive information

DLP systems may simply block traffic that violates the organization's policy, or in some cases, they may automatically apply encryption to the content

DLP systems also have two mechanisms of action:

- **Pattern matching** - they watch for the telltale signs of sensitive information

&emsp;&emsp;i.e. a number that is formatted like a credit card or Social Security number

- **Watermarking** - systems or administrators apply electronic tags to sensitive documents and then the DLP system can monitor systems and networks for unencrypted content containing those tags

&emsp;&emsp;i.e. used in digital rights management (DRM) solutions that enforce copyright and data ownership restrictions

##

### Data Minimization

Seeks to reduce risk by reducing the amount of sensitive information that we maintain on a regular basis

The best way to achieve data minimization is to simply destroy data when it is no longer necessary to meet our original business purpose

If we can't completely remove data from a dataset, we can often transform it into a format where the original sensitive information is de-identified. The **de-identification** process removes the ability to link data back to an individual, reducing its sensitivity

**Data Obfuscation**

- **Hashing** - uses a hash function to transform a value in our dataset to a corresponding hash value

If someone has a list of possible values for a field, they can conduct something called a **rainbow table attack**. In this attack, the attacker computes the hashes of those candidate values and then checks to see if those hashes exist in our data file

- **Tokenization** - replaces sensitive value with a unique identifier using a lookup table

i.e. replace a widely known value, such as a student ID, with a randomly generated 10-digit number. We'd then maintain a lookup table that allows us to convert those back to student IDs if we need to determine someone's identity. Need to keep the lookup table secure

- **Masking** - partially redacts sensitive information by replacing some or all sensitive fields with blank characters

i.e. might replace all but the last four digits of a credit card number with X's or *'s to render the card number unreadable
