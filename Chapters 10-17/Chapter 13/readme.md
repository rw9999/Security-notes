# Wireless and Mobile Security

Significant portions of the networks in most organizations are now wireless, and wireless networks have a number of security challenges that wired networks don't. 

They broadcast their signal, and they are frequently accessible from outside of the spaces that organizations own and manage. 

Cellular and point-to-point commercial wireless networks aren't even in the control of customers at all, which means that the traffic they carry may need to be treated as if it is traversing a potentially hostile network path.

## Building Secure Wireless Networks

Wireless networks are found throughout our organizations. From enterprise networks that authenticate users and that are managed and monitored using powerful tools, to simple wireless routers used in homes and small businesses to provide connectivity to residents, customers, or guests, Wi-Fi is everywhere. 

Wi-Fi networks aren't the only type of network that you will encounter, however—Bluetooth, cellular, Zigbee, and other types of connectivity are also found in organizations.

Unlike wired networks, these wireless networks don't stop outside the walls of your organization, making wireless network security a very different challenge to secure. 

The fact that many devices have the ability to create ad hoc wireless networks, or to bridge their wired and wireless network connections, means that devices throughout your organization may also end up being paths to the network or to the device itself for malicious actors.

## Connectivity Methods

Designing a secure network often starts with a basic understanding of the type of network connectivity that you will be deploying or securing.

### Cellular

Cellular networks provide connectivity for mobile devices like cell phones by dividing geographic areas into “cells” with tower coverage allowing wireless communications between devices and towers or cell sites.

Modern cellular networks use technologies like LTE (longterm evolution) 4G and related technology and new 5G networks, which are being steadily deployed around the world.

5G requires much greater antenna density but also provides greater bandwidth and throughput. Whereas cellular providers and organizations that wanted cellular connectivity tended to place towers where coverage was needed for 4G networks, 5G networks will require much more attention to antenna deployment, which means that organizations may need to design around 5G antenna placement as part of their building and facility design efforts over time.

Cellular connectivity is normally provided by a cellular carrier rather than an organization, unlike Wi-Fi or other technologies that companies may choose to implement for themselves. 

That means that the cellular network is secure, managed, and controlled outside of your organization, and that traffic sent via a cellular connection goes through a third-party network. Cellular data therefore needs to be treated as you would an external network connection, rather than your own corporate network.

#

### Wi-Fi

The term Wi-Fi covers a range of wireless protocols that are used to provide wireless networking.

Wi-Fi primarily relies on the 2.4 GHz and 5 GHz radio bands and uses multiple channels within those bands to allow multiple networks to coexist.

Wi-Fi signals can reach to reasonably long ranges, although the frequencies Wi-Fi operates on are blocked or impeded by common obstacles like walls and trees.

Despite those impediments, one of the most important security concerns with Wi-Fi networks is that they travel beyond the spaces that organizations own or control.

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/1ab72c1c-01b1-4469-a321-86bc214a9614)

Both current and historical Wi-Fi standards, ranging from 802.11b, which was the first broadly deployed Wi-Fi standard, to 802.11ac, the most broadly deployed current standard. 802.11ax, or Wi-Fi 6, is steadily becoming more available, but organizations are likely to have a broad existing deployment of 802.11ac devices until they replace them as part of normal upgrades.

In many environments, 802.11n, 802.11g, or even older standards may still be encountered.

Fortunately, Wi-Fi protocols like WPA2 and WPA3 provide security features and functionality to help keep wireless signals secure. Those features include encryption options, protection for network frames, and authentication options.

Wi-Fi devices are most commonly deployed in either ad hoc mode, which allows devices to talk to each other directly, or in infrastructure mode, which sends traffic through a base station, or access point.

Wi-Fi networks use service set identifiers (SSIDs) to identify their network name. SSIDs can be broadcast or kept private.

#

### Bluetooth

Bluetooth is a short-range wireless standard.

Like Wi-Fi and many other technologies, it operates in the 2.4 GHz range, which is used for many different wireless protocols.

Bluetooth is primarily used for low-power, short-range (less than 100 meters and typically 5–30 meters) connections that do not have very high bandwidth needs. Bluetooth devices are usually connected in a peer-to-peer rather than a client-server model.

Since Bluetooth is designed and implemented to be easy to discover, configure, and use, it can also be relatively easy to attack.

