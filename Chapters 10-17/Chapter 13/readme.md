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

