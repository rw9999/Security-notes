# Identity and Access Management

Identities are one of the most important security layers in modern organizations. Identities, and the accounts they are connected to, allow those organizations to control who has access to their systems and services; to identify the actions that users, systems, and services are performing; and to control the rights that those accounts have and don't have

A well-designed identity and access management architecture and implementation is critical to how organizations work.

#

### Identity

Identities are the sets of claims made about a subject. Subjects are typically people, applications, devices, or organizations, but the most common application of identity is to individuals.

Identities are typically linked to information about the subject, including details that are important to the use of their identity. This information includes attributes, or information about the subject.

Attributes can include a broad range on information, from name, age, location, or job title, to physical attributes like hair and eye color or height.

Attributes are sometimes differentiated from traits. When used this way, attributes are changeable things, like the subject's title or address, whereas traits are inherent to the subject, such as height, eye color, or place of birth.

When a subject wants to use their identity, they need to use one of a number of common ways to assert or claim an identity:

- Usernames, the most commonly used means of claiming an identity. It is important to remember that usernames are  associated with an identity and are not an authentication factor themselves.

- Certificates, which can be stored on a system or paired with a storage device or security token.

- Tokens, a physical device that may generate a code, plug in via USB, or connect via Bluetooth or other means to present a certificate or other information.

- SSH keys, which are cryptographic representations of identity that replace a username and password.

- Smartcards use an embedded chip. Both contactless and physical chip reader–capable cards as well as hybrid cards are broadly deployed, and cryptographic smartcards

#

### Authentication and Authorization


The **Extensible Authentication Protocol** (EAP) is an authentication framework that is commonly used for wireless networks.

Many different implementations exist that use the EAP framework, including vendor-specific and open methods like EAP-TLS, LEAP, and EAP-TTLS. Each of these protocols implements EAP messages using that protocol's messaging standards. EAP is commonly used for wireless network authentication.

**Challenge Handshake Authentication Protocol (CHAP)** is an authentication protocol designed to provide more security than protocols like PAP

CHAP uses an encrypted challenge and three-way handshake to send credentials


![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/841c7a4d-2626-4a09-8ca3-b6ffbb01a63b)

Microsoft introduced their own version of CHAP called MS-CHAP, but vulnerabilities in both MS-CHAP versions 1 and 2 have led to it being largely replaced by other protocols.

**Password Authentication Protocol (PAP)** is a password-centric authentication protocol that was commonly used with the Point-to-Point Protocol (PPP) to authenticate users.

PAP sends unencrypted passwords, making it unsuitable for use in most modern networks.

**802.1X** is an IEEE standard for network access control (NAC), and it is used for authentication for devices that want to connect to a network.

In 802.1X systems, supplicants send authentication requests to authenticators such as network switches, access points, or wireless controllers.

Those controllers connect to an authentication server, typically via RADIUS. The RADIUS servers may then rely on a backend directory using LDAP or Active Directory as a source of identity information.

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/f152b599-b242-4dc7-b4b6-04f336c750ad)

**RADIUS (Remote Authentication Dial-in User Service)** is one of the most common authentication, authorization, and accounting (AAA) systems for network devices, wireless networks, and other services.

RADIUS can operate via TCP or UDP and operates in a client-server model.

RADIUS sends passwords that are obfuscated by a shared secret and MD5 hash, meaning that its password security is not very strong.

RADIUS traffic between the RADIUS network access server and the RADIUS server is typically encrypted using IPSec tunnels or other protections to protect the traffic

In an AAA system, users must first authenticate, typically with a username and password. The system then allows them to perform actions they are authorized to by policies or permission settings. Accounting tracks resource utilization like time, bandwidth, or CPU utilization.

**Terminal Access Controller Access Control System Plus (TACACS+)**, is a Cisco-designed extension to TACACS, the Terminal Access Controller Access Control System.

TACACS+ uses TCP traffic to provide authentication, authorization, and accounting services. It provides full-packet encryption as well as granular command controls, allowing individual commands to be secured as needed.

**Kerberos** is designed to operate on untrusted networks and uses authentication to shield its authentication traffic.

Kerberos users are composed of three main elements: the primary, which is typically the username; the instance, which helps to differentiate similar primaries; and realms, which consist of groups of users.

Realms are typically separated by trust boundaries and have distinct Kerberos key distribution centers (KDCs).

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/9501b64f-6de9-4c1c-ba8e-28296a19700d)

When a client wants to use Kerberos to access a service, the client requests an authentication ticket, or ticket-granting ticket (TGT).