Bluetooth does support encryption, but the encryption relies on a PIN used by both devices. 

Fixed PINs for devices like headsets reduce the security of their connection. 

Attacks against authentication, as well as the negotiated encryption keys, mean that Bluetooth may be susceptible to eavesdropping as well as other attacks.

#

### NFC

Near-field communication (NFC) is used for very short-range communication between devices.

You've likely seen NFC used forpayment terminals using Apple Pay or Google Wallet with cell phones. 

NFC is limited to about 4 inches of range, meaning that it is not used to build networks of devices and instead is primarily used for low-bandwidth, device-to-device purposes.

That doesn't mean that NFC can't be attacked, but it does mean that threats will typically be in close proximity to an NFC device. 

Intercepting NFC traffic, replay attacks, and spoofing attacks are all issues that NFC implementations need to account for.

At the same time, NFC devices must ensure that they do not respond to queries except when desired so that an attacker cannot simply bring a receiver into range and activate an NFC transaction or response.

#

### RFID

Radio frequency identification (RFID) is a relatively short-range (from less than a foot of some passive tags to about 100 meters for active tags) wireless technology that uses a tag and a receiver to exchange information.

RFID may be deployed using either active tags, which have their own power source and always send signals to be read by a reader; semi-active tags, which have a battery to power their circuits but are activated by the reader; or passive tags, which are entirely powered by the reader.

RFID tags also use one of three frequency ranges.

Low-frequency RFID is used for short-range, low-power tags and are commonly used for entry access and identification purposes, where they are scanned by a nearby reader. Low-frequency RFID is not consistent around the world, meaning that tags may not meet frequency or power requirements in other countries.

High-frequency RFID tags have a longer readable range at up to a meter under normal circumstances and can communicate more quickly. 

In fact, high-frequency RFID is used for near-field communication, and many tags support read-only, write-only, and rewritable tags.

The final frequency range is ultra-high-frequency RFID, the fastest to read and with the longest range.

This means that high frequency RFID tags are used in circumstances where readers need to be further away. Highfrequency tags have found broad implementation for inventory and antitheft purposes as well as a multitude of other uses where a tag that can be remotely queried from meters away can be useful.

Because of their small size and flexible form factor, RFID tags can be embedded in stickers, small implantable chips like those used to identify pets, and in the form of devices like tollway tags. 

RFID tags can be attacked in a multitude of ways, from simple destruction or damage of the tag so that it cannot be read, to modification of tags, some of which can be reprogrammed. Tags can be cloned, modified, or spoofed; readers can be impersonated; and traffic can be captured.

#

### Infrared

Unlike the other wireless technologies in this chapter, infrared (IR) network connections only work in line of sight.

IR networking specifications support everything from very low-bandwidth modes to gigabit speeds, including

- SIR, 115 Kbit/s
- MIR, 1.15 Mbit/s
- FIR, 4 Mbit/s
- VFIR, 16 Mbit/s
- UFIR, 96 Mbit/s
- GigaIR, 512 Mbit/s-1 Gbit/s

Since IR traffic can be captured by anything with a line of sight to it, it can be captured if a device is in the area.

Of course, this also means that unlike Wi-Fi and Bluetooth traffic, devices that are outside of the line of sight of the device typically won't be able to capture IR traffic.

Infrared connections are most frequently used for point-to-point connections between individual devices, but IR technologies that exist to create networks and groups of devices do exist.

Despite this, infrared connectivity is less frequently found in modern systems and devices, having largely been supplanted by Bluetooth and Wi-Fi.

#

### GPS

Global Positioning System (GPS), unlike the other technologies described so far, is not used to create a network where devices transmit.

Instead, it uses a constellation of satellites that send out GPS signals, which are received by a compatible GPS receiver.

While the U.S. GPS system is most frequently referred to, other systems, including the Russian GLONASS system and smaller regional systems, also exist.

GPS navigation can help position devices to within a foot of their actual position, allowing highly accurate placement for geofencing and other GPS uses.

GPS also provides a consistent time signal, meaning that GPS receivers may be integrated into network time systems.

Like other radio frequency–based systems, GPS signals can be jammed or spoofed, although attacks against GPS are uncommon in normal use. GPS jamming is illegal in the United States, but claims have been made that GPS spoofing has been used to target military drones, causing them to crash, and real-world proof-of-concept efforts have been demonstrated.

