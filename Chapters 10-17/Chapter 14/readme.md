# Incident Response

When things go wrong, organizations need a way to respond to incidents to ensure that their impact is limited and that normal operations can resume as quickly as possible. 

That means you need to know how to identify an incident given a series of events or data points, how to contain the incident, and then what to do about it

No matter how strong an organization's security protections are, eventually something will go wrong. Whether that involves a direct attack by a malicious actor, malicious software, an insider threat, or even just a simple mistake, a security incident is an eventuality for all organizations.

Organizations therefore need an incident response (IR) plan, process, and team, as well as the technology, skills, and training to respond appropriately.

A strong incident response process is not just a one-time action or something that is applied only in emergencies. Instead, IR is an ongoing process that improves organizational security using information that is learned from each security incident.

Although individual organizations may define them differently, in general an **incident** is a violation of the organization's policies and procedures or security practices.

**Events**, on the other hand, are an observable occurrence, which means that there are many events, few of which are likely to be incidents.

#

### The Incident Response Process

The first step toward a mature incident response capability for most organizations is to understand the incident response process and what happens at each stage. Although organizations may use slightly different labels or steps and the number of steps may vary, the basic concepts remain the same.

Organizations must prepare for incidents, identify incidents when they occur, and then contain and remove the artifacts of the incident.

Once the incident has been contained, the organization can work to recover and return to normal, and then make sure that the lessons learned from the incident are baked into the preparation for the next time something occurs.


![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/d78f1562-46b5-4c7a-81a8-b5fb8ef0e24f)

The six steps you will need to know for the Security+ exam are as follows:

1. **Preparation.** In this phase, you build the tools, processes, and procedures to respond to an incident. That includes building and training an incident response team, conducting exercises, documenting what you will do and how you will respond, and acquiring, configuring, and operating security tools and incident response capabilities.

2. **Identification.** This phase involves reviewing events to identify incidents. You must pay attention to indicators of compromise, use log analysis and security monitoring capabilities, and have a comprehensive awareness and reporting program for your staff.

3. **Containment.** Once an incident has been identified, the incident response team needs to contain it to prevent further issues or damage. Containment can be challenging and may not be complete if elements of the incident are not identified in the initial identification efforts.

4. **Eradication.** The eradication stage involves removing the artifacts associated with the incident. In many cases, that will involve rebuilding or restoring systems and applications from backups rather than simply removing tools from a system since proving that a system has been fully cleaned can be very difficult. Complete eradication and verification is crucial to ensuring that an incident is over.

5. **Recovery.** Restoration to normal is the heart of the recovery phase. That may mean bringing systems or services back online  or other actions that are part of a return to operations. Recovery requires eradication to be successful, but it also involves implementing fixes to ensure that whatever security weakness, flaw, or action that allowed the incident to occur has been remediated to prevent the event from immediately reoccurring.

6. **Lessons learned.** These are important to ensure that organizations improve and do not make the same mistakes again. They may be as simple as patching systems or as complex as needing to redesign permission structures and operational procedures. Lessons learned are then used to inform the preparation process, and the cycle continues.

Although this list may make it appear as if incidents always proceed in a linear fashion from item to item, many incidents will move back and forth between stages as additional discoveries are made or as additional actions are taken by malicious actors.

So, you need to remain nimble and understand that you may not be in the phase you think you are, or that you need to operate in multiple phases at once as you deal with components of an incident—or multiple incidents at once.

#

### Preparing for Incident Response

The next step after understanding and defining an organization's IR process is to determine who will be on the organization's IR team, who will be in charge of the IR process, and who will lead the IR team. Next, plans are built, and then the plans are tested via exercises.

#

### Incident Response Team

Building an IR team involves finding the right members for the team.

Typical teams often include the following:

- A member of management or organizational leadership. This individual will be responsible for making decisions for the team and will act as a primary conduit to senior management for the organization. Ideally, teams should have a leader with enough seniority to make decisions for the organization in an emergency.

- Information security staff members are likely to make up the core of the team and will bring the specialized IR and analysis skills needed for the process. Since containment often requires immediate action using security tools like firewalls, intrusion prevention systems, and other security tools, the information security team can also help speed up the IR process.

- The team will need technical experts such as systems administrators, developers, or others from disciplines throughout the organization. The composition of the IR team may vary depending on the nature of the incident, and not all technical experts may be pulled in for every incident. Knowing the systems, software, and architecture can make a huge difference in the IR process, and familiarity can also help responders find unexpected artifacts that might be missed by someone who does not work with a specific system every day.

- Communications and public relations staff are important to help make sure that internal and external communications are handled well. Poor communications—or worse, no communications—can make incidents worse or severely damage an organization's reputation.

