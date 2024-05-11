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