#

### USB

Although this chapter is about wireless networks and mobile devices, USB is an important connectivity method for many mobile devices.

Since USB is a direct cabled connection, it isn't subject to the same risks that a wireless network is, but it does come with its own concerns.


One of the most significant risks that USB connectivity brings to mobile devices is that the device that is connected can then access the mobile device, often as a directly mounted filesystem, and may also be able to perform software or firmware updates or otherwise make changes or gather data from the mobile device.

Some organizations ban connecting to USB chargers or using cables or systems to charge from that the organization has not preapproved or issued.

Some organizations will issue charge-only USB cables that allow charging but do not have the data pins connected inside the USB cable.

#

### What About WiMAX?

The Security+ exam doesn't cover WiMAX, a microwave-based wireless technology that is used for connectivity much like DSL or cable in areas where wireless options are desirable.

Point-to point and point-to-multipoint wireless technologies beyond those listed earlier are outside the scope of the exam, but you may encounter them in your job. 

If you do, you'll need to consider what makes those services or protocols different from those that you're used to, and plan security based on their specific needs. In the meantime, you'll continue to encounter cellular (LTE and 5G) and Wi-Fi networks far more often than WiMAX or other technologies.

#


### Wireless Network Models

The wireless technologies we have described so far operate in one of three major models: point-to-point, point-to-multipoint, or broadcast.

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/9f5246c2-797c-4361-b492-09feb465d756)

A point-to-point network connects two nodes, and transmissions between them can only be received by the endpoints.

Point-to-multipoint networks like Wi-Fi have many nodes receiving the information sent by a node. 

Broadcast designs send out information on many nodes and typically do not care about receiving a response. GPS and radio are both examples of broadcast models.

## Attacks Against Wireless Networks

One of the first things you need to consider when designing a secure network is how it could be attacked.

Attackers may pose as legitimate wireless networks, add their own wireless devices to your network, interfere with the network, use protocol flaws or attacks, or take other steps to attack your network.

### Rogue Access Points and Evil Twins

The first of these attacks that you need to know about is the evil twin attack.

An evil twin is a malicious fake access point that is set up to appear to be a legitimate, trusted network.

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/cb14ec41-fa52-444e-89ea-ef382cac87a3)

An evil twin attack where the client wireless device has opted for the evil twin access point (AP) instead of the legitimate access point. The attacker may have used a more powerful AP, placed the evil twin closer to the target, or used another technique to make the AP more likely to be the one the target will associate with.

Once a client connects to the evil twin, the attacker will typically provide Internet connectivity so that the victim does not realize that something has gone wrong.

The attacker will then capture all of the victim's network traffic and look for sensitive data, passwords, or other information that they can use.

Presenting false versions of websites, particularly login screens, can provide attackers who have successfully implemented an evil twin with a quick way to capture credentials.

Rogue access points are APs added to your network either intentionally or unintentionally.

Once they are connected to your network, they can offer a point of entry to attackers or other unwanted users. 

Since many devices have built-in wireless connectivity and may show up as an accessible network, it is important to monitor your network and facilities for rogue access points.

Most modern enterprise wireless controller systems have built-in functionality that allows them to detect new access points in areas where they are deployed.

In addition, wireless intrusion detection systems or features can continuously scan for unknown access points and then determine if they are connected to your network by combining wireless network testing with wired network logs and traffic information.

This helps separate out devices like mobile phones set up as hotspots and devices that may advertise a setup Wi-Fi network from devices that are plugged into your network and that may thus create a real threat.

#

### Attacking Wi-Fi

WPA2 preshared keys can be attacked if they are weak, and WPA passphrase hashes are generated using the SSID and its length.

Rainbow tables exist for these SSIDs matched with frequently used passwords, meaning that common network names and weak passwords can be easily leveraged.

WPA2 doesn't ensure that encrypted communications cannot be read by an attacker who acquires the preshared key. In other words, WPA2 doesn't implement perfect forward secrecy.

Other attacks exist, including attacks on authentication via MSCHAPv2, attacks on WPS, the quick single-button setup capability that many home Wi-Fi devices have built-in, flaws in the WPA2 protocol's handling of handshakes for reestablishing dropped connections, and even flaws in the newest WPA3 protocol that result in the potential for successful downgrade attacks and handshake protocol issues.