- Legal and human relations (HR) staff may be involved in some, but not all, incidents. Legal counsel can advise on legal issues, contracts, and similar matters. HR may be needed if staff were involved, particularly if the incident involves an insider or is an HR-related investigation.

- Law enforcement is sometimes added to a team, but in most cases only when specific issues or attacks require their involvement.

Regardless of the specific composition of your organization's team, you will also need to ensure that team members have proper training. That may mean IR training for security professionals and technical staff, or it could include exercises and practice for the entire team as a group to ensure that they are ready to work together.

#

### Exercises

There are three major types of exercises that incident response teams use to prepare:

- **Tabletop exercises** are used to talk through processes. Team members are given a scenario and are asked questions about how they would respond, what issues might arise, and what they would need to do to accomplish the tasks they are assigned in the IR plan. Tabletop exercises can resemble a brainstorming session as team members think through a scenario and document improvements in their responses and the overall IR plan.

- **Walk-throughs** take a team through an incident step by step. This exercise can help ensure that team members know their roles as well as the IR process, and that the tools, access, and other items needed to respond are available and accessible to them. A walk-through is an excellent way to ensure that teams respond as they should without the overhead of a full simulation.

- **Simulations** can include a variety of types of event. Exercises may simulate individual functions or elements of the plan, or only target specific parts of an organization. They can also be done at full scale, involving the entire organization in the exercise. It is important to plan and execute simulations in a way that ensures that all participants know that they are engaged in an exercise so that no actions are taken outside of the exercise environment.

When you conduct an exercise, start every call, text, or email with “This is an exercise” or a similar cue to let the person who is responding know that they should not take actual action. 

Of course, doing so can lead to biases and incorrect estimates on what effort or time would be required to perform an action or response. 

In most cases, keeping exercises properly under control is more important than detailed testing. 

In those cases where specific performance is needed, you may want to ensure that the person has a script or can perform a task that is scoped and limited to the needs of the simulation without causing problems or issues with normal operations.

#

### Building Incident Response Plans

Incident response plans can include several subplans to handle various stages of the response process.

Your organization may choose to combine them all into a single larger document or may break them out to allow the response team to select the components that they need.

Individual plans may also be managed or run by different teams.

Regardless of the structure of your response plans, they need to be regularly reviewed and tested.

A plan that is out of date, or that the team is not familiar with, can be just as much of a problem as not having a plan at all.

- **Communication plans** are critical to incident response processes.

A lack of communication, incorrect communication, or just poor communication can cause significant issues for an organization and its ability to conduct business. 

At the same time, problematic communications can also make incidents worse, as individuals may not know what is going on or may take undesired actions, thinking they are doing the right thing due to a lack of information or with bad or partial information available to them. 

Because of the importance of getting communication right, communication plans may also need to list roles, such as who should communicate with the press or media, who will handle specific stakeholders, and who makes the final call on the tone or content of the communications.

- **Stakeholder management** plans are related to communication plans and focus on groups and individuals who have an interest or role in the systems, organizations, or services that are impacted by an incident.

Stakeholders can be internal or external to an organization and may have different roles and expectations that need to be called out and addressed in the stakeholder management plan. 

Many stakeholder management plans will help with prioritization of which stakeholders will receive communications, what support they may need, and how they will be provided, with options to offer input or otherwise interact with the IR process, communications and support staff, or others involved in the response process.

- **Business continuity (BC)** plans focus on keeping an organization functional when misfortune or incidents occur.

In the context of IR processes, BC plans may be used to ensure that systems or services that are impacted by an incident can continue to function despite any changes required by the IR process.

That might involve ways to restore or offload the services or use of alternate systems.

Business continuity plans have a significant role to play for larger incidents, whereas smaller incidents may not impact an organization's ability to conduct business in a significant way.

- **Disaster recovery (DR)** plans define the processes and procedures that an organization will take when a disaster occurs.

Unlike a business continuity plan, a DR plan focuses on natural and man-made disasters that may destroy facilities, infrastructure, or otherwise prevent an organization from functioning normally. 

A DR plan focuses on restoration or continuation of services despite a disaster.

In addition to these types of plans, **continuity of operation planning (COOP)** is a federally sponsored program in the United States that is part of the national continuity program. COOP defines the requirements that government agencies need to meet to ensure that continuity of operations can be ensured.

Those requirements include how they will ensure their essential functions, the order of succession for the organization so that staff know who will be in charge and who will perform necessary functions, how authority will be delegated, how disaster recovery can function using continuity facilities, and a variety of other requirements.

COOP defines how federal agencies build a complete disaster recovery and business continuity plan.

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/36e2cd15-7529-4012-abb0-eea0b3deb461)

