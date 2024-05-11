# Security Policies, Standards, and Compliance

Policy serves as the foundation for any cybersecurity program, setting out the principles and rules that guide the execution of security efforts throughout the enterprise.

Often, organizations base these policies on best practice frameworks developed by industry groups such as the National Institute of Standards and Technology (NIST) or the International Organization for Standardization (ISO). 

In many cases, organizational policies are also influenced and directed by external compliance obligations that regulators impose on the organization.

### Understanding Policy Documents**

An organization's **information security policy framework contains a series of documents designed to describe the organization's cybersecurity program.

The scope and complexity of these documents vary widely, depending on the nature of the organization and its information resources. 

These frameworks generally include four different types of document:

- Policies
- Standards
- Procedures
- Guidelines

Keep in mind that the definitions of these categories vary significantly from organization to organization and it is very common to find the lines between them blurred.

Though at first glance that may seem incorrect, it's a natural occurrence as security theory meets the real world. 

As long as the documents are achieving their desired purpose, there's no harm and no foul.

#

### Policies

Policies are high-level statements of management intent. 

Compliance with policies is mandatory.

An information security policy will generally contain broad statements about cybersecurity objectives, including the following:

- A statement of the importance of cybersecurity to the organization

- Requirements that all staff and contracts take measures to protect the confidentiality, integrity, and availability of information and information systems

- Statement on the ownership of information created and/or possessed by the organization

- Designation of the chief information security officer (CISO) or other individual as the executive responsible for cybersecurity issues

- Delegation of authority granting the CISO the ability to create standards, procedures, and guidelines that implement the policy

In many organizations, the process to create a policy is laborious and requires very high-level approval, often from the chief executive officer (CEO).

Keeping policy statements at a high level provides the CISO with the flexibility to adapt and change specific security requirements with changes in the business and technology environments.

For example, the five-page information security policy at the University of Notre Dame simply states

"The Information Governance Committee will create handling standards for each Highly Sensitive data element. Data stewards may create standards for other data elements under their stewardship. These information handling standards will specify controls to manage risks to University information and related assets based on their classification. All individuals at the University are responsible for complying with these controls."

By way of contrast, the federal government's Centers for Medicare & Medicaid Services (CMS) has a 95-page information security policy. This mammoth document contains incredibly detailed requirements, such as

"A record of all requests for monitoring must be maintained by the CMS CIO along with any other summary results or documentation produced during the period of monitoring. The record must also reflect the scope of the monitoring by documenting search terms and techniques. All information collected from monitoring must be controlled and protected with distribution limited to the individuals identified in the request for monitoring and other individuals specifically designated by the CMS Administrator or CMS CIO as having a specific need to know such information."

The CMS document even goes so far as to include a complex chart describing the many cybersecurity roles held by individuals throughout the agency.

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/dcabe157-c672-45ca-9648-83250411a036)

This approach may meet the needs of CMS, but it is hard to imagine the long-term maintenance of that document. Lengthy security policies often quickly become outdated as necessary changes to individual requirements accumulate and become neglected because staff are weary of continually publishing new versions of the policy.

Organizations commonly include the following documents in their information security policy library:

- **Information security policy** that provides high-level authority and guidance for the security program.

- **Acceptable use policy (AUP)** that provides network and system users with clear direction on permissible uses of information resources

- **Data governance policy** that clearly states the ownership of information created or used by the organization.

- **Data classification policy** that describes the classification structure used by the organization and the process used to properly assign classifications to data.

- **Data retention policy** that outlines what information the organization will maintain and the length of time different categories of work product will be retained prior to destruction.

- **Credential management policy** that describes the account lifecycle from provisioning through active use and decommissioning. This policy should include specific requirements for personnel who are employees of the organization as well as third-party contractors. It should also include requirements for credentials used by devices, service accounts, and administrator/root accounts.

- **Password policy** that sets forth requirements for password length, complexity, reuse, and similar issues.

- **Continuous monitoring policy** that describes the organization's approach to monitoring and informs employees that their activity is subject to monitoring in the workplace.

- **Code of conduct/ethics** that describes expected behavior of employees and affiliates and covers situations not specifically addressed in policy.