#

### Bluetooth Attacks

You need to be familiar with two types of Bluetooth attacks for the Security+ exam: **bluejacking** and **bluesnarfing**.

Bluejacking simply sends unsolicited messages to Bluetooth-enabled devices.

Bluesnarfing is unauthorized access to a Bluetooth device, typically aimed at gathering information like contact lists or other details the device contains.

Unfortunately, there aren't many security steps that can be put in place for most Bluetooth devices.

Many simply require pairing using an easily guessed code (often 0000), and then proceed to establish a long-term key that is used to secure their communications.

Unfortunately, that long-term key is used to generate session keys when combined with other public factors, thus making attacks against them possible.

Despite years of use of Bluetooth in everything from mobile devices to medical devices, wearables, and cars, the security model for Bluetooth has not significantly improved.

Therefore, your best option to secure Bluetooth devices is to turn off Bluetooth if it is not absolutely needed and to leave it off except when in use.

In addition, if devices allow a pairing code to be set, change it from the defaultpairing code and install all patches for Bluetooth devices. Unfortunately, this will leave many vulnerable devices, particularly those that are embedded or no longer supported by the software or hardware manufacturer.

#

### Bluetooth Impersonation Attacks

Bluetooth impersonation attacks (BIAS) take advantages of weaknesses in the Bluetooth specification, which means that all devices that implement Bluetooth as expected are likely to be vulnerable to them.

They exploit a lack of mutual authentication, authentication procedure downgrade options, and the ability to switch roles.

Although BIAS attacks have not yet been seen in the wild, as of May 2020 information about them had been published, leading to widespread warnings that exploits were likely to be developed.

#

### RF and Protocol Attacks

Attackers who want to conduct evil twin attacks, or who want systems to disconnect from a wireless network for any reason, have two primary options to help with that goal: disassociation attacks and jamming.

**Disassociation** describes what happens when a device disconnects from an access point.

Many wireless attacks work better if the target system can be forced to disassociate from the access point that it is using when the attack starts. That will cause the system to attempt to reconnect, providing an attacker with a window of opportunity to set up a more powerful evil twin or to capture information as the system tries to reconnect.

The best way for attackers to force a system to disassociate is typically to send a de-authentication frame, a specific wireless protocol element that can be sent to the access point by spoofing the victim's wireless MAC address.

When the AP receives it, it will disassociate the device, requiring it to then reconnect to continue.

Since management frames for networks that are using WPA2 are often not encrypted, this type of attack is relatively easy to conduct.

WPA3, however, requires protected management frames and will prevent this type of deauthentication attack from working.

Another means of attacking radio frequency networks like Wi-Fi and Bluetooth is to jam them.

Jamming will block all the traffic in the range or frequency it is conducted against.

Since jamming is essentially wireless interference, jamming may not always be intentional—in fact, running into devices that are sending out signals in the same frequency range as Wi-Fi devices isn't uncommon.

Wi-Fi deauthers are often incorrectly called jammers. A deauther will send deauthentication frames, whereas a jammer sends out powerful traffic to drown out traffic.

Jammers are generally prohibited in the United States by FCC regulations, whereas deauthers are not since they operate within typical wireless power and protocol norms.

A final type of attack against Wi-Fi networks is an **initialization vector (IV)** attack.

The original implementation of wireless security was WEP (Wired Equivalent Privacy).

WEP used a 24-bit initialization vector, which could be reverse-engineered once enough traffic from a network was captured.

After the traffic was analyzed, the initialization vector used to generate an RC4 key stream could be derived, and all traffic sent on the network could be decrypted.

Fortunately, IV attacks are no longer a concern for modern networks.

Both WPA2 and WPA3 do not use weak initialization vectors like this, making the IV attack historical knowledge.

Although initialization vector attacks are listed on the Security+ exam outline, they're unlikely to show up on the test. Even the most out-of-date networks you encounter in the real world are likely to support WPA2 at a minimum. If you do encounter a network using WEP, you'll probably find a lot of other critical security flaws due to truly ancient devices and systems as well!

#

### Designing a Network

Designing your Wi-Fi network for usability, performance, and security requires careful wireless access point (WAP) placement as well as configuration.