The four phases of the Continuity of Operations as defined by the Federal Emergency Management Agency (FEMA) as part of COOP.

#

### Policies

Organizations define policies as formal statements about organizational intent.

In short, they explain why an organization wishes to operate in a certain way, and they define things like the purpose or objective of an activity or program.

**Incident response policies** are commonly defined as part of building an IR capability. Well-written incident response policies will include important components of the IR process.

They will identify the team and the authority that the team operates under.

They will also require the creation and maintenance of incident handling and response procedures and practices, and they may define the overall IR process used by the organization.

In some cases, they may also have specific communication or compliance requirements that are included in the overall policy based on organizational needs.

It helps to bear in mind that a policy is a high-level statement of management intent that is used to convey the organization's expectations and direction for a topic.

Standards will then point to a policy for their authority, while providing specific guidance about what should be done.

Procedures are then used to implement standards or to guide how a task is done.

Policies tend to be slow to change, whereas standards change more frequently, and procedures and guidelines may be updated frequently to handle organizational needs or technology change, or for other business-related reasons.

An IR policy isn't the only policy that your organization may rely on to have a complete incident response capability. In fact, organizations often have many IT policies that can impact response.

A **retention policy** determines how long you keep data and how it will be disposed of. 

A retention policy is important to incident responders since it may determine how long the organization keeps incident data, how long logs will be available, and what data is likely to have been retained and thus may have been exposed if a system or data store is compromised or exposed.

#

### Attack Frameworks and Identifying Attacks

Incident responders frequently need ways to describe attacks and incidents using common language and terminology.

Attack frameworks are used to understand adversaries, document techniques, and to categorize tactics.

As you review frameworks like these, consider how you would apply them as part of an incident response process.

For example, if you find an attack tool as part of an incident response effort, what would consider that tool via the Diamond model lead you to? What information might you seek next, and why?

#

### MITRE ATT&CK

MITRE provides the ATT&CK, or Adversarial Tactics, Techniques, and Common Knowledge, a knowledgebase of adversary tactics and techniques.

The ATT&CK matrices includes detailed descriptions, definitions, and examples for the complete threat lifecycle from initial access through execution, persistence, privilege escalation, and exfiltration. At each level, it lists techniques and components, allowing threat assessment modeling to leverage common descriptions and knowledge.

ATT&CK matrices include pre-attack, enterprise matrices focusing on Windows, macOS, Linux, and cloud computing, as well as iOS and Android mobile platforms.

It also includes details of mitigations,threat actor groups, software, and a host of other useful details. All of this adds up to make ATT&CK the most comprehensive freely available database of adversary techniques, tactics, and related information that the authors of this book are aware of.

The ATT&CK framework is the most popular of the three models discussed here and has broad support in a variety of security tools, which means that analysts are most likely to find ATT&CK-related concepts, labels, and tools in their organizations.

#

### The Diamond Model of Intrusion Analysis

The Diamond Model of Intrusion Analysis describes a sequence where an adversary deploys a capability targeted at an infrastructure against a victim.

In this model, activities are called events, and analysts label the vertices as events are detected or discovered.

The model is intended to help analysts discover more information by highlighting the relationship between elements by following the edges between the events.

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/5559387d-4b16-4e27-ae9e-c6e596d8713d)

The Diamond Model uses a number of specific terms:

- **Core Features** for an event, which are the adversary, capability, infrastructure, and victim (the vertices of the diamond)

- **The Meta-Features**, which are start and end timestamps, phase, result, direction, methodology, and resources, which are used to order events in a sequence known as an activity thread, as well as for grouping events based on their features

- A **Confidence Value**, which is undefined by the model but that analysts are expected to determine based on their own work

The Diamond Model focuses heavily on understanding the attacker and their motivations, and then uses relationships between these elements to allow defenders to both understand the threat and think about what other data or information they may need to obtain or may already have available.

#

### The Cyber Kill Chain

Lockheed Martin's Cyber Kill Chain is a seven-step process.

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/71db8b9c-60b2-4bdb-ad06-d5be61662c53)

Here are the seven stages of the Cyber Kill Chain:

**Reconnaissance**

This stage identifies targets. Adversaries are planning their attacks and will gather intelligence about the target, including both open source intelligence and direct acquisition of target data via scanning.

Defenders must gather data about reconnaissance activities and prioritize defenses based on that information.

**Weaponization**

This stage involves building or otherwise acquiring a weaponizer, which combines malware and an exploit into a payload that can be delivered to the target. This may require creating decoy documents, choosing the right  command-and-control (C2) tool, and other details. The model emphasizes the fact that defenders need to conduct full malware analysis in this stage to understand not only what payload is dropped but also how the weaponized exploit was made. 

