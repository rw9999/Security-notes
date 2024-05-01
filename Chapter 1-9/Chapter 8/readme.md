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

##

### Federation