Tuning and placement are critical, because wireless access points have a limited number of channels to operate within, and multiple wireless access points using the same channel within range of each other can decrease the performance and overall usability of the network.

At the same time, organizations typically don't want to extend signal to places where they don't intend their network to reach. 

That means your design may need to include AP placement options that limit how far wireless signal extends beyond your buildings or corporate premises.

An important part of designing a wireless network is to conduct a site survey.

**Site surveys** involve moving throughout the entire facility or space to determine what existing networks are in place and to look at the physical structure for the location options for your access points.

In new construction, network design is often included in the overall design for the facility. Since most deployments are in existing structures, however, walking through a site to conduct a survey is critical.

Site survey tools test wireless signal strength as you walk, allowing you to match location using GPS and physically marking your position on a floorplan or map as you go.

They then show where wireless signal is, how strong it is, and what channel or channels each access point or device is on in the form of a **heatmap**.

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/2e0b6bc4-65e9-437b-802c-3552ded254c3)

Note that access points have a high signal area that drops off and that the heat maps aren't perfect circles. The building's construction and interference from other devices can influence how the wireless signal behaves.

Determining which channels your access points will use is also part of this process.

In the 2.4 GHz band, each channel is 20 MHz wide, with a 5 MHz space between. There are 11 channels for 2.4 GHz Wi- Fi deployments, resulting in overlap between channels in the 100 MHz of space allocated.



In most use, this means that channels 1, 6, and 11 are used when it is possible to control channel usage in a space to ensure that there is no overlap and thus interference between channels.

In dense urban areas or areas where other organizations may have existing Wi-Fi deployments, overlapping the channels in use onto your heatmap will help determine what channel each access point should use.

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/ff528f09-dcc9-4c1a-810e-56c4e66b4a3a)

The 2.4 GHz channels in use in North America. Additional channels are available in Japan, Indonesia, and outside of the U.S., with those areas supporting channels 12 and 13 in addition to the 11 channels U.S. networks use. 

Note the overlap between the channels, which can cause interference if access points use overlapping channels within reach of each other.

Many access points will automatically select the best channel when they are deployed.

Wireless network management software can monitor for interference and overlap problems and adjust your network using the same capabilities that they use to determine if there are new rogue access points or other unexpected wireless devices in their coverage area.

These more advanced enterprise Wi- Fi controllers and management tools can also adjust broadcast power to avoid interference or even to overpower an unwanted device.

Figuring out what access points and other devices are already in place, and what networks may already be accessible in a building or space that you intend to deploy a wireless network into, can be a challenge.

Fortunately, Wi-Fi analyzer software is used to gather all the data you need to survey and plan networks, create heatmaps, identify the best channel mapping to use in 2D and 3D models, conduct speed tests, and perform wireless client information, among other tasks. 

Although each analyzer tool may have different functionality and features, they are a critical part of the toolkit that network engineers and security professionals use to assess wireless networks.

#

### Controller and Access Point Security

Enterprise networks rely on wireless local area network (WLAN) controllers to help managed access points and the organization's wireless network.

They offer additional intelligence and monitoring; allow for software-defined wireless networks; and can provide additional services, such as blended Wi-Fi and 5G wireless roaming.

Wireless controllers can be deployed as hardware devices, as a cloud service, or as a virtual machine or software package.

Not all organizations will deploy a wireless controller. 

Small and even mid-sized organizations may choose to deploy standalone access points to provide wireless network access.

In both of these scenarios, properly securing controllers and access points is an important part of wireless network security.

Much like other network devices, both controllers and APs need to be configured to be secure by changing default settings, disabling insecure protocols and services, setting strong passwords, protecting their administrative interfaces by placing them on isolated VLANs or management networks, and by ensuring that they are regularly patched and updated.

In addition, monitoring and logging should be turned on and tuned to ensure that important information and events are logged both to the wireless controller or access point and to central management software or systems.

More advanced WLAN controllers and access points may also have advanced security features such as threat intelligence, intrusion prevention, or other capabilities integrated into them.

Depending on your network architecture and security design, you may want to leverage these capabilities, or you may choose to disable them because your network infrastructure implements those capabilities in another location or with another tool, or they do not match the needs of the network where you have them deployed.

#

### Wi-Fi Security Standards

