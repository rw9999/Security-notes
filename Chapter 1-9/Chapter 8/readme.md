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

**Password Authentication Protocol (PAP)** is a password-centric authentication protocol that was commonly used with the Point-to- Point Protocol (PPP) to authenticate users.

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
