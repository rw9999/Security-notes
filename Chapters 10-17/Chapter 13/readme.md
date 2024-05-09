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