Wi-Fi networks rely on security and certification standards to help keep them secure.

In fact, modern wireless devices can't even display the Wi-Fi trademark without being certified to a current standard like WPA2 or WPA3.

WPA2, or Wi-Fi Protected Access 2, is a widely deployed and used standard that provides two major usage modes:

- WPA-Personal, which uses a preshared key and is thus often called WPA-PSK. This allows clients to authenticate without an authentication server infrastructure.

- WPA-Enterprise relies on a RADIUS authentication server as part of an 802.1x implementation for authentication. Users can thus have unique credentials and be individually identified.

WPA2 introduced the use of the Counter Mode **Cipher Block Chaining Message Authentication Code Protocol (CCMP)**.

CCMP uses Advanced Encryption Standard (AES) encryption to provide confidentiality, delivering much stronger encryption than WEP or the wired equivalent privacy protocol used previously.

In addition to confidentiality, CCMP provides authentication for the user and access control capabilities. 

You'll note that user authentication is provided but not network authentication—that is an important addition in WPA3.

WPA3, the replacement for WPA2, has been required to be supported in all Wi-Fi devices since the middle of 2018.

WPA3 hasn't reached broad implementation in normal use due the numbers of unsupported devices in many organizations, but as devices are replaced, WPA3 deployments will become more common.

WPA3 improves on WPA2 in a number of ways depending on whether it is used in Personal or Enterprise mode.

WPA3-Personal provides additional protection for password-based authentication, using a process known as **Simultaneous Authentication of Equals (SAE)**.

SAE replaces the preshared keys used in WPA2 and requires interaction between both the client and network to validate both sides.

That interaction slows down brute-force attacks and makes them less likely to succeed.

Since SAE means that users don't have to all use the same password, and in fact allows them to choose their own, it helps with usability as well.

WPA3-Personal also implements perfect forward secrecy, which ensures that the traffic sent between the client and network is secure even if the client's password has been compromised.

Perfect forward secrecy uses a process that changes the encryption keys on an ongoing basis so that a single exposed key won't result in the entire communication being exposed. Systems using perfect forward secrecy can refresh the keys they are using throughout a session at set intervals or every time a communication is sent.

WPA3-Enterprise provides stronger encryption than WPA2, with an optional 192-bit mode, and adds authenticated encryption and additional controls for deriving and authenticating keys and encrypting network frames. WPA3 thus offers numerous security advantages over existing WPA2 networks.

#

### Wireless Authentication

Although the security protocols and standards that a network uses are important, it is also critical to control access to the network itself. Organizations have a number of choices when it comes to choosing how they provide access to their networks.

The Security+ exam outline includes three major types of authentication in modern Wi-Fi networks:

- Open networks, which do not require authentication but that often use a **captive portal** to gather some information from users who want to use them.

Captive portals redirect traffic to a website or registration page before allowing access to the network. Open networks do not provide encryption, leaving user data at risk unless the traffic is sent via secure protocols like HTTPS.

- Use of preshared keys (PSKs) requires a passphrase or key that is shared with anybody who wants to use the network. This allows traffic to be encrypted but does not allow users to be uniquely identified.

- Enterprise authentication relies on a RADIUS server and utilizes an Extensible Authentication Protocol (EAP) for authentication.

You may have noticed that the authentication types on the exam outline match WPA2.

WPA3-Personal replaces the WPA2-PSK authentication mode with password-based authentication, where users can choose passwords, and implements perfect forward secrecy to keep traffic secure.

WPA3-Enterprise continues to use RADIUS but improves the encryption and key management features built into the protocol, and provides greater protection for wireless frames.

Open Wi-Fi networks also get an upgrade with the Wi-Fi Enhanced Open certification, which uses opportunistic wireless encryption (OWE) to provide encrypted Wi-Fi on open networks when possible—a major upgrade from the unencrypted open networks used with WPA2.

#

### Wireless Authentication Protocols

802.1x is an IEEE standard for access control and is used for both wired and wireless devices.

In wireless networks, 802.1x is used to integrate with RADIUS servers, allowing enterprise users to authenticate and gain access to the network.

Additional actions can be taken based on information about the users, such as placing them in groups or network zones, or taking other actions based on attributes once the user has been authenticated.

Wi-Fi networks rely on IEEE 802.1x and various versions of EAP.