Defenders should also build detections for weaponizers, look at the timeline of when malware was created versus its use, and collect both files and metadata to help them see if the tools are widely shared or closely held and thus potentially very narrowly targeted.

**Delivery**

This stage occurs when the adversary deploys their tool either directly against targets or via a release that relies on staff at the target interacting with it, such as in an email payload, on a USB stick, or via websites that they visit. 

Defenders in this stage must observe how the attack was delivered and what was targeted, and then infer what the adversary was intending to accomplish. Retention of logs is critical because it can help you determine what happened and aid in analysis of the attack.

**Exploitation** 

This stage uses a software, hardware, or human vulnerability to gain access. It can involve zero-day exploits and may use either adversary-triggered exploits or victim-triggered exploits.

Defense against this stage focuses on user awareness, secure coding, vulnerability scanning, penetration testing, endpoint hardening, and similar activities to ensure that organizations have a strong security posture and very limited attack surface.

**Installation**

This stage focuses on persistent backdoor access for attackers. 

Defenders must monitor for typical artifacts of a persistent remote shell or other remote access methodologies.

**Command-and-Control (C2)**

C2 access allows two-way communication and continued control of the remote system. 

Defenders will seek to detect the C2 infrastructure by hardeningthe network, deploying detection capabilities, and conducting ongoing research to ensure they are aware of new C2 models and technology.

**Actions on Objectives**

The final stage occurs when the mission's goal is achieved. Adversaries will collect credentials, escalate privileges, pivot and move laterally through the environment, and gather and exfiltrate information. They may also cause damage to systems or data. 

Defenders must establish their incident response playbook, detect the actions of the attackers and capture data about them, respond to alerts, and assess the damage the attackers have caused.

## Incident Response Data and Tools

Incident responders rely on a wide range of data for their efforts. As a security professional, you need to be aware of the types of data you may need to conduct an investigation and to determine both what occurred and how to prevent it from happening again.

### Security Information and Event Management Systems

In many organizations, the central security monitoring tool is a security information and event management (SIEM) tool.

SIEM devices and software have broad security capabilities, which are typically based on the ability to collect and aggregate log data from a variety of sources and then to perform correlation and analysis activities with that data.

This means that organizations will send data inputs—including logs and other useful information from systems, network security devices, network infrastructure, and many other sources—to a SIEM for it to ingest, compare to the other data it has, and then to apply rules, analytical techniques, and machine learning or artificial intelligence to the data.

SIEM systems may include the ability to review and alert on user behavior or to perform sentiment analysis, a process by which they look at text using natural language processing and other text analysis tools to determine emotions from textual data.

Another data input for SIEM devices is packet capture.

The ability to capture and analyze raw packet data from network traffic, or to receive packet captures from other data sources, can be useful for incident analysis, particularly when specific information is needed about a network event.

Correlating raw packet data with IDS or IPS events, firewall and WAF logs, and other security events provides a powerful tool for security practitioners.

SIEM devices also provide alerting, reporting, and response capabilities, allowing organizations to see when an issue needs to be addressed and to track the response to that issue through its lifecycle. 

This may include forensic capabilities, or it may be more focused on a ticketing and workflow process to handle issues and events.

#

### SIEM Dashboards

The first part of a SIEM that many security practitioners see is a dashboard like the AlienVault SIEM dashboard shown. 

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/5512ce97-8ff8-4a3a-8651-28d18881d150)

Dashboards can be configured to show the information considered most useful and critical to an organization or to the individual analyst, and multiple dashboards can be configured to show specific views and information.

The key to dashboards is understanding that they provide a high-level, visual representation of the information they contain. 

That helps security analysts to quickly identify likely problems, abnormal patterns, and new trends that may be of interest or concern.

SIEM dashboards have a number of important components that provide elements of their display. These include sensors that gather and send information to the SIEM, trending and alerting capabilities, correlation engines and rules, and methods to set sensitivity and levels.

#

### Sensors

Although devices can send data directly to a SIEM, sensors are often deployed to gather additional data.

Sensors are typically software agents, although they can be a virtual machine or even a dedicated device.

Sensors are often placed in environments like a cloud infrastructure, a remote datacenter, or other locations where volumes of unique data are being generated, or where a specialized device is needed because data acquisition needs are not being met by existing capabilities. 

Sensors gather useful data for the SIEM and may either forward it in its original form or do some preprocessing to optimize the data before the SIEM ingests it.

Choosing where to deploy sensors is part of network and security architecture and design efforts, and sensors must be secured and protected from attack and compromise just like other network security components.

#

### Sensitivity and Thresholds