- **Change management and change control policies** that describe how the organization will review, approve, and implement proposed changes to information systems in a manner that manages both cybersecurity and operational risk.

- **Asset management** that describes the process that the organization will follow for accepting new assets (such as computers and mobile devices) into inventory, tracking those assets over their lifetime, and properly disposing of them at the end of their useful life.

As you read through the list, you may notice that some of the documents listed tend to conflict with our description of policies as high-level documents and seem to better fit the definition of a standard in the next section. CompTIA specifically includes these items as elements of information security policy whereas many organizations would move some of them, such as password requirements, into standards documents.

#

### Standards

Standards provide mandatory requirements describing how an organization will carry out its information security policies.

These may include the specific configuration settings used for a common operating system, the controls that must be put in place for highly sensitive information, or any other security objective.

Standards are typically approved at a lower organizational level than policies and, therefore, may change more regularly.

For example, the University of California at Berkeley maintains a detailed document titled the Minimum Security Standards for Electronic Information.

This document divides information into four different data protection levels (DPLs) and then describes what controls are required, optional, and not required for data at different levels, using a detailed matrix.

The standard then provides detailed descriptions for each of these requirements with definitions of the terms used in the requirements.

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/4ab883cf-39f9-4f6d-8c98-89581d636e97)

For example, requirement 3.1 reads “Secure configurations.” Later in the document, UC Berkeley expands this to read “Resource Custodians must utilize well-managed security configurations for hardware, software, and operating systems based on industry standards.” It goes on to defined “well-managed” as including the following:

- Devices must have secure configurations in place prior to deployment.

- Any deviations from defined security configurations must be approved through a change management process and documented. A process must exist to annually review deviations from the defined security configurations for continued relevance.

- A process must exist to regularly check configurations of devices and alert the Resource Custodian of any changes

This approach provides a document hierarchy that is easy to navigate for the reader and provides access to increasing levels of detail as needed.

Clicking those links leads to advice to organizations subject to this policy that begins with this text:

"UC Berkeley security policy mandates compliance with Minimum Security Standard for Electronic Information for devices handling covered data. The recommendations below are provided as optional guidance."

This is a perfect example of three elements of the information security policy framework working together. 

Policy sets out the high-level objectives of the security program and requires compliance with standards, which includes details of required security controls. 

Guidelines provide advice to organizations seeking to comply with the policy and standards.

In some cases, organizations may operate in industries that have commonly accepted standards that the organization either must follow or chooses to follow as a best practice. 

Failure to follow industry best practices may be seen as negligence and can cause legal liability for the organization. 

Many of these industry standards are expressed in the standard frameworks discussed later in this chapter.

#

### Procedures

Procedures are detailed, step-by-step processes that individuals and organizations must follow in specific circumstances.

Similar to checklists, procedures ensure a consistent process for achieving a security objective.

Organizations may create procedures for building new systems, releasing code to production environments, responding to security incidents, and many other tasks.

Compliance with procedures is mandatory.

For example, Visa publishes a document titled What to Do if Compromised that lays out a mandatory process that merchants suspecting a credit card compromise must follow.

Although the document doesn't contain the word procedure in the title, the introduction clearly states that the document “establishes procedures and timelines for reporting and responding to a suspected or confirmed Compromise Event.”

The document provides requirements covering the following areas of incident response:

- Notify Visa of the incident within three days
- Provide Visa with an initial investigation report
- Provide notice to other relevant parties
- Provide exposed payment account data to Visa
- Conduct PCI forensic investigation
- Conduct independent investigation
- Preserve evidence

Each of these sections provides detailed information on how Visa expects merchants to handle incident response activities.

For example, the forensic investigation section describes the use of Payment Card Industry Forensic Investigators (PFI) and reads as follows:

  Upon discovery of an account data compromise, or receipt of an independent forensic investigation notification, an entity must:

- Engage a PFI (or sign a contract) within five (5) business days.

- Provide Visa with the initial forensic (i.e., preliminary) report within ten (10) business days from when the PFI is engaged (or the contract is signed).

- Provide Visa with a final forensic report within ten (10) business days of the completion of the review.

There's not much room for interpretation in this type of language.