EAP is used by 802.1x as part of the authentication process when devices are authenticating to a RADIUS server.

There are many EAP variants because EAP was designed to be extended, as the name implies.

Here are common EAP variants that you should be aware of:

- **Protected Extensible Authentication Protocol (PEAP)** authenticates servers using a certificate and wraps EAP using a TLS tunnel to keep it secure. Devices on the network use unique encryption keys, and Temporal Key Integrity Protocol (TKIP) is implemented to replace keys on a regular basis.

- **Flexible Authentication via Secure Tunneling Extensible Authentication Protocol (EAP-FAST)** is a Cisco-developed protocol that improved on vulnerabilities in the Lightweight Extensible Authentication Protocol (LEAP). EAP-FAST is focused on providing faster reauthentication while devices are roaming. EAP-FAST works around the public key exchanges that slow down PEAP and EAP-TLS by using a shared secret (symmetric) key for reauthentication. EAP-FAST can use either preshared keys or dynamic keys established using public key authentication.

- **Extensible Authentication Protocol-Transport Layer Security (EAP-TLS)** implements certificate-based authentication as well as mutual authentication of the device and network. It uses certificates on both client and network device to generate keys that are then used for communication. EAP-TLS is used less frequently due to the certificate management challenges for deploying and managing certificates on large numbers of client devices.

- **EAP Tunneled Transport Layer Security (EAP-TTLS)** extends EAP-TLS, and unlike EAP-TLS, it does not require that client devices have a certificate to create a secure session. This removes the overhead and management effort that EAP-TLS requires to distribute and manage endpoint certificates while still providing TLS support for devices. A concern for EAP-TTLS deployments is that EAP-TTLS can require additional software to be installed on some devices, whereas PEAP, which provides similar functionality, does not. EAP-TTLS does provide support for some less secure authentication mechanisms, meaning that there are times where it may be implemented due to specific requirements.

When organizations want to work together, RADIUS servers can be federated to allow individuals from other organizations to authenticate to remote networks using their home organization's accounts and credentials.

Federating RADIUS servers like this requires trust to be established between the RADIUS servers as part of a federation.

Many higher education institutions provide a federated authentication service for wireless called eduroam, which allows students, faculty, and staff from any eduroam institution to authenticate and use the networks at any other eduroam supporting organization. Of course, RADIUS servers can be federated in a single organization as well if there are multiple RADIUS domains.

## Managing Secure Mobile Devices

Organizations use a wide variety of mobile devices, ranging from phones and tablets to more specialized devices. As you consider how your organization should handle them, you need to plan for your deployment and management model, whether you will use a mobile device management tool, and what 
security options and settings you will put in place.

### Mobile Device Deployment Methods

When organizations use mobile devices, one important design decision is the deployment and management model that will be selected.

The most common options are BYOD, or bring your own device; CYOD, or choose your own device; COPE, or corporate-owned, personally enabled; and fully corporate-owned.

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/5e5fcadc-92d6-455d-8ca3-90fca04673fb)


#

### Mobile Device Management

Mobile devices can be a challenge to manage, particularly due to operating system limitations, variability between hardware manufacturers, carrier settings, and operating system versions.

Many mobile devices are intended to be used by individuals and don't have the broad set of built-in controls that more business-oriented devices and software typically have. When you add in the wide variety of device deployment models, security practitioners face real challenges in an increasingly mobile device–focused environment.

Thus, when administrators and security professionals need to manage mobile devices, they frequently turn to mobile device management (MDM) or unified endpoint management (UEM) tools.

MDM tools specifically target devices like Android and iOS phones, tablets, and other similar systems.

UEM tools combine mobile devices, desktops and laptops, and many other types of devices in a single management platform.

A third class of tools known as mobile application management (MAM) tools focuses specifically on the applications that are deployed to mobile devices.

Common features include application delivery, configuration, update and version management, performance monitoring and analytics, logging, and data gathering, as well as various controls related to users and authentication. 

Although MAM products are in use in some organizations, they are becoming less common as more full-featured MDM and UEM tools take over the market to provide more control of mobile devices.

