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