Visa is laying out a clear and mandatory procedure describing what actions the merchant must take, the type of investigator they should hire, and the timeline for completing different milestones.

Organizations commonly include the following procedures in their policy frameworks:

- **Monitoring procedures** that describe how the organization will perform security monitoring activities, including the possible use of continuous monitoring technology

- **Evidence production procedures** that describe how the organization will respond to subpoenas, court orders, and other legitimate requests to produce digital evidence

- **Patching procedures** that describe the frequency and process of applying patches to applications and systems under the organization's care

Of course, cybersecurity teams may decide to include many other types of procedures in their frameworks, as dictated by the organization's operational needs.

#

### Guidelines

Guidelines provide best practices and recommendations related to a given concept, technology, or task.

Compliance with guidelines is not mandatory, and guidelines are offered in the spirit of providing helpful advice. That said, the “optionality” of guidelines may vary significantly depending on the organization's culture.

In April 2016, the chief information officer (CIO) of the state of Washington published a 25-page document providing guidelines on the use of electronic signatures by state agencies.

The document is not designed to be obligatory but, rather, offers advice to agencies seeking to adopt electronic signature technology.

The document begins with a purpose section that outlines three goals of guideline:

1. Help agencies determine if, and to what extent, their agency will implement and rely on electronic records and electronic signatures.

2. Provide agencies with information they can use to establish policy or rules governing their use and acceptance of digital signatures.

3. Provide direction to agencies for sharing of their policies with the Office of the Chief Information Officer (OCIO) pursuant to state law.

The first two stated objectives line up completely with the function of a guideline. Phrases like “help agencies determine” and “provide agencies with information” are common in guideline documents.

There is nothing mandatory about them, and in fact, the guidelines explicitly state that Washington state law “does not mandate that any state agency accept or require electronic signatures or records.”

The third objective might seem a little strange to include in a guideline. Phrases like “provide direction” are more commonly found in policies and procedures.

Browsing through the document, the text relating to this objective is only a single paragraph within a 25-page document:

"The Office of the Chief Information Officer maintains a page on the OCIO.wa.gov website listing links to individual agency electronic signature and record submission policies. As agencies publish their policies, the link and agency contact information should be emailed to the OCIO Policy Mailbox. The information will be added to the page within 5 working days. Agencies are responsible for notifying the OCIO if the information changes."

Reading this paragraph, the text does appear to clearly outline a mandatory procedure and would not be appropriate in a guideline document that fits within the strict definition of the term.

However, it is likely that the committee drafting this document thought it would be much more convenient to the reader to include this explanatory text in the related guideline rather than drafting a separate procedure document for a fairly mundane and simple task.

#

### Exceptions and Compensating Controls

When adopting new security policies, standards, and procedures, organizations should also provide a mechanism for exceptions to those rules.

Inevitably, unforeseen circumstances will arise that require a deviation from the requirements.

The policy framework should lay out the specific requirements for receiving an exception and the individual or committee with the authority to approve exceptions.

The state of Washington uses an exception process that requires the requestor document the following information:

- Standard/requirement that requires an exception
- Reason for noncompliance with the requirement
- Business and/or technical justification for the exception
- Scope and duration of the exception
- Risks associated with the exception
- Description of any supplemental controls that mitigate the risks associated with the exception
- Plan for achieving compliance
- Identification of any unmitigated risks

Many exception processes require the use of **compensating controls**to mitigate the risk associated with exceptions to security standards.

The Payment Card Industry Data Security Standard (PCI DSS) includes one of the most formal compensating control processes in use today. 

It sets out three criteria that must be met for a compensating control to be satisfactory:

1. The control must meet the intent and rigor of the original requirement.

2. The control must provide a similar level of defense as the original requirement, such that the compensating control sufficiently offsets the risk that the original PCI DSS requirement was designed to defend against.

3. The control must be “above and beyond” other PCI DSS requirements.

For example, an organization might find that it needs to run an outdated version of an operating system on a specific machine because software necessary to run the business will only function on that operating system version. Most security policies would prohibit using the outdated operating system because it might be susceptible to security vulnerabilities.

The organization could choose to run this system on an isolated network with either very little or no access to other systems as a compensating control.