In addition to MDM, UEM, and MAM tools, you may encounter enterprise mobility management (EMM) tools. The Security+ exam doesn't cover those, but you should be aware you may encounter that acronym too. EMM tools tend to have a tighter focus on enterprise data, but their focus has changed from managing that data on mobile devices to allowing mobility as a business practice for users across a broad range of platforms while keeping enterprise data secure.

Regardless of the type of tool you choose, there are a number of features your organization may use to ensure that your mobile devices and the data they contain are secure.

Although the following list isn't a complete list of every feature available in MDM, UEM, and MAM tools, you need to know about each of them, and why you might want to have it, to be ready for the exam.

- Application management features are important to allow enterprise control of applications. These features may include deploying specific applications to all devices; limiting which applications can be installed; remotely adding, removing, or changing applications and settings for them; or monitoring application usage.

- Content management (sometimes called MCM, or mobile content management) ensures secure access and control of organizational files, including documents and media on mobile devices. A major concern for mobile device deployments is the combination of organizational data and personal data on BYOD and shared-use devices. Content management features lock away business data in a controlled space and then help manage access to that data. In many cases, this requires use of the MDM's application on the mobile device to access and use the data.

- Remote-wipe capabilities are used when a device is lost or stolen, or when the owner is no longer employed by the organization. It is important to understand the difference between a full device wipe and wiping tools that can wipe only the organizational data and applications that have been deployed to the device. In environments where individuals own the devices, remote wipe can create liability and other issues if it is used and wipes the device. At the same time, remote wipe with a confirmation process that lets you know when it has succeeded is a big part of helping protect organizational data.

Remote-wipe capabilities will work only if the device can receive the command to perform the wipe. This means that thieves and attackers who want to steal your data will immediately place the device in airplane mode or will isolate the phone using an RF-blocking bag or other container to ensure that the device can't send or receive Bluetooth, Wi-Fi, or cellular signals. A smart attacker can prevent remote wipes and may be able to gain access to your data. That's when device encryption, strong passcodes, and the underlying security of the operating system become even more important.

- Geolocation and geofencing capabilities allow you to use the location of the phone to make decisions about its operation. Some organizations may only allow corporate tablets to be used inside corporate facilities to reduce the likelihood of theft or data access outside their buildings. Other organizations may want devices to wipe themselves if they leave a known area. Geolocation can also help locate lost devices, in addition to the many uses for geolocation that we are used to in our daily lives with mapping and similar tools.

- Screen locks, passwords, and PINs are all part of normal device security models to prevent unauthorized access. Screen lock time settings are one of the most frequently set security options for basic mobile device security. Much like desktops and laptops, mobile device management tools also set things like password length, complexity, and how often passwords or PINs must be changed.

- Biometrics are widely available on modern devices, with fingerprints and facial recognition the most broadly adopted and deployed. Biometrics can be integrated into mobile device management capabilities so that you can deploy biometric authentication for users to specific devices and leverage biometric factors for additional security or ease of use.

- Context-aware authentication goes beyond PINs, passwords, and biometrics to better reflect user behavior. Context may include things like location, hours of use, and a wide range of other behavioral elements that can determine whether a user should be able to log in.

- Containerization is an increasingly common solution to handling separation of work and personal-use contexts on devices. Using a secure container to run applications, store data, and otherwise keep the use of a device separate greatly reduces the risk of cross-contamination and exposure. In many MDM models, applications use wrappers to run them, helping keep them separate and secure. In others, a complete containerization environment is run as needed.

- Storage segmentation can be used to keep personal and business data separate as well. This may be separate volumes or even separate encrypted volumes that require specific applications, wrappers, or containers to access them. In fact, storage segmentation and containerization or wrapper technology are often combined to better implement application and separation.

- Full-device encryption (FDE) remains the best way to ensure that stolen or lost devices don't result in a data breach. When combined with remote-wipe capabilities and strong authentication requirements, FDE can provide the greatest chance of a device resisting data theft.

- Push notifications may seem like an odd inclusion here, but sending messages to devices can be useful in a number of scenarios. You may need to alert a user to an issue or ask them to perform an action. Or you may want to communicate with someone who found a lost device or tell a thief that the device is being tracked. Thus, having the ability to send messages from a central location can be a useful tool in an MDM or UEM system.

UEM and MDM tools may also include features like per-application VPN to keep application data secure when that application is used, onboarding tools to help with BYOD environments, and advanced threat detection and response capabilities.