Organizations can create a massive amount of data, and security data is no exception to that rule.

Analysts need to understand how to control and limit the alerts that a SIEM can generate.

To do that, they set thresholds, filter rules, and use other methods of managing the sensitivity of the SIEM. 

Alerts may be set to activate only when an event has happened a certain number of times, or when it impacts specific high-value systems. Or, an alert may be set to activate once instead of hundreds or thousands of times.

Regardless of how your SIEM handles sensitivity and thresholds, configuring and managing them so that alerts are sent only on items that need to be alerted on helps avoid alert fatigue and false positives.

One of the biggest threats to SIEM deployments is **alert fatigue**. Alert fatigue occurs when alerts are sent so often, for so many events, that analysts stop responding to them.

In most cases, these alerts aren't critical, high urgency, or high impact and are in essence just creating noise. Or, there may be a very high proportion of false positives, causing the analyst to spend hours chasing ghosts. 

In either case, alert fatigue means that when an actual event occurs it may be missed or simply disregarded, resulting in a much worse security incident than if analysts had been ready and willing to handle it sooner.

#

### Trends

A trend can point to a new problem that is starting to crop up, an exploit that is occurring and taking over, or simply which malware is most prevalent in your organization.

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/4ecade0a-6529-404f-841c-f4c5ff38c003)

You can see an example of categorizing malware activity, identifying which signatures have been detected the most frequently, which malware family is most prevalent, and where it sends traffic to. This can help organizations identify new threats as they rise to the top.

#

### Alerts and Alarms

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/ed160c61-b47b-4ba3-a5fd-98e04202d0c0)

Note that the alarms are categorized by their time and severity, and then provide detailed information that can be drilled down into. 

Events like malware beaconing and infection are automatically categorized, prioritized, marked by source and destination, and matched to an investigation by an analyst as appropriate. 

They also show things like which sensor is reporting the issue.

#

### Correlation and Analysis

Individual data points can be useful when investigating an incident, but matching data points to other data points is a key part of most investigations.

Correlation requires having data such as the time that an event occurred, what system or systems it occurred on, what user accounts were involved, and other details that can help with the analysis process.

A SIEM can allow you to search and filter data based on multiple data points like these to narrow down the information related to an incident.

Automated correlation and analysis is designed to match known events and indicators of compromise to build a complete dataset for an incident or event that can then be reviewed and analyzed.

As you can see in the screenshots from the AlienVault SIEM, you can add tags and investigations to data. Although each SIEM tool may refer to these by slightly different terms, the basic concepts and capabilities remain the same.

#

### Rules

The heart of alarms, alerts, and correlation engines for a SIEM is the set of rules that drive those components.

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/24ee5c7d-35ac-436b-a504-3fcf76f52e38)

An example of how an alarm rule can be built using information the SIEM gathers.

Rule conditions can use logic to determine if and  when a rule will be activated, and then actions can trigger based on the rule.

Results may be as simple as an alert or as complex as a programmatic action that changes infrastructure, enables or disables firewall rules, or triggers other defenses.

Rules are important but can also cause issues.

Poorly constructed rule logic may miss events or cause false positives or overly broad detections.

If the rule has an active response component, a mistriggered rule can cause an outage or other infrastructure issue. Thus, rules need to be carefully built, tested, and reviewed on a regular basis.

Although SIEM vendors often provide default rules and detection capabilities, the custom-built rules that organizations design for their environments and systems are key to a successful SIEM deployment.

The Security+ exam does not specifically call out SIEM rules, but underneath correlation, alerting, and trending capabilities, rules are often what is driving detections and alerts.

Finally, SIEM devices also follow the entire lifecycle for data. That means most have the ability to set retention and data lifespan for each type of data and have support for compliance requirements. 

In fact, most SIEM devices have prebuilt rules or modules designed to meet specific compliance requirements based on the standards they require.

SIEM devices frequently have built-in integrations for cloud services like Google, ServiceNow, Office 365, Okta, Sophos, and others. That means you can import data directly from those services to get a better view of your security environment.

#

### Log Files

Log files provide incident responders with information about what has occurred.

Of course, that makes log files a target for attackers as well, so incident responders need to make sure that the logs they are using have not been tampered with and that they have timestamps and other data that is correct.

Once you're sure the data you are working with is good, logs can provide a treasure trove of incident-related information.

In many enterprise environments, specific logs or critical log entries will be sent to a secure logging infrastructure to ensure a trustworthy replica of the logs collected at endpoint systems exists.

Security practitioners will still review local logs, particularly because the volume of log data at endpoints throughout an organization means that complete copies of all logs for every system are not typically maintained.