The general idea is that a compensating control finds alternative means to achieve an objective when the organization cannot meet the original control requirement.

Although PCI DSS offers a very formal process for compensating controls, the use of compensating controls is a common strategy in many different organizations, even those not subject to PCI DSS.

Compensating controls balance the fact that it simply isn't possible to implement every required security control in every circumstance with the desire to manage risk to the greatest feasible degree.

In many cases, organizations adopt compensating controls to address a temporary exception to a security requirement. In those cases, the organization should also develop remediation plans designed to bring the organization back into compliance with the letter and intent of the original control.

## Personnel Management

An organization's employees require access to information and systems to carry out their assigned job functions. 

With this access comes the risk that an employee will, through intentional or accidental action, become the source of a cybersecurity incident. 

Organizations that follow personnel management best practices can reduce the likelihood and impact of employee-centered security risks.

### Least Privilege

The principle of least privilege says that individuals should be granted only the minimum set of permissions necessary to carry out their job functions.

Least privilege is simple in concept but sometimes challenging to implement in practice.

It requires careful attention to the privileges necessary to perform specific jobs and ongoing attention to avoid security issues. 

Privilege creep, one of these issues, occurs when an employee moves from job to job within the organization, accumulating new privileges, but never has the privileges associated with past duties revoked.

#

### Separation of Duties

Organizations may implement separation of duties for extremely sensitive job functions.

Separation of duties takes two different tasks that, when combined, have great sensitivity and creates a rule that no single person may have the privileges required to perform both tasks.

The most common example of separation of duties comes in the world of accounting.

Individuals working in accounting teams pose a risk to the organization should they decide to steal funds. They might carry out this theft by creating a new vendor in the accounting system with the name of a company that they control and then issuing checks to that vendor through the normal check-writing process.

An organization might manage this risk by recognizing that the ability to create a new vendor and issue a check is sensitive when used in combination and implement separation of duties for them.

In that situation, no single individual would have the permission to both create a new vendor and issue a check. 

An accounting employee seeking to steal funds in this manner would now need to solicit the collusion of at least one other employee, reducing the risk of fraudulent activity.

**Two-person control** is a concept that is similar to separation of duties but with an important difference: instead of preventing the same person from holding two different privileges that are sensitive when used together, two-person control requires the participation of two people to perform a single sensitive action.

#

### Job Rotation and Mandatory Vacations

Organizations also take other measures to reduce the risk of fraudulent activity by a single employee. 

Two of these practices focus on uncovering fraudulent actions after they occur by exposing them to other employees.

Job rotation practices take employees with sensitive roles and move them periodically to other positions in the organization.

The motivating force behind these efforts is that many types of fraud require ongoing concealment activities. 

If an individual commits fraud and is then rotated out of their existing assignment, they may not be able to continue those concealment activities due to changes in privileges and their replacement may discover the fraud themselves.

Mandatory vacations serve a similar purpose by forcing employees to take annual vacations of a week or more consecutive time and revoking their access privileges during that vacation period.

#

### Clean Desk Space

Clean desk policies are designed to protect the confidentiality of sensitive information by limiting the amount of paper left exposed on unattended employee desks.

Organizations implementing a clean desk policy require that all papers and other materials be secured before an employee leaves their desk.

#

### Onboarding and Offboarding

Organizations should have standardized processes for onboarding new employees upon hire and offboarding employees who are terminated or resign.

These processes ensure that the organization retains control of its assets and handles the granting and revocation of credentials and privileges in an orderly manner.

New hire processes should also include background checks designed to uncover any criminal activity or other past behavior that may indicate that a potential employee poses an undetected risk to the organization.

#

### Nondisclosure Agreements

Nondisclosure agreements (NDAs) require that employees protect any confidential information that they gain access to in the course of their employment.

Organizations normally ask new employees to sign an NDA upon hire and periodically remind employees of their responsibilities under the NDA.

Offboarding processes often involve exit interviews that include a final reminder of the employee's responsibility to abide by the terms of the NDA even after the end of their affiliation with the organization.

#

### Social Media

Organizations may choose to adopt social media policies that constrain the behavior of employees on social media.

