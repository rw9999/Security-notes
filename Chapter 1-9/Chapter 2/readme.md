# Cybersecurity Threat Landscape

### Classifying Cybersecurity Threats

Characteristics to keep in mind:

Internal vs. External

Level of Sophistication/Capability

Resources/Funding

Intent/Motivation

**White-hat hackers** - known as authorized attackers, are those who act with authorization and seek to discover security vulnerabilities with the intent of correcting them

**Black-Hat Hackers** - known as unauthorized attackers, are those with malicious intent

**Gray-Hat Hackers** - known as semi-authorized attackers, are those who fall somewhere between white- and black-hat hackers. They act without proper authorization, but they do so with the intent of informing their targets of any security vulnerabilities

##

### Threat Actors

**Script Kiddies** - a derogatory term for people who use hacking techniques but have limited skills

- rely on automated tools from the internet
- often have little knowledge of how their attack work, seek convenient targets
- plentiful and unfocused
- young, work alone, lack of resources

**Hacktivists** - use hacking techniques to accomplish some activist goal

- might attack a network due to some political issue or a company whose policies they disagree with
- believe they are motivated by the greater good, even if their activity violates the law
- risk getting caught to accomplish their goals
- skill levels of hacktivists vary widely
- resources of hacktivists also vary somewhat

**Criminal Syndicates** - motive is simply illegal financial gain and often prefer to remain in the shadows, drawing as little attention to themselves as possible

- Organized crime tends to have attackers who range from moderately skilled to highly skilled
- tend to have more resources, both in terms of time and money, than do hacktivists or script kiddies
- willing to invest in their criminal enterprises in the hopes of yielding a significant return on their investments

2019 Internet Organized Crime Threat Assessment (IOCTA), the European Union Agency for Law Enforcement Cooperation (EUROPOL) found that organized crime groups were active in a variety of cybercrime categories including the following:

- Cyber-dependent crime
- Child sexual exploitation
- Payment fraud
- Dark web
- Terrorism
- Cross-cutting crime factors

### Advanced Persistent Threats

use advanced techniques, not simply tools downloaded from the Internet

the attacks are persistent, occurring over a significant period of time.

**Nation-state attacks** - They tend to be characterized by highly skilled attackers with significant resources. A nation has the labor force, time, and money to finance ongoing, sophisticated attacks

The motive can be political or economic. In some cases, the attack is done for traditional espionage goals: to gather information about the target's defense capabilities. In other cases, the attack might be targeting intellectual property or other economic assets

**Zero-day attacks ** - vulnerabilities that are not known to other attackers or cybersecurity teams. After they uncover a vulnerability, they do not disclose it but rather store it in a vulnerability repository for later use

unknown to product vendors, and therefore, no patches are available to correct them

### Insiders

**Insider attacks** - occur when an employee, contractor, vendor, or other individual with authorized access to information and systems uses that access to wage an attack against the organization

aimed at disclosing confidential information, but insiders may also seek to alter information or disrupt business processes

- might be of any skill level
- differing motivations behind their attacks
- usually working alone and have limited financial resources and time
- automatic advantage/might have significant access and knowledge

Cybersecurity teams should work with human resources partners to identify insiders exhibiting unusual behavior and intervene before the situation escalates.

**Shadow IT** - where individuals and groups seek out their own technology solutions

puts sensitive information in the hands of vendors outside of the organization's control

### Competitors

May engage in corporate espionage designed to steal sensitive information from your organization and use it for their own business advantage

##

### Threat Vectors

means that threat actors use to obtain that access

**Email and Social Media**
- most commonly exploited threat vectors

Phishing messages, spam messages, and other email-borne attacks are a simple way to gain access to an organization's network

Attackers might directly target users on social media, or they might use social media in an effort to harvest information about users that may be used in another type of attack

**Direct Access** - may seek to gain direct access to an organization's network by physically entering the organization's facilities

Most common ways they do this is by entering public areas of a facility, such as a lobby, customer store, or other easily accessible location and sitting and working on their laptops, which are surreptitiously connected to unsecured network jacks on the wall
 
Attackers who gain physical access to a facility may be able to find an unsecured computer terminal, network device, or other system

**Wireless Networks** - offer an even easier path onto an organization's network