An authentication server checks the client's credentials and responds with the TGT, which is encrypted using the ticket-granting service's (TGS) secret key.

When the client wants to use a service, the client sends the TGT to the TGS (which is usually also the KDC) and includes the name of the resource it wants to use.

The TGS sends back a valid session key for the service, and the client presents the key to the service to access it.

Internet-based systems often rely on a number of core technologies to accomplish authentication and authorization. These include the following:

- **Security Assertion Markup Language (SAML**) is an XML-based open standard for exchanging authentication and authorization information.

SAML is often used between identity providers and service providers for web-based applications.

Using SAML means that service providers can accept SAML assertions from a range of identity providers, making it a common solution for federated environments like those we will discuss later in this chapter.

- **OpenID** is an open standard for decentralized authentication.

OpenID identity providers can be leveraged for third-party sites using established identities.

Google, Microsoft, Amazon, and many other organizations are OpenID identity providers (IdPs).

Relying parties (RPs) redirect authentication requests to the IdP, and then receive a response back with an assertion that the user is who they claim to be due to successful authentication, and the user is logged in using the OpenID for that user.

- **OAuth** is an open standard for authorization used by many websites.

OAuth provides a method for users to determine what information to provide to third-party applications and sites without sharing credentials.

These technologies are a major part of the foundation for many webbased SSO and federation implementations.

##

### Single Sign-On

Single sign-on (SSO) systems allow a user to log in with a single identity and then use multiple systems or services without reauthenticating.

SSO systems provide significant advantages because they simplify user interactions with authentication and authorization systems, but they require a trade-off in the number of identity-based security boundaries that are in place.

This means that many organizations end up implementing single sign-on for many systems but may require additional authentication steps or use of an additional privileged account for high-security environments.

Single sign-on is commonly implemented using LDAP and Kerberos such as in Windows domains and Linux infrastructures, or via a SAML implementation for web applications and federated services.

#

### Federation

Identity providers manage the life cycle of digital identities from creation through maintenance to eventual retirement of the identity in the systems and services it supports.

Identity providers are often part of **federated identity** deployments, where they are paired with relying parties, which trust the identity provider to handle authentication and then rely on that authentication to grant access to services. Federation is commonly used for many web services, but other uses are also possible.

Here are a number of terms commonly used in federated environments that you should be aware of:

- The principal, typically a user

- Identity providers (IdPs), who provide identity and authentication services via an **attestation** process in which the IdP validates that the user is who they claim to be

- Service providers (SPs), who provide services to users whose identities have been attested to by an identity provider

In addition, the term relying party (RP) is sometimes used, with a similar meaning to a service party. An RP will require authentication and identity claims from an IdP

#

### Directory Services

Directory services are used in networks to provide information about systems, users, and other information about an organization.

Directory services like the **Lightweight Directory Access Protocol (LDAP)** are commonly deployed as part of an identity management infrastructure and offer hierarchically organized information about the organization.

They are frequently used to make available an organizational directory for email and other contact information.

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/7690815f-171a-4105-98f7-c6d74a634d86)

Since directories contain significant amounts of organizational data and may be used to support a range of services, including directory-based authentication, they must be well protected.

The same set of needs often means that directory servers need to be publicly exposed to provide services to systems or business partners who need to access the directory information. In those cases, additional security, tighter access controls, or even an entirely separate public directory service may be needed.

## Authentication Methods

Once you've claimed an identity by providing a username or some other means, your next step is to prove that the identity belongs to you. That process is the core of the authentication process.

Using a password remains the most common means of authentication, but passwords have a number of flaws. 

The first, and most important, is that passwords can be stolen and used by third parties with relative ease. Unless the owner of the password changes it, the password will remain usable by attackers. 

Passwords are also susceptible to brute-force attacks, allowing a determined attacker who can spend enough time freely using them to eventually break into a system. This has led to the use of multiple factors, preventing a lost or stolen password from allowing easy account compromise.

#

### Multifactor Authentication

One way to ensure that a single compromised factor like a password does not create undue risk is to use multifactor authentication (MFA).

There are three major type of factors:

- **Something you know**, including passwords, PINs, or the answer to a security question.

- **Something you have** like a smartcard, USB or Bluetooth token, or another object or item that is in your possession like the Titan security key

- **Something you are**, which relies on a physical characteristic of the person who is authenticating themselves. Fingerprints, retina scans, voice prints, and even your typing speed and patterns are all included as options for this type of factor.