Common logs used by incident responders that are covered in the Security+ exam outline include the following:

- **System logs** include everything from service changes to permission issues. The Windows system log tracks information generated by the system while it is running.

- **Application logs** for Windows include information like installer information for applications, errors generated by applications, license checks, and any other logs that applications generate and send to the application log.

- **Security logs** for Windows systems store information about failed and successful logins, as well as other authentication log information. Authentication and security logs for Linux systems are stored in /var/log/auth.log and /var/log/secure.

- **Vulnerability scan output** is another form of data that can be pulled into incident analysis activities. Scans can provide clues about what attackers may have targeted, changes in services, or even suddenly patched issues due to attackers closing a hole behind them

- **Network and security device logs** can include logs for routers and switches with configuration changes, traffic information, network flows, and data captured by packet analyzers like Wireshark.

- **Web logs**, like those from Apache and Internet Information Services (IIS), track requests to the web server and related events. These logs can help track what was accessed, when it was accessed, and what IP address sent the request. Since requests are logged, these logs can also help identify attacks, including SQL injection and other web server and web application– specific attacks.

- **DNS logs** provide details about DNS queries. This may seem less useful, but DNS logs can show attackers gathering information, provide information that shows what systems may be compromised based on their DNS requests, and show whether internal users are misusing organizational resources.

- **Authentication logs** are useful to determine when an account was logged into and may also show privilege use, login system or location, incorrect password attempts, and other details of logins and usage that can be correlated to intrusions and misuse.

- **Dump files**, like the memory dump created when Windows experiences a blue screen of death, may not seem as if they'd be useful for incident response, but they can contain information that shows the state of memory and the system at the time of a crash. If the crash occurred because of an attacker or exploit, or if malware or attack tools were on the system, the dump file may contain those artifacts.

- **VoIP (Voice over IP)**, **call manager logs**, and **Session Initiation Protocol (SIP) logs** can provide information about calls that were placed as well as other events on a VoIP system.

Security practitioners will use SIEM tools as well as manual search tools like grep and tail to review logs for specific log entries that may be relevant to an event or incident. Lists of important Windows event IDs are commonly available, and many Linux log entries can be easily identified by the text they contain.

#

### Going With the Flow

Tracking your bandwidth utilization using a bandwidth monitor can provide trend information that can help spot both current problems and new behaviors

Network flows, either using Cisco's proprietary NetFlow protocol, which is a software-driven capability, or SFlow, which is broadly implemented on devices from many vendors, are an  important tool in an incident responder's toolkit.

In addition to NetFlow and SFlow, you may encounter IPFIX, an open standard based on NetFlow 9 that many vendors support.

The hardware deployed in your environment is likely to drive the decision about which to use, with each option having advantages and disadvantages.

Network flows are incredibly helpful when you are attempting to determine what traffic was sent on your network, where it went, or where it came from.

Flows contain information such as the source and destination of traffic, how  much traffic was sent, and when the traffic occurred.

You can think of flow information like phone records—you know what number was called and how long the conversation took, but not what was said. Thus, although flows like those shown in the following graphic are useful hints, they may not contain all the information about an event.

Flows may not show all the traffic for another reason too: keeping track of high-volume traffic flows can consume a large amount of network device processing power and storage, and thus many flows are sampled at rates like 10:1 or even 1000:1

That means flows may not capture all traffic, and you may lose some resolution and detail in your flow analysis.

Even though flows may only show part of the picture, they are a very useful diagnostic and incident response tool. If you're tasked with providing network security for an organization, you may want to consider setting up flows as part of your instrumentation efforts.

#

### Logging Protocols and Tools

In addition to knowing how to find and search through logs, you need to know how logs are sent to remote systems, what tools are used to collect and manage logs, and how they are acquired.

Traditional Linux logs are sent via **syslog**, with clients sending messages to servers that collect and store the logs. Over time, other syslog replacements have been created to improve upon the basic functionality and capabilities of syslog.

When speed is necessary, the rocket-fast system for log processing, or **rsyslog**, is an option. It supports extremely high message rates, secure logging via TLS, and TCP-based messages as well as multiple backend database options.

Another alternative is **syslog-ng**, which provides enhanced filtering, direct logging to databases, and support for sending logs via TCP protected by TLS.

The enhanced features of syslog replacements like rsyslog and syslog-ng mean that many organizations replace their syslog infrastructure with one of these options.

A final option for log collection is NXLog, an open source and commercially supported syslog centralization and aggregation tool that can parse and generate log files in many common formats while also sending logs to analysis tools and SIEM solutions.

Regardless of the logging system you use, you will have to make decisions about retention on both local systems and central logging and monitoring infrastructure.