Social media analysis performed by the organization may include assessments of both personal and professional accounts, because that activity may reflect positively or negatively upon the organization. 

Organizations should make their expectations and practices clear in a social media policy

#

### User Training

Users within your organization should receive regular security awareness training to ensure that they understand the risks associated with your computing environment and their role in minimizing those risks.

Strong training programs take advantage of a diversity of training techniques, including the use of computer-based training (CBT).

Not every user requires the same level of training.

Organizations should use role-based training to make sure that individuals receive the appropriate level of training based on their job responsibilities.

For example, a systems administrator should receive detailed and highly technical training, whereas a customer service representative requires less technical training with a greater focus on social engineering and pretexting attacks that they may encounter in their work.

Phishing attacks often target users at all levels of the organization, and every security awareness program should include specific antiphishing campaigns designed to help users recognize suspicious requests and respond appropriately.

These campaigns often involve the use of phishing simulations, which send users fake phishing messages to test their skills. Users who click on the simulated phishing message are sent to a training program designed to help them better recognize fraudulent messages.

Security awareness training also commonly incorporates elements of **gamification**, designed to make training more enjoyable and help users retain the message of the campaign.

Capture the flag (CTF) exercises are a great example of this. CTF programs pit technologists against one another in an attempt to attack a system and achieve a specific goal, such as stealing a sensitive file. Participants in the CTF exercise gain an appreciation for attacker techniques and learn how to better defend their own systems against similar attacks.

## Third-Party Risk Management

Many risks facing an organization come from third-party organizations with whom the organization does business. 

These risks may be the result of a vendor relationship that arises somewhere along the organization's supply chain or they may be the result of other business partnerships. 

Organizations may deploy some standard agreements and practices to manage these risks.

Commonly used agreements include the following:

- **Master service agreements (MSA)** provide an umbrella contract for the work that a vendor does with an organization over an extended period of time. The MSA typically includes detailed security and privacy requirements. Each time the organization enters into a new project with the vendor, they may then create a statement of work (SOW) that contains project-specific details and references the MSA.

- **Service level agreements (SLA)** are written contracts that specify the conditions of service that will be provided by the vendor and the remedies available to the customer if the vendor fails to meet the SLA. SLAs commonly cover issues such as system availability, data durability, and response time.

- A **memorandum of understanding (MOU)** is a letter written to document aspects of the relationship. MOUs are an informal mechanism that allows the parties to document their relationship to avoid future misunderstandings. MOUs are commonly used in cases where an internal service provider is offering a service to a customer that is in a different business unit of the same company.

- **Business partnership agreements (BPAs)** exist when two organizations agree to do business with each other in a partnership. For example, if two companies jointly develop and market a product, the BPA might specify each partner's responsibilities and the division of profits.

Organizations will need to select the agreement type(s) most appropriate for their specific circumstances. 

#

### Winding Down Vendor Relationships

All things come to an end, and third-party relationships are no exception. 

Organizations should take steps to ensure that they have an orderly transition when a vendor relationship ends or the vendor is discontinuing a product or service on which the organization depends. 

This should include specific steps that both parties will follow to have an orderly transition when the vendor announces a product's end of life (EOL) or a service's end of service life (EOSL).

These same steps may be followed if the organization chooses to stop using the product or service on its own.

Vendor agreements should also include NDA terms, and organizations should ensure that vendors ask their own employees to sign NDAs if they will have access to your sensitive information.

#

### Complying with Laws and Regulations

Legislators and regulators around the world take an interest in Cybersecurity due to the potential impact of cybersecurity shortcomings on individuals, government, and society.

Whereas the European Union (EU) has a broad-ranging data protection regulation, cybersecurity analysts in the United States are forced to deal with a patchwork of security regulations covering different industries and information categories.

Some of the major information security regulations facing organizations include the following:

- The **Health Insurance Portability and Accountability Act (HIPAA)** includes security and privacy rules that affect healthcare providers, health insurers, and health information clearinghouses in the United States.

- The **Payment Card Industry Data Security Standard (PCI DSS)** provides detailed rules about the storage, processing, and transmission of credit and debit card information. PCI DSS is not a law but rather a contractual obligation that applies to credit card merchants and service providers worldwide.