- Somewhere you are, sometimes called a location factor, is based on your current location. GPS, network location, and other data can be used to ensure that only users who are in the location they should be can authenticate.

- Something you can do, which is used in Windows 10's Picture Password feature or gesture passwords on Android phones. This is a type of knowledge factor that requires a different form of interaction.

- Something you exhibit, which could be a behavior pattern or similar characteristic. These are typically a form of the “something you are” factors, like typing speed or similar patterns.

- Someone you know, which can include trust relationships from others.

Current attacks already focus on weak points in systems that use text messages for a second factor by cloning cellphones or redirecting SMS messages sent via VoIP systems.

Targeted attacks that can steal and quickly use a second factor by infecting mobile phones and other similar techniques will continue to be increasingly necessary for attackers to succeed in compromising accounts and thus will appear far more frequently in the near future.

#

### One-Time Passwords

One-time passwords are an important way to combat password theft and other password-based attacks

An attacker can obtain a one-time password but cannot continue using it, and it means that brute-force attacks will be constantly attempting to  identify a constantly changing target. Though it is possible that a brute-force attack could randomly match a one-time password during the time that it is valid, the likelihood of an attack like that succeeding is incredibly small, and common controls that prevent brute-force attacks will make that type of success essentially impossible.

There are two primary models for generation of one-time passwords.

The first is **time-based one-time passwords (TOTPs)**, which use an algorithm to derive a one-time password using the current time as part of the code-generation process.

The code is valid for a set period of time and then moves on to the next time-based code, meaning that even if a code is compromised it will be valid for only a relatively short period of time.

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/ee803f74-a6e2-465d-ae2f-a7bc32effd7c)

The other one-time password generation model is **HMAC**-based onetime password (HOTP).

HMAC stands for hash-based message authentication codes.

HOTP uses a seed value that both the token or HOTP code-generation application and the validation server use, as well as a moving factor.

For HOTP tokens that work when you press a button, the moving factor is a counter, which is also stored on the token and the server.

HOTP password generators like rely on an event such as pressing a button to cause them to generate a code.

Since the codes are iterative, they can be checked from the last known use of the token, with iterations forward until the current press is found.

Like TOTP solutions, authentication applications can also implement HOTP and work the same way that a hardware token implementation does.

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/cb2d8a7d-c61d-41a6-aee6-b7b8b4b4189c)

The exam outline calls tokens like these a “token key.” Thus, if you see a token or token key, you should be aware that they typically have an interchangeable meaning and that most real-world references are likely to call them a token, a hardware token, or a security token.

In addition to application and hardware tokens, a third common implementation of a one-time password system is the use of codes based on the short message service (SMS), or text message.

In this model, when a user attempts to authenticate, an SMS message is sent to their phone, and they then input that code as an additional factor for the authentication process.

In situations where hardware and software tokens as well as SMS aren't suitable, some organizations will implement a phone call–based **push notification**. Push notifications are messages sent to a user to inform them of an event, in this case an authentication attempt.

If users respond to the phone call with the requested validation—typically by pushing a specific button on the keypad—the authentication can proceed.

Phone calls suffer from a number of issues as an authentication factor, including lower speed, which can cause issues with login timeouts; the potential for hijacking of calls via a variety of means; and additional costs for the implementing organization due to phone call costs.

Although one-time passwords that are dynamically generated as they are needed are more common, at times there is a need for a one-time password that does not require a device or connectivity.

In those cases, **static codes** remain a useful option. Static codes are also algorithmically generated like other one-time passwords but are pre-generated and often printed or stored in a secure location.

This creates a new risk model, which is that the paper they are printed on could be stolen, or if they are stored electronically the file they're stored in could be lost or accessed. This would be equivalent to losing a button-press activated token or an unlocked smartphone, so static codes can be dangerous if they are not properly secured.

#

### Attacking One-Time Passwords

One-time passwords aren't immune to attack, although they can make traditional attacks on accounts that rely on acquiring passwords fail.

TOTP passwords can be stolen by either tricking a user into providing them, gaining access to a device like a phone where they are generated, or otherwise having near real-time access to them.

This means that attackers must use a stolen TOTP password immediately. 

One-time passwords sent via SMS can be redirected using a cloned SIM, or if the phone is part of a VoIP network, by compromising the VoIP system or account and redirecting the SMS factor.

# 

### Biometrics

Biometric factors are an example of the “something you are” factor, and they rely on the unique physiology of the user to validate their identity.

Some biometric technologies also count as one of the factors that the Security+ exam outline describes, because they are something you exhibit, like a voice print or gait.