Take into account operational needs; likely scenarios where you may need the logs you collect; and legal, compliance, or other requirements that you need to meet.

In many cases organizations choose to keep logs for 30, 45, 90, or 180 days depending on their needs, but some cases may even result in some logs being kept for a year or more. Retention comes with both hardware costs and potential legal challenges if you retain logs that you may not wish to disclose in court.

#

### Digging in to systemd's Journal in Linux

The Security+ exam outline includes a large number of types of logging systems and software, logs, analysis tools, and other data sources. You should focus on thinking about why you might need each of them, and where a specific tool is named, you should make sure you know its basic usage and functions.

Most Linux distributions rely on systemd to manage services and processes and, in general, manage the system itself.

Accessing the systemd journal that records what systemd is doing using the journald daemon can be accomplished using journalctl.

This tool allows you to review kernel, services, and initrd messages as well as many others that systemd generates.

Simply issuing the journalctl command will display all the journal entries, but additional modes can be useful. If you need to see what happened since the last boot, the -b flag will show only those entries. Filtering by time can be accomplished with the –since flag and a time/date entry in the format “year-month-day hour:minute:seconds.”

#

### Going Beyond Logs: Using Metadata

Metadata generated as a normal part of system operations, communications, and other activities can also be used for incident response.

Metadata is data about other data—in the case of systemsand services, metadata is created as part of files, embedded in documents, used to define structured data, and included in transactions and network communications, among many other places you can find it.

The Security+ exam outline focuses on four types of metadata, but the techniques behind metadata analysis can be used for other data types in many cases as well. The four types of metadata you will need to consider for the exam are as follows:

- **Email metadata** includes headers and other information found in an email. Email headers provide details about the sender, the recipient, the date and time the message was sent, whether the email had an attachment, which systems the email traveled through, and other header markup that systems may have added, including antispam and other information.

- **Mobile metadata** is collected by phones and other mobiledevices as they are used. It can include call logs, SMS and other message data, data usage, GPS location tracking, cellular tower information, and other details found in call data records. Mobile metadata is incredibly powerful because of the amount of geospatial information that is recorded about where the phone is at any point during each day.

- **Web metadata** is embedded into websites as part of the code of the website but is often invisible to everyday users. It can include metatags, headers, cookies, and other information that help with search engine optimization, website functionality, advertising, and tracking, or that may support specific functionality.

- **File metadata** can be a powerful tool when reviewing when a file was created, how it was created, if and when it was modified, who modified it, the GPS location of the device that created it, and many other details. Mobile devices may also include the GPS location of the photo if they are not set to remove that information from photos, resulting in even more information leakage.

Metadata is commonly used for forensic and other investigations, and most forensic tools have built-in metadata-viewing capabilities.

## Mitigation and Recovery

An active incident can cause disruptions throughout an organization. The organization must act to mitigate the incident and then work to recover from it without creating new risks or vulnerabilities.

At the same time, the organization may want to preserve incident data and artifacts to allow forensic analysis by internal responders or law enforcement.

### Playbooks

Playbooks are step-by-step guides intended to help incident response teams take the right actions in a given scenario.

Organizations build playbooks for each type of incident or event that they believe they are likely to handle, with examples ranging from advanced persistent threats to phishing attacks.

A playbook will often have stages with steps at each stage of the incident response cycle, as well as a set of guidelines about when to activate the playbook and who should be involved to run through the playbook.

A playbook for a malware infection's identification stage might include identifying indicators of compromise using antimalware and antivirus software, packet captures, and network traffic analysis, and then a path forward to a containment stage with steps for that stage as well.

Playbooks take into account factors like industry best practices, organizational policies, laws, regulation, and compliance requirements, and the organizational structure and staffing.

They also define when they are complete, allowing organizations to resume normal operations.

A well-written, tested set of playbooks for the incident types your organization is most likely to encounter is one of the best ways to ensure that responses happen appropriately in a stressful situation. The ability to refer to steps and processes that were created with forethought and care can make an immense difference in the quality of an incident response process.

#

### Runbooks

Runbooks are the operational procedures guides that organizations use to perform actions.

Since they are procedural guides, runbooks simplify the decision process for common operations that may support incident response, and they can help guide and build automation for tasks like communications, malware removal, or scanning. 

Runbooks are typically action-oriented and thus may be paired with a playbook as elements of the playbook's process.

#

### Secure Orchestration, Automation, and Response (SOAR)

Managing multiple security technologies can be challenging, and using the information from those platforms and systems to determine your organization's security posture and status requires integrating different data sources.

At the same time, managing security operations and remediating issues you identify is also an important part of security work. SOAR platforms seek to address these needs.