- The **Gramm–Leach–Bliley Act (GLBA)** covers U.S. financial institutions, broadly defined. It requires that those institutions have a formal security program and designate an individual as having overall responsibility for that program.

- The **Sarbanes–Oxley (SOX)** Act applies to the financial records of U.S. publicly traded companies and requires that those companies have a strong degree of assurance for the IT systems that store and process those records.

- The **General Data Protection Regulation (GDPR)** implements security and privacy requirements for the personal information of European Union residents worldwide.

- The **Family Educational Rights and Privacy Act (FERPA)** requires that U.S. educational institutions implement security and privacy controls for student educational records.

- Various **data breach notification laws** describe the requirements that individual states place on organizations that suffer data breaches regarding notification of individuals affected by the breach.

Remember that this is only a brief listing of security regulations. There are many other laws and obligations that apply to specific industries and data types.

You should always consult your organization's legal counsel and subject matter experts when designing a compliance strategy for your organization. 

You'll need to understand the various national, territory, and state laws that apply to your operations, and the advice of a well-versed attorney is crucial when interpreting and applying cybersecurity regulations to your specific business and technical environment.

#

### Adopting Standard Frameworks

Developing a cybersecurity program from scratch is a formidable undertaking. 

Organizations will have a wide variety of control objectives and tools at their disposal to meet those objectives. Teams facing the task of developing a new security program or evaluating an existing program may find it challenging to cover a large amount of ground without a roadmap.

Fortunately, several standard security frameworks are available to assist with this task and provide a standardized approach to developing cybersecurity programs.

#

### NIST Cybersecurity Framework

The National Institute for Standards and Technology (NIST) is responsible for developing cybersecurity standards across the U.S. federal government.

The guidance and standard documents they produce in this process often have wide applicability across the private sector and are commonly referred to by nongovernmental security analysts due to the fact that they are available in the public domain and are typically of very high quality.

In 2018, NIST released version 1.1 of a Cybersecurity Framework (CSF) designed to assist organizations attempting to meet one or more of the following five objectives:

- Describe their current cybersecurity posture.

- Describe their target state for cybersecurity.

- Identify and prioritize opportunities for improvement within the context of a continuous and repeatable process.

- Assess progress toward the target state.

- Communicate among internal and external stakeholders about cybersecurity risk.

The NIST framework includes three components:
- The Framework Core is a set of five security functions that apply across all industries and sectors: identify, protect, detect, respond, and recover. The framework then divides these functions into categories, subcategories, and informative references. A small excerpt of this matrix in completed form, looking specifically at the Identify(ID) function and the Asset Management category.

- The Framework Implementation assesses how an organization is positioned to meet cybersecurity objectives. This approach is an example of a maturity model that describes the current and desired positioning of an organization along a continuum of progress. In the case of the NIST maturity model, organizations are assigned to one of four maturity model tiers.

- Framework profiles describe how a specific organization might approach the security functions covered by the Framework Core. An organization might use a framework profile to describe its current state and then a separate profile to describe its desired future state.


![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/98157327-0ee1-4c9a-b3d9-2eb5f2945055)


![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/0ab92ee6-012e-4733-a2fb-8d78b9d2e04c)

NIST Cybersecurity Framework implementation tiers


![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/874483ad-5a2f-4010-bd06-7e955aa14cfe)
![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/eac720eb-57c5-433a-9c1e-ada18cfcbd1f)

The NIST Cybersecurity Framework provides organizations with a sound approach to developing and evaluating the state of their cybersecurity programs.

#

### NIST Risk Management Framework

In addition to the CSF, NIST publishes a Risk Management Framework (RMF).

The RMF is a mandatory standard for federal agencies that provides a formalized process that federal agencies must follow to select, implement, and assess risk-based security and privacy controls.

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/bc9aeb3f-cce0-403b-99ce-b36df57c87ad)

The Security+ exam covers both the NIST CSF and RMF, and it can be a little confusing to keep them straight.

The RMF is a formal process for implementing security controls and authorizing system use, whereas the CSF provides a broad structure for cybersecurity controls.