Some of the most common biometric technologies include the following:

- **Fingerprints**, which check the unique patterns of ridges and valleys on your fingertips using either optical, ultrasonic, or capacitive scanners.

- **Retina scanning** uses the unique patterns of blood vessels in the retina to tell users apart.

- **Iris recognition** systems use pattern recognition and infrared imaging to uniquely identify an individual's eyes. Iris recognition can be accomplished from farther away than retina scans, making it preferable in many circumstances.

- **Facial recognition** techniques match specific features to an original image in a database.

- **Voice recognition** systems rely on patterns, rhythms, and the sounds of a user's voice itself to recognize the user.

- **Vein recognition**, sometimes called vein matching or vascular technology, uses scanners that can see the pattern of veins, often in a user's finger. Vein scanners do not need to touch the user, unlike fingerprint scanners, making them less likely to be influenced by things like dirt or skin conditions.

- **Gait** analysis measures how a person walks to identify them.

Biometric technologies are assessed based on four major measures.

The first is Type I errors, or the **false rejection** rate (FRR).

False rejection errors mean that a legitimate biometric measure was presented and the system rejected it.

Type II errors, or **false acceptance** errors, are measured as the false acceptance rate (FAR).

These occur when a biometric factor is presented and is accepted when it shouldn't be.

These are compared using a measure called the **relative operating characteristic** (ROC).

The ROC compares the FRR against the FAR of a system, typically as a graph.

For most systems, as you decrease the likelihood of false rejection, you will increase the rate of false acceptance, and determining where the accuracy of a system should be set to minimize false acceptance and prevent false rejection is an important element in the configuration of biometric systems.

The place on this chart where FAR and FRR cross over is called the **crossover error rate**.

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/333ef3bc-1c18-4970-b4cd-bcae06f5e5e3)

#

### Evaluating Biometrics

When you assess biometrics systems, knowing their FAR and FRR will help you determine their efficacy rates, or how effective they are at performing their desired function.

The FIDO Alliance sets their FRR threshold for acceptance for certification for biometric factors to 3 in 100 attempts and at 1 in 10,000 for FAR.

The Imposter Attack Presentation Match Rate (IAPMR), a measure that tackles the question of how often an attack will succeed. IAPMR is a challenging measure because it requires attacks that are designed to specifically take advantage of the weaknesses of any given biometric system.

In addition to measures like these, in the real world you have to assess the user acceptance of the biometric system.

Biometric systems must often be deployed with a backup method available for some percentage of the user population, even if they will consent to use the system.

#

### Knowledge-Based Authentication

KBA is frequently used for password resets in the form of security questions.

Knowledge-based authentication questions are also used to validate users who are creating accounts by dynamically generating questions that the account requestor can be expected to know.

In any KBA implementation, it is important that others cannot easily discover the answer, that the answer is unique, and that the answer is something that the user should be able to remember easily or will likely know.

Allowing users to set their own questions or asking about more obscure information is a more secure option.

#

### Managing Authentication

For individuals, one option that provides a high level of security is a password key (often called a security key).

These are hardware devices that support things like one-time passwords, public key cryptography for security certificates, and various security protocols like FIDO and Universal 2nd Factor (U2F). They're available in a variety of form factors and with different types of connectivity; most provide USB and/or Bluetooth.

Password vaults (often called password managers) are another common solution for authentication management.

They are software solutions that store, manage, and secure passwords and other information, allowing users to use strong passwords without memorizing dozens, or even hundreds, of individual complex passwords.

Enterprise password manager applications are widely deployed in organizations to help with the management of servers, applications, and devices, and they have additional features like logging and auditing as well as management tools to ensure that passwords are properly rotated and monitored for use and abuse.

Computers also have the ability to have built in or add-on security modules like the **Trusted Platform Module** (TPM) standard.

TPM modules or chips have a built-in cryptoprocessor used to store RSA key pairs protected by a password set by the system owner.

TPM modules can help prevent unauthorized changes to firmware and software as part of a trusted or secure boot process, and they are supported by operating systems allowing drive encryption and other cryptographic-based security features.

Although some systems, including many enterprise-class laptops, have TPM chips built in, they can also be added to systems that support them as an add-on module.

A final option you should be aware of is the use of hardware security modules (HSMs).

HSMs, which are most often found as either an independent physical device or a plug-in expansion card for a computer, integrate cryptoprocessors to securely create, store, and manage encryption keys; provide encryption and decryption services; and perform other cryptographic processing in a secure way.