As a mitigation and recovery tool, SOAR platforms allow you to quickly assess the attack surface of an organization, the state of systems, and where issues may exist. They also allow automation of remediation and restoration workflows.

#

### Containment, Mitigation, and Recovery Techniques

In many cases, one of the first mitigation techniques will be to quickly block the cause of the incident on the impacted systems or devices.

That means you may need to reconfigure endpoint security solutions:

- Application allow listing (sometimes referred to as whitelisting), which lists the applications and files that are allowed to be on a system and prevents anything that is not on the list from being installed or run.

- Application deny lists or block lists (sometimes referred to as blacklists), which list applications or files that are not allowed on a system and will prevent them from being installed or copied to the system.

- Quarantine solutions, which can place files in a specific safe zone. Antimalware and antivirus often provide an option to quarantine suspect or infected files rather than deleting them, which can help with investigations.

Understanding the settings you are using and the situations where they may apply is critical. Quarantine can be a great way to ensure that you still have access to the files, but it does run the danger of allowing the malicious files to still be on the system, even if they should be in a safe location.

Configuration changes are also a common remediation and containment.

They may be required to address a security vulnerability that allowed the incident to occur, or they may be needed to isolate a system or network.

In fact, configuration changes are one of the most frequently used tools in containment and remediation efforts.

They need to be carefully tracked and recorded, since responders can still make mistakes, and changes may have to be rolled back after the incident response process to allow a return to normal function.

The specific configuration changes you should consider for the Security+ exam are as follows:

- Firewall rule changes, either to add new firewall rules, modify existing firewall rules, or in some cases, to remove firewall rules.

- Mobile device management (MDM) changes, including applying new policies or changing policies; responding by remotely wiping devices; locating devices; or using other MDM capabilities to assist in the IR process.

- Data loss prevention (DLP) tool changes, which may focus on preventing data from leaving the organization or detecting new types or classifications of data from being sent or shared. DLP changes are likely to be reactive in most IR processes, but DLP can be used to help ensure that an ongoing incident has a lower chance of creating more data exposure.

- Content filter and URL filtering capabilities, which can be used to ensure that specific sites are not able to be browsed or accessed. Content filter and URL filtering can help prevent malware from phoning home or connecting to C2 sites, and it can also prevent users from responding to phishing attacks and similar threats.

- Updating or revoking certificates, which may be required if the certificates were compromised, particularly if attackers had access to the private keys for the certificates. At the same time, removing certificates from trust lists can also be a useful tool, particularly if an upstream service provider is not responding promptly and there are security concerns with their services or systems

When you're faced with an incident response scenario, you should consider what was targeted; how it was targeted; what the impact was; and what controls, configuration changes, and tools you can apply to first contain and then remediate the issue.

It is important to bear in mind the operational impact and additional risks that the changes you are considering may result in, and to ensure that stakeholders are made aware of the changes or are involved in the decision, depending on the urgency of the situation.

Although they aren't directly mentioned in the Security+ exam outline, there are a number of other common configuration changes used for incident response. Among them are patching, disabling services, changing permissions, and other common system hardening practices. As you prepare for the exam, remember that many of the techniques used for system hardening are also frequently used in incident response scenarios.

At times, broader action may also be necessary. Removing systems, devices, or even entire network segments or zones may be required to stop further spread of an incident or when the source of the incident cannot be quickly identified. 

The following techniques support this type of activity:

- **Isolation** moves a system into a protected space or network where it can be kept away from other systems. Isolation can be as simple as removing a system from the network or as technically complex as moving it to an isolation VLAN, or in the case of virtual machines or cloud infrastructure, it may require moving the system to an environment with security rules that will keep it isolated while allowing inspection and investigation.

- **Containment** leaves the system in place but works to prevent further malicious actions or attacks.

Network-level containment is frequently accomplished using firewall rules or similar capabilities to limit the traffic that the system can send or receive. 

System and application-level containment can be more difficult without shutting down the system or interfering with the functionality and state of the system, which can have an impact on forensic data. 

Therefore, the decisions you make about containment actions can have an impact on your future investigative work. Incident responders may have different goals than forensic analysts, and organizations may have to make quick choices about whether rapid response or forensic data is more important in some situations.

- **Segmentation** is often employed before an incident occurs to place systems with different functions or data security levels in different zones or segments of a network. Segmentation can also be done in virtual and cloud environments.

In essence, segmentation is the process of using security, network, or physical machine boundaries to build separation between environments, systems, networks, or other components. Incident responders may choose to use segmentation techniques as part of a response process to move groups of systems or services so that they can focus on other areas. You might choose to segment infected systems away from the rest of your network or to move crucial systems to a more protected segment to help protect them during an active incident.