It's important to understand that, although both the CSF and RMF are mandatory for government agencies, only the CSF is commonly used in private industry.

#

### ISO Standards

The International Organization for Standardization (ISO) publishes a series of standards that offer best practices for cybersecurity and privacy.

As you prepare for the Security+ exam, you should be familiar with four specific ISO standards: ISO 27001, ISO 27002, ISO 27701, and ISO 31000.

#

### ISO 27001

ISO 27001 is a standard document titled “Information technology— Security techniques—Information security management systems— Requirements.” 

This standard includes control objectives covering 14 categories:

- Information security policies
- Organization of information security
- Human resource security
- Asset management
- Access control
- Cryptography
- Physical and environmental security
- Operations security
- Communications security
- System acquisition, development, and maintenance
- Supplier relationships
- Information security incident management
- Information security aspects of business continuity management
- Compliance with internal requirements, such as policies, and with external requirements, such as laws

The ISO 27001 standard was once the most commonly used information security standards, but it is declining in popularity outside of highly regulated industries that require ISO compliance.

Organizations in those industries may choose to formally adopt ISO 27001 and pursue **certification** programs, where an external assessor validates their compliance with the standard and certifies them as operating in accordance with ISO 27001.

#

### ISO 27002

The ISO 27002 standard goes beyond control objectives and describes the actual controls that an organization may implement to meet cybersecurity objectives.

ISO designed this supplementary document for organizations that wish to

- Select information security controls
- Implement information security controls
- Develop information security management guidelines

#

### ISO 27701

Whereas ISO 27001 and ISO 27002 focus on cybersecurity controls, ISO 27701 contains standard guidance for managing privacy controls.

ISO views this document as an extension to their ISO 27001 and ISO 27002 security standards.

Be careful with the numbering of the ISO standards, particularly ISO 27001 and ISO 27701. They look nearly identical, but it is important to remember that ISO 27001 covers cybersecurity and ISO 27701 covers privacy.

#

### ISO 31000

ISO 31000 provides guidelines for risk management programs.

This document is not specific to cybersecurity or privacy but covers risk management in a general way so that it may be applied to any risk.

#

### Benchmarks and Secure Configuration Guides

Quality control procedures verify that an organization has sufficient security controls in place and that those security controls are functioning properly.

Every security program should include procedures for conducting regular internal tests of security controls and supplement those informal tests with formal evaluations of the organization's security program. 

Those evaluations may come in two different forms: audits and assessments.

Audits are formal reviews of an organization's security program or specific compliance issues conducted on behalf of a third party.

Audits require rigorous, formal testing of controls and result in a formal statement from the auditor regarding the entity's compliance. 

Audits may be conducted by internal audit groups at the request of management or by external audit firms, typically at the request of an organization's governing body or a regulator.

Organizations providing services to other organizations often hire an independent assessor to perform a service organization controls (SOC) audit under the American Institute for Certified Public Accountants (AICPA) Statement on Standards for Attestation Engagements 18 (SSAE 18).

There are three different categories of SOC assessment:

- **SOC 1 engagements** assess the organization's controls that might impact the accuracy of financial reporting.

- **SOC 2 engagements** assess the organization's controls that affect the security (confidentiality, integrity, and availability) and privacy of information stored in a system. SOC 2 audit results are confidential and are normally only shared outside the organization under an NDA.

- **SOC 3 engagements** also assess the organization's controls that affect the security (confidentiality, integrity, and availability) and privacy of information stored in a system. However, SOC 3 audit results are intended for public disclosure.

In addition to the three categories of SOC assessment, there are two different types of SOC report.

Both reports begin with providing a description by management of the controls put in place. T

hey differ in the scope of the opinion provided by the auditor:

- **Type 1 reports** provide the auditor's opinion on the description provided by management and the suitability of the design of the controls.

- **Type 2 reports** go further and also provide the auditor's opinion on the operating effectiveness of the controls. That is, the auditor actually confirms that the controls are functioning properly.

Assessments are less formal reviews of security controls that are typically requested by the security organization itself in an effort to engage in process improvement. 

During an assessment, the assessor typically gathers information by interviewing employees and taking them at their word, rather than preforming the rigorous independent testing associated with an audit.