Cloud providers now provide HSMs as a service, allowing a secure way to add HSMs to cloud infrastructure.

An important part of HSM design is the security of the device itself, and HSMs often carry a third-party security certification to prove that they have been assessed and validated to meet standards like FIPS-140, the U.S. government's cryptographic security standard.

## Accounts

Accounts contain information about a user, including things like rights and permissions that are associated with the account.

### Account Types

There are many types of accounts, and they can almost all be described as one of a few basic account types:

- User accounts, which can run the gamut from basic access to systems, devices, or applications to power users with broad rights and privileges.

- Privileged or administrative accounts, like the root account or members of the wheel group on Linux and Unix systems, and the Windows default Administrator account.

- Shared and generic accounts or credentials, which are often prohibited by security policies.

Although shared accounts can be useful, many organizations build delegation capabilities to allow multiple users to act in the same way or with the same rights to avoid shared account issues such as the inability to determine who was logged into the shared account or what actions each user who shares the account took.

- Guest accounts, which are provided to temporary users and which typically have very limited privileges, but are also likely to have far less information about the user who uses them, if any.

- Service accounts associated with applications and services. Service accounts should not be used for interactive logins, and many organizations have specific security policies in place to ensure service account security.

#

### Account Policies and Controls

Account policies are set to provide controls about how and when accounts can be used, to control password complexity, lifespan, and other details.

Password complexity determines the makeup of passwords.

Password complexity settings will set which characters can and cannot be used for a password, how long it must be, if it can contain words or if there are specific words it cannot contain, and any related settings that determine how complex the password will be.

The trade-off with password complexity is that requiring additional complexity can make it less likely that users will remember their password, and additional time and money can be spent on support for password resets.

Complexity may also lead users to record their passwords, potentially in an insecure location, or to reuse complex passwords so that they don't have to remember as many.

Password lifespans were also commonly used, although increasing use of MFA has led many organizations to stop requiring regular password changes.

When passwords were the sole protection for accounts, password lifespan was seen as a way to limit the maximum amount of time that a password could be exposed if it was compromised.

**Password history** settings are used to prevent **password reuse**.

Basic password histories keep track of past passwords for a given number of iterations set by the administrator. More advanced password history systems may be able to recognize if the password is too similar to previous entries to ensure that passwords with a minor change are not being used.

MFA tends to be the best solution when implemented well.

In addition to controls related to passwords, account controls can leverage other information from the login process. Common controls include the following:

In addition to controls related to passwords, account controls can leverage other information from the login process. Common controls include the following:

- The time of day, which can prevent employees from accessing systems after their shift, potentially reducing the opportunities for attackers to use the accounts when the account owner won't notice or for insiders to abuse their privileges.

**Time-based logins** are more common for shift-based or hourly workers.

- The network location of the system that is being authenticated to.

This can help prevent data from being accessed from the wrong network, or it can help preserve trust boundaries by ensuring systems authenticate only from inside a protected network.

- Geolocation data can be used to allow logins only from a geofenced area, a predetermined, GPS data–driven location or locations.

Geotagging is also sometimes used with this to tag specific data or systems with locations they can be used in.

Geographic information is also used to determine if an impossible travel time issue is occurring where a user logs in from one place and then another with enough distance between the two to ensure that the user cannot have traveled to the new location in the time given.

Account audits help to make sure that accounts are well managed, that accounts have the proper account permissions, and that appropriate controls are in place.

Account audits, which may be manual or automatic, focus on ensuring that accounts are configured as expected with appropriate permissions and rights based on the user's role or the organization's rules and standards for that type of account or user.

Finally, when accounts encounter issues, accounts can be locked out or disabled. Account lockouts are frequently automated and based on incorrect login attempts.

Lockouts may require human intervention or may automatically unlock after a period of time. 

Lockouts that unlock after some set period are called back-off algorithms, and various back-off algorithm designs exist that are intended to slow down or stop brute-force attackers while still allowing legitimate users a chance to log in to their account without calling support.

In cases where accounts need to be terminated due to compromise or lifecycle changes like termination or retirement, or if other issues occur, disabling accounts is an important option.

Disabled accounts, rather than deleted accounts, can be a cause for concern, since they may still have privileges that could be used by an attacker if the account was restored on purpose or by accident. Thus, account audits often review disabled accounts to see if they are managed well and if the organization has a habit of reenabling them or validates why they were reenabled.

#

### Privileged Access Management

Privileged access management (PAM) tools can be used to handle administrative and privileged accounts.