**Removable Media** - Attackers also commonly use removable media, such as USB drives, to spread malware and launch their attacks

**Cloud** - Attackers routinely scan popular cloud services for files with improper access controls, systems that have security flaws, or accidentally published API keys and passwords.

Vulnerabilities facing organizations operating in cloud environments bear similarities to those found in on-premises environments, but the controls often differ

**Third-Party Risks** -  attackers may attempt to interfere with an organization's IT supply chain, gaining access to devices at the manufacturer or while the devices are in transit from the manufacturer to the end user

##

### Threat Data and Intelligence

the set of activities and resources available to cybersecurity professionals seeking to learn about changes in the threat environment

Threat intelligence information can also be used for **predictive analysis** to identify likely risks to the organization

Many sources of threat intelligence, ranging from open-source intelligence (OSINT) that you can gather from publicly available sources, to commercial services that provide proprietary or closed-source intelligence information

Threat feeds often include technical details about threats, such as IP addresses, hostnames and domains, email addresses, URLs, file hashes, file paths, CVE numbers, and other details about a threat.

**Vulnerability databases** are also an essential part of an organization's threat intelligence program. Reports of vulnerabilities certainly help direct an organization's defensive efforts, but they also provide valuable insight into the types of exploit being discovered by researchers.

Threat intelligence sources may also provide **indicators of compromise (IoCs)**. These are the telltale signs that an attack has taken place and may include file signatures, log patterns, and other evidence left behind by attackers. IoCs may also be found in file and code repositories that offer threat intelligence information.

**Open Source Intelligence** - threat intelligence that is acquired from publicly available sources

Many government and public sources of threat intelligence data

**Dark Web ** - a network run over standard Internet connections but using multiple layers of encryption to provide anonymous communication

**Closed-source intelligence** -  Commercial security vendors, government organizations, and other security-centric organizations do their own information gathering and research, and they may use custom tools, analysis models, or other proprietary methods to gather, curate, and maintain their threat feeds.

Threat maps provide a geographic view of threat intelligence

##

### Assessing Threat Intelligence

1. Is it timely? A feed that is operating on delay can cause you to miss a threat, or to react after the threat is no longer relevant.
	
2. Is the information accurate? Can you rely on what it says, and how likely is it that the assessment is valid? Does it rely on a single source or multiple sources? How often are those sources correct? 
	
3. Is the information relevant? If it describes the wrong platform, software, or reason for the organization to be targeted, the data may be very timely, very accurate, and completely irrelevant to your organization
   
![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/ad2f215a-1f95-49dd-b434-d170ae6554d4)

##

### Threat Indicator Management and Exchange

Managing threat information at any scale requires standardization and tooling to allow the threat information to be processed and used in automated ways

**Structured Threat Information eXpression (STIX)** -  an XML language originally sponsored by the U.S. Department of Homeland Security

STIX 2.0 defines 12 STIX domain objects, including things like attack patterns, identities, malware, threat actors, and tools. These objects are then related to each other by one of two STIX relationship object models: either as a relationship or a sighting. STIX has been handed off to the Organization for the Advancement of Structured Information Standards (OASIS)

A companion to STIX is the **Trusted Automated eXchange of Indicator Information (TAXII)** protocol. TAXII is intended to allow cyber threat information to be communicated at the application layer via HTTPS. TAXII is specifically designed to support STIX data exchange

**Open Indicators of Compromise (OpenIOC)** is an XML-based framework that was developed by Mandiant, and it uses Mandiant's indicators for its base framework. A typical IOC includes metadata like the author, the name of the IOC, and a description of the indicator

**Information Sharing and Analysis Centers (ISACs)** help infrastructure owners and operators share threat information and provide tools and assistance to their members

##

### Conducting Your Own Research

- Vendor security information websites
	
- Vulnerability and threat feeds from vendors, government agencies, and private organizations
	
- Academic journals and technical publications, such as Internet Request for Comments (RFC) documents. RFC documents are particularly informative because they contain the detailed technical specifications for Internet protocol
	
- Professional conferences and local industry group meetings
	
- Social media accounts of prominent security professionals

Keep a particular eye out for information on adversary tactics, techniques, and procedures (TTPs)