PAM tools focus on ensuring that the concept of least privilege is maintained by helping administrators specify only the minimum set of privileges needed for a role or task. 

PAM tools often provide more detailed, granular controls; increased audit capabilities; and additional visibility and reporting on the state of privileged accounts.

#

### Access Control Schemes

User accounts and account controls are important, but systems also implement access control schemes to determine which users, services, and programs can access various files or other objects that they host.

**Attribute-based access control (ABAC)** relies on policies that are driven by the attributes of the users.

This allows for complex rulesets based on combinations of attributes that provide users with specific rights that match the attributes they have.

Since attributes can be set in specific contexts, this also means that ABAC schemes can be very flexible. The downside of ABAC policies is that they can also be complex to manage well due to their flexibility.

Attribute-based access control schemes are useful for application security, where they are often used for enterprise systems that have complex user roles and rights that vary depending on the way and role that users interact with a system. They're also used with databases and content management systems, microservices, and APIs for similar reasons.

**Role-based access control (RBAC)** systems rely on roles that are then matched with privileges that are assigned to those roles.

This makes RBAC a popular option for enterprises that can quickly categorize employees with roles like “cashier” or “database administrator” and provide users with the appropriate access to systems and data based on those roles. 

RBAC systems boil down to three primary rules:

- Role assignment, which states that subjects can use only permissions that match a role they have been assigned.
- Role authorization, which states that the subject's active role must be authorized for the subject. This prevents subjects from taking on roles they shouldn't be able to.
- Permission authorization, which states that subjects can use only permissions that their active role is allowed to use.

Together, these three rules describe how permissions can be applied in an RBAC system. With these three rules, role hierarchies can be built that allow specific permissions to be available at the right levels based on roles in any given environment.

**Rule-based access control**, also sometimes called RBAC (and sometimes RuBAC to help differentiate it from role-based access control) is applied using a set of rules, or access control lists (ACLs), that apply to various objects or resources.

When an attempt is made to access an object, the rule is checked to see if the access is allowed. A common example of a rule-based access control is a firewall ruleset.

**Mandatory access control (MAC)** systems rely on the operating system to enforce control as set by a security policy administrator.

In a MAC implementation, users do not have the ability to grant access to file or otherwise change the security policies that are set centrally.

MAC implementations were once only found in government and military systems, but now they can be found in specific high-securitysystems like SELinux and in Windows as Mandatory Integrity Control (MIC).

**Discretionary access control (DAC)** is an access control scheme that many people are used to from their own home PCs.

The most common type of discretionary access control assigns owners for objects like files and directories, and then allows the owner to delegate rights and permissions to those objects as they desire.

Linux file permissions provide an easy example of this. The owner of a file (or directory) can set permissions that apply to the owner, the group, or the world, and they can choose to allow the file to be read, modified, or executed.

In addition to access control schemes, the Security+ exam outline covers two specific implementations of access control systems that you need to be familiar with:

- **Privileged access management** is the set of controls, tools, and processes used to handle privileges for elevated accounts and rights.

 Accounts like administrator, root, or similar high-level accounts need to be managed and secured.

 Managing administrative and privileged accounts typically starts with ensuring that least privilege is enforced to provide users and accounts with only the rights they need to perform their jobs. PAM solutions can be deployed to manage and control these accounts as part of a risk reduction strategy.

 - **Conditional access** describes the process of testing the security state of devices and users before allowing access to data, networks, or other resources.

The advantage of conditional access is that it does not simply look for permissions to provide access control. Instead, you need to have both the permissions or rights to access an object and a system or device that is sufficiently secure or trusted to access the object as well.

#

### Filesystem Permissions

Filesystem controls determine which accounts, users, groups, or services can perform actions like reading, writing, and executing (running) files.

Linux filesystem permissions are shown in file listings with the letters drwxrwxrwx, indicating whether a file is a directory, and then displaying user, group, and world (sometimes called other) permissions.

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/1e0e7136-f372-4fc2-ac2e-64a3882a6e0c)

Windows file permissions can be set using the command line or the GUI.

Note that the permissions are similar but not quite the same as those set in Linux.

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/6cd1be78-54cd-4621-a6e6-431365fee085)

The modify permission allows viewing as well as changing files or folders.

Read and execute does not allow modification or changes but does allow the files to be run, while read and write work as you'd expect them to.

Filesystem permissions are an important control layer for systems, and improperly set or insecure permissions are often leveraged by attackers to acquire data and to run applications that they should not be able to.
