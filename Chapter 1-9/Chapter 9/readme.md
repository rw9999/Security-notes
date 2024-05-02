# Resilience and Physical Security

Building a resilient, secure infrastructure requires an understanding of the risks that your organization may face.

Natural and human-created disasters, physical attacks, and even accidents can all have a serious impact on your organization's ability to function.

Physical security can help provide greater resilience as well as protecting data and systems. Physical access to systems, networks, and devices is one of the easiest ways to bypass or overcome security controls, making physical security a key design element for secure organizations.

#

### Building Cybersecurity Resilience

Availability is a critical part of an organization's security, because systems that are offline or otherwise unavailable are not meeting business needs.

Cost, maintenance requirements, suitability to the risks that your organization faces, and other factors are factors you must take into account when building cybersecurity resilience.

One of the most common ways to build resilience is through **redundancy**—in other words, having more than one of a system, service, device, or other component.

Single points of failure—places where the failure of a single device, connection, or other element could disrupt or stop the system from functioning—must be identified and either compensated for or documented in the design.

After all your assessment work has been completed, a design is created that balances business needs, design requirements and options, and the cost to build and operate the environment.

Designs often have compromises made in them to meet cost, complexity, staffing, or other limitations based on the overall risk and likelihood  of occurrence for the risks that were identified in the assessment and design phases.

Common elements in designs for redundancy include the following:

- Geographic dispersal of systems ensures that a single disaster, attack, or failure cannot disable or destroy them.

For data centers and other facilities, a common rule of thumb is to place data centers at least 90 miles apart, preventing most common natural disasters from disabling both (or more!) data centers. This also helps ensure that facilities will not be impacted by issues with the power grid, network connectivity, and other similar issues.

- Separation of servers and other devices in data centers is also commonly used to avoid a single rack being a point of failure.

Thus, systems may be placed in two or more racks in case of a single-point failure of a power distribution unit (PDU) or even something as simple as a leak that drips down into the rack.

- Use of multiple network paths (**multipath**) solutions ensures that a severed cable or failed device will not cause a loss of connectivity.

- Redundant network devices, including multiple routers, security devices like firewalls and intrusion prevention systems, or other security appliances, are also commonly implemented to prevent a single point of failure.

    - **Load balancers**, which make multiple systems or services appear to be a single resource, allowing both redundancy and increased ability to handle loads by distributing it to more than one system. Load balancers are also commonly used to allow system upgrades by redirecting traffic away from systems that will be upgraded and then returning that traffic after they are patched or upgraded.
    - **NIC teaming**, which combines multiple network cards into a single virtual network connection. R**edundant network interface cards** (NICs) are also used to ensure connectivity in situations where a system's availability is important and multiple systems cannot be reasonably used. Redundant NICs are likely to be connected to independent network paths to ensure end-to-end reliability, whereas NIC teams will connect to the same network devices in case of a NIC failure while providing greater bandwidth.
 
- Protection of power, through the use of **uninterruptible power supply** (UPS) systems that provide battery or other backup power options for short periods of time; **generator systems** that are used to provide power for longer outages; and design elements, such as **dual-supply** or multisupply hardware, ensures that a power supply failure won't disable a server.

**Managed power distribution units** (PDUs) are also used to provide intelligent power management and remote control of power delivered inside server racks and other environments.

- Systems and storage redundancy helps ensure that failed disks, servers, or other devices do not cause an outage.

- Diversity of technologies is another way to build resilience into an infrastructure. Using different vendors, cryptographic solutions, platforms, and controls can make it more difficult for a single attack or failure to have system- or organizationwide impacts.

There is a real cost to using different technologies such as additional training, the potential for issues when integrating disparate systems, and the potential for human error that increases as complexity increases.

#

### Storage Resiliency: Backups and Replication

The use of redundant arrays of inexpensive disks (RAID) is a common solution that uses multiple disks with data either striped (spread across disks) or mirrored (completely copied), and technology to ensure that data is not corrupted or lost (parity).

RAID ensures that one or more disk failures can be handled by an array without losing data.

|RAID description|Description|Advantage|Disadvantage|
|----------------|-----------|---------|------------|
|RAID 0 - Striping| Data is spread across all drives in the array.|Better I/O performance (speed), all capacity used.|Not fault tolerant—all data lost if a drive is lost.|
|RAID 1 – Mirroring|All data is copied exactly to another drive or drives.|High read speeds from multiple drives, data available if a drive fails.|Uses twice the storage for the same amount of data.|
|RAID 5 – Striping with parity|Data is striped across drives, with one drive used for parity (checksum) of the data. Parity is spread across drives as well as data.|Data reads are fast, data writes are slightly slower. Drive failures can be rebuilt as long as only one drive fails.|Can only tolerate a single drive failure at a time. Rebuilding arrays after a drive loss can be slow and impact performance.|
|RAID 6 – Striping with double parity|Like RAID 5, but additional parity is stored on another drive.|Like RAID 5, but allows for more than one drive to fail at a time.|Slower write performance than RAID 5 as the additional parity data is managed. Rebuilding arrays after a drive loss can be slow and impact performance.|
|RAID 10 – Mirroring and striping|Data is striped across two or more drives and then mirrored to the same number of drives.|Combines the advantages and disadvantages of both RAID 0 and RAID 1.|Combines the advantages and disadvantages of both RAID 0 and RAID 1. Sometimes written as RAID 1+0.|

In addition to disk-level protections, backups and replication are frequently used to ensure that data loss does not impact an organization.

Backups are a copy of the live storage system: a **full backup**, which copies the entire device or storage system; an **incremental backup**, which captures the changes since the last backup and is faster to back up but slower to recover; or a **differential backup**, which captures the changes since the last full backup and is faster to recover but slower to back up.

Running a full backup each time a backup is required requires far more space than an incremental backup, but incremental backups need to be layered with each set of changes applied to get back to a full backup if a complete restoration is required.

Since most failures are not a complete storage failure and the cost of space for multiple full  backups is much higher, most organizations choose to implement incremental backups, typically with a full backup on a periodic basis.

A third type of backup is a **snapshot**. A snapshot captures the full state of a system or device at the time the backup is completed.

Snapshots are common for virtual machines (VMs), where they allow the machine state to be restored at the point in time that the snapshot was taken.

Snapshots can be useful to clone systems, to go back in time to a point before a patch or upgrade was installed, or to restore a system state to a point before some other event occurred.

Since they're taken live, they can also be captured while the system is running, often without significant performance impact.

Like a full backup, a snapshot can consume quite a bit of space, but most virtualization systems that perform enterprise snapshots are equipped with compression and de-duplication technology that helps to optimize space usage for snapshots.

Images are a similar concept to snapshots, but most often they refer to a complete copy of a system or server, typically down to the bit level for the drive.

This means that a restored image is a complete match to the system at the moment it was imaged.

Images are a backup method of choice for servers where complex configurations may be in use, and where cloning or restoration in a short timeframe may be desired.

Forensic images use essentially the same technology to capture a bitwise copy of an entire storage device, although they have stronger requirements around data validation and proof of secure handling.

Virtualization systems and virtual desktop infrastructure (VDI) also use images to create nonpersistent systems, which are run using a “gold master” image.

The gold master image is not modified when the nonpersistent system is shut down, thus ensuring that the next user has the same expected experience.

In addition to these types of backups, copies of individual files can be made to retain specific individual files or directories of files.

Ideally, a backup copy will be validated when it is made to ensure that the backup matches the original file. safe storage of the media that the backup copy is made on is an important element in ensuring that the backup is secure and usable.

Backup media decisions involve capacity, reliability, speed, cost, expected lifespan while storing data, how often it can be reused before wearing out, and other factors, all of which can influence the backup solution that an organization chooses.

Common choices include the following:

- Tape has historically been one of the lowest-cost-per-capacity options for large-scale backups. Magnetic tape remains in use in large enterprises, often in the form of tape robot systems that can load and store very large numbers of tapes using a few drives and several cartridge storage slots.

- Disks, either in magnetic or solid-state drive form, are typically more expensive for the same backup capacity as tape but are often faster. Disks are often used in large arrays in either a network attached storage (NAS) device or a storage area network (SAN).

- Optical media like Blu-ray disks and DVDs, as well as specialized optical storage systems, remain in use in some circumstances, but for capacity reasons they are not in common use as a largescale backup tool.

- Flash media like microSD cards and USB thumb drives continue to be used in many places for short-term copies and even longerterm backups. Though they aren't frequently used at an enterprise scale, they are important to note as a type of media that may be used for some backups.

The decision between tape and disk storage at the enterprise level also raises the question of whether backups will be **online**, and thus always available, or if they will be **offline** backups and will need to be retrieved from a storage location before they can be accessed.

The advantage of online backups is in quick retrieval and accessibility, whereas offline backups can be kept in a secure location without power and other expense required for their active maintenance.

Offline backups are often used to ensure that an organization cannot have a total data loss, whereas online backups help you respond to immediate issues and maintain operations.

You may also encounter the term “nearline” backups—backup storage that is not immediately available but that can be retrieved within a reasonable period of time, usually without a human involved. Tape robots are a common example of nearline storage, with backup tapes accessed and their contents provided on demand by the robot

Cloud backups like Amazon's Glacier and Google's Coldline provide lower prices for slower access times and provide what is essentially offline storage with a nearline access model.

These long-term archival storage models are used for data that is unlikely to be needed, and thus very slow and potentially costly retrieval is acceptable as long as bulk storage is inexpensive and reliable.

As industry moves to a software-defined infrastructure model, including the use of virtualization, cloud infrastructure, and containers, systems that would have once been backed up are no longer being backed up. Instead, the code that defines them is backed up, as well as the key data that they are designed to provide or to access.

Some organizations choose to utilize off-site storage for their backup media, either at a site they own and operate or through a third-party service like Iron Mountain, which specializes in storage of secure backups in environmentally controlled facilities.

Off-site storage, a form of geographic diversity, helps ensure that a single disaster cannot destroy an organization's data entirely. Distance considerations are also important to ensure that a single regional disaster is unlikely to harm the off-site storage.

Although traditional backup methods have used on-site storage options like tape drives, storage area networks (SANs), and network attached storage (NAS) devices, cloud and third-party off-site backup options have continued to become increasingly common.

A few important considerations come into play with cloud and off-site third-party backup options:

- Bandwidth requirements for both the backups themselves and restoration time if the backup needs to be restored partially or fully.

Organizations with limited bandwidth or locations with low bandwidth are unlikely to be able to perform a timely restoration. This fact makes off-site options less attractive if quick restoration is required, but they remain attractive from a disaster recovery perspective to ensure that data is not lost completely.

- Time to retrieve files and cost to retrieve files.

Solutions like Amazon's Glacier storage focus on low-cost storage but have higher costs for retrieval, as well as slower retrieval times. Administrators need to understand storage tiering for speed, cost, and other factors, but they must also take these costs and technical capabilities into account when planning for the use of third-party and cloud backup capabilities.

- Reliability.

Many cloud providers have extremely high advertised reliability rates for their backup and storage services, and these rates may actually beat the expected durability of local tape or disk options.

- New security models required for backups.

Separation of accounts, additional controls, and encryption of data in the remote storage location are all common considerations for use of third-party services.

Exam outline considers SAN devices in two ways:

First, as a means of replicating data, where SANs use RAID to ensure that data is not lost. Some organizations even run a backup SAN with all of the organization's data replicated to it in another location.

Second, the Security+ exam outline considers SANs as a type of backup. Here, a SAN can be looked at as a network attached array of disks. NAS devices are only mentioned under backups, not under replication, but they can be used for data replication and backups.

What's the key difference between SAN and NAS devices? A SAN typically provides block-level access to its storage, thus looking like a physical drive. NAS devices usually present data as files, although this line is increasingly blurry since SAN and NAS devices may be able to do both.

In that case, organizations may simply use SAN and NAS to describe big (SAN) or smaller (NAS) devices.

#

### Response and Recovery Controls

Recovery controls and techniques focus on returning to normal operations. Because of this, controls that allow a response to compromise or other issues that put systems into a nontrusted or improperly configured state are important to ensure that organizations maintain service availability.

An important response control in that list is the concept of **nonpersistence**. This means the ability to have systems or services that are spun up and shut down as needed.

Some systems are configured to revert to a known state when they are restarted; this is common in cloud environments where a code-defined system will be exactly the same as any other created and run with that code.

Reversion to a known state is also possible by using snapshots in a virtualization environment or by using other tools that track changes or that use a system image or build process to create a known state at startup.

One response control is the ability to return to a last-known good configuration. Windows systems build this in for the patching process, allowing a return to a checkpoint before a patch was installed.

Change management processes often rely on a last-known good configuration checkpoint, via backups, snapshots, or another technology, to handle misconfigurations, bad patches, or other issues.

When a system has been compromised, or when the operating system has been so seriously impacted by an issue that it cannot properly function, one alternative is to use live boot media. This is a bootable operating system that can run from removable media like a thumb drive or DVD.

Using live boot media means that you can boot a full operating system that can see the hardware that a system runs on and that can typically mount and access drives and other devices.

This means that repair efforts can be run from a known good, trusted operating system.

Boot sector and memory-resident viruses, bad OS patches and driver issues, and a variety of other issues can be addressed using this technique.

When loads on systems and services become high or when components in an infrastructure fail, organizations need a way to respond.

High-availability solutions including load balancing, content distribution networks, and clustered systems, provide the ability to respond to high-demand scenarios as well as to failures in individual systems.

Scalability is a common design element and a useful response control for many systems in modern environments where services are designed to scale across many servers instead of requiring a larger server to handle more workload.

You should consider two major categories of scalability:

- **Vertical scalability** requires a larger or more powerful system or device.

Vertical scalability can help when all tasks or functions need to be handled on the same system or infrastructure.

Vertical scalability can be very expensive to increase, particularly if the event that drives the need to scale is not ongoing or frequent.

There are, however, times when vertical scalability is required, such as for every large memory footprint application that cannot be run on smaller, less capable systems.

- **Horizontal scaling** uses smaller systems or devices but adds more of them.

When designed and managed correctly, a horizontally scaled system can take advantage of the ability to transparently add and remove more resources, allowing it to adjust as needs grow or shrink. 

This approach also provides opportunities for transparent upgrades, patching, and even incident response.

Moves to the cloud and virtualization have allowed scaling to be done more easily. 

Many environments support horizontal scaling with software-defined services and systems that can scale at need to meet demand, while also allowing safer patching capabilities and the ability to handle failed systems by simply replacing them with another identical replacement as needed.

Not every environment can be built using horizontally scalable systems, and not every software or hardware solution is well suited to those scenarios. At the same time, natural and human-created disasters, equipment failures, and a host of other issues can impact the ability of an organization to operate its facilities and datacenters.

When an organization needs to plan for how it would operate if its datacenter or other infrastructure hosting locations were offline, they consider site resilience options as a response control.

**Site resiliency** has historically been a major design element for organizations, and for some it remains a critical design element.

Three major types of disaster recovery sites are used for site resilience:

- Hot sites have all the infrastructure and data needed to operate the organization. Because of this, some organizations operate them full time, splitting traffic and load between multiple sites to ensure that the sites are performing properly. This approach also ensures that staff are in place in case of an emergency.
- Warm sites have some or all of the systems needed to perform the work required by the organization, but the live data is not in place. Warm sites are expensive to maintain because of the hardware costs, but they can reduce the total time to restoration because systems can be ready to go and mostly configured. They balance costs and capabilities between hot sites and cold sites.
- Cold sites have space, power, and often network connectivity, but they are not prepared with systems or data. This means that in a disaster an organization knows they would have a place to go but would have to bring or acquire systems. Cold sites are challenging because some disasters will prevent the acquisition of hardware, and data will have to be transported from another facility where it is stored in case of disaster. However, cold sites are also the least expensive option to maintain of the three types.

In each of these scenarios, the **restoration order** needs to be considered.

Restoration order decisions balance the criticality of systems and services to the operation of the organization against the need for other infrastructure to be in place and operational to allow each component to be online, secure, and otherwise running properly.

A site restoration order might include a list like the following:

1. Restore network connectivity and a bastion or shell host.
2. Restore network security devices (firewalls, IPS).
3. Restore storage and database services.
4. Restore critical operational servers.
5. Restore logging and monitoring service.
6. Restore other services as possible.

Each organization and infrastructure design will have slightly different restoration order decisions to make based on criticality to the organization's functional requirements and dependencies in the datacenter's or service's operating environment.


An increasing number of designs use the cloud to replace or work in tandem with existing recovery sites. Major cloud infrastructure vendors design across multiple geographic regions and often have multiple datacenters linked inside a region as well. This means that rather than investing in a hot site, organizations can build and deploy their infrastructure in a cloud-hosted environment, and then either use tools to replicate their environment to another region or architect (or rearchitect) their design to take advantage of multiple regions from the start.

Since cloud services are typically priced on a usage basis, designing and building an infrastructure that can be spun up in another location as needed can help with both capacity and disaster recovery scenarios.

## Physical Security Controls

Physical access to systems, facilities, and networks is one of the easiest ways to circumvent technical controls, whether by directly accessing a machine, stealing drives or devices, or plugging into a trusted network to bypass layers of network security control keeping it safe from the outside world.

### Site Security

Site security looks at the entire facility or facilities used by an organization and implements a security plan based on the threats and risks that are relevant to each specific location.

That means that facilities used by an organization in different locations, or as part of different business activities, will typically have different site security plans and controls in place.

Some organizations use **industrial camouflage** to help protect them.

A common example is the nondescript location that companies pick for their call centers. Rather than making the call center a visible location for angry customers to seek out, many are largely unmarked and otherwise innocuous.

Although security through obscurity is not a legitimate technical control, in the physical world being less likely to be noticed can be helpful in preventing many intrusions that might not otherwise happen.

Many facilities use fencing as a first line of defense. **Fences** act as a deterrent by both making it look challenging to access a facility and as an actual physical defense. Highly secure facilities will use multiple lines of fences, barbed wire or razor wire at the top, and  other techniques to increase the security provided by the fence. Fence materials, the height of the fence, where entrances are placed and how they are designed, and a variety of other factors are all taken into consideration for security fencing.

A second common physical control is the placement of bollards. Bollards are posts or other obstacles that prevent vehicles from moving through an area.

Bollards may look like posts, pillars, or even planters, but their purpose remains the same: preventing vehicle access. Some bollards are designed to be removable or even mechanically actuated so that they can be raised and lowered as needed. Many are placed in front of entrances to prevent both accidents and intentional attacks using vehicles.

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/eb7c7833-46ed-4883-ab99-247fcfc1d40e)

**Lighting** plays a part in exterior and interior security. Bright lighting that does not leave shadowed or dark areas is used to discourage intruders and to help staff feel safer. Automated lighting can also help indicate where staff are active, allowing security guards and other staff members to know where occupants are.

A newer concern for organizations is the broad use of drones and unmanned aerial vehicles (UAVs).

Drones can be used to capture images of a site, to deliver a payload, or even to take action like cutting a wire or blocking a camera.

Although drone attacks aren't a critical concern for most organizations, they are increasingly an element that needs to be considered.

Anti-drone systems include systems that can detect the wireless signals and electromagnetic emissions of drones, or the heat they produce via infrared sensors, acoustic systems that listen for the sounds of drones, radar that can detect the signature of a drone flying in the area, and of course optical systems that can recognize drones.

Once they are spotted, a variety of techniques may be used against drones, ranging from kinetic systems that seek to shoot down or disable drones, to drone-jamming systems that try to block their control signals or even hijack them.

Of course, laws also protect drones as property, and shooting down or disabling a drone on purpose may have expensive repercussions for the organization or individual who does so.

Inside a facility, physical security is deployed in layers much like you would find in a technical security implementation.

**Badges** can play a number of roles in physical security.

In addition to being used for entry access via magnetic stripe and radio frequency ID (RFID) access systems, badges also often include a picture and other information that can quickly allow personnel and guards to determine if the person is who they say they are, what areas or access they should have, and if they are an employee or guest.

This also makes badges a target for social engineering attacks by attackers who want to acquire, copy, or falsify a badge as part of their attempts to get past security.

Badges are often used with **proximity readers**, which use RFID to query a badge without requiring it to be inserted or swiped through a magnetic stripe reader.

**Alarms** and alarm systems are used to detect and alert about issues, including unauthorized access, environmental problems, and fires.

Alarm systems may be locally or remotely monitored, and they can vary significantly in complexity and capabilities. Much like alerts from computer-based systems, alarms that alert too often or with greater frequency are likely to be ignored, disabled, or worked around by staff.

**Fire suppression systems** are an important part of safety systems and help with resilience by reducing the potential for disastrous fires

One of the most common types of fire suppression system is sprinkler systems. There are four major types, including wet sprinkler systems, which have water in them all the time; dry sprinklers, which are empty until needed; pre-action sprinklers, which fill when a potential fire is detected and then release at specific sprinkler heads as they 
are activated by heat; and deluge sprinklers, which are empty, with open sprinkler heads, until they are activated and then cover an entire area.

Water-based sprinkler systems are not the only type of fire suppression system in common use. Gaseous agents, which displace oxygen, reduce heat, or help prevent the ability of oxygen and materials to combust, are often used in areas such as datacenters, vaults, and art museums where water might not be a viable or safe option. Chemical agents, including both wet and dry agents, are used as well; examples are foam-dispensing systems used in airport hangars and dry chemical fire extinguishers used in home and other places.

**Signage** may not immediately seem like a security control, but effective signage can serve a number of purposes. It can remind authorized personnel that they are in a secure area and that others who are not authorized should not be permitted to enter and should be reported if they are seen.

Signs can also serve as a deterrent control, such as those that read “authorized personnel only.” However, much like many other deterrent controls, signs act to prevent those who might casually violate the rules the sign shows, not those actively seeking to bypass the security controls an organization has in place.

Some organizations use access control vestibules (often called mantraps) as a means to ensure that only authorized individuals gain access to secure areas and that attackers do not use piggybacking attacks to enter places they shouldn't be.

An access control vestibule is a pair of doors that both require some form of authorized access to open.

The first door opens after authorization and closes, and only after it is closed can the person who wants to enter provide their authorization to open the second door. That way, a person following behind (piggybacking) will be noticed and presumably will be asked to leave or will be reported.

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/0c71ea9c-517f-4df8-984e-0e6b9eaee389)

**Locks** are one of the most common physical security controls you will encounter.

A variety of lock types are commonly deployed, ranging from traditional physical locks that use a key, push buttons, or other code entry mechanisms, to locks that use biometric identifiers such as fingerprints, to electronic mechanisms connected to computer systems with card readers or passcodes associated with them. Locks can be used to secure  spaces and devices or to limit access to those who can unlock them. Cable locks are a common solution to ensure that devices like computers or other hardware are not removed from a location.

Although locks are heavily used, they are also not a real deterrent for most determined attackers. Locks can be bypassed, picked, or otherwise disabled if attackers have time and access to the lock. 

Thus, locks are not considered a genuine physical security control. A common phrase among security professionals is “Locks keep honest people honest.”\

#

### Guards

Security guards are used in areas where human interaction is either necessary or helpful. Guards can make decisions that technical control systems cannot, and they can provide additional capabilities by offering both detection and response capabilities. Guards are commonly placed in reception areas, deployed to roam around  facilities, and stationed in security monitoring centers with access to cameras and other sensors. 

Robot sentries are relatively rare. Some robots are deployed in specific circumstances to help monitor areas, but widespread deployment of robotic sentries has not occurred yet.

Visitor logs are a common control used in conjunction with security guards.

A guard can validate an individual's identity, ensure that they enter only the areas they are supposed to, and ensure that they have signed a visitor log and that their signature matches a signature on file or on their ID card.

Each of these can be faked, however, an alert security guard can significantly increase the security of a facility.

Security guards also bring their own challenges; humans can be fallible, and social engineering attempts can persuade guards to violate policies or even to provide attackers with assistance. Guards are also relatively expensive, requiring ongoing pay, whereas technical security controls are typically installed and maintained at lower costs. Consequently, guards are a solution that is deployed only where there is a specific need for their capabilities in most organizations.

#

### Cameras and Sensors

Camera systems are a common form of physical security control, allowing security practitioners and others to observe what is happening in real-time and to capture video footage of areas for future use when conducting investigations or for other reasons. 

Cameras come in a broad range of types, including black and white, infrared, and color cameras, with each type suited to specific scenarios. 

In addition to the type of camera, the resolution of the camera, whether it is equipped with zoom lenses, and whether it has a pan/tilt/zoom (PTZ) capability are all factors in how well it works for its intended purpose and how much it will cost.

The exam focuses on two types of camera capabilities:

- **Motion recognition** cameras activate when motion occurs. These types of cameras are particularly useful in areas where motion is relatively infrequent. Motion recognition cameras, which can help conserve storage space, will normally have a buffer that will be retrieved when motion is recognized so that they will retain a few seconds of video before the motion started; that way, you can see everything that occurred.

- **Object detection ** cameras and similar technologies can detect specific objects, or they have areas that they watch for changes. These types of camera can help ensure that an object is not moved and can detect specific types of objects like a gun or a laptop.

Another form of camera system is a closed-circuit television (CCTV), which displays what the camera is seeing on a screen. Some CCTV systems include recording capabilities as well, and the distinction between camera systems and CCTV systems is increasingly blurry as technologies converge.

Common sensor systems include motion, noise, moisture, and temperature detection sensors. Motion and noise sensors are used as security sensors, or to turn on or off environment control systems based on occupancy. Temperature and moisture sensors help maintain datacenter environments and other areas that require careful control of the environment, as well as for other monitoring purposes.

This USB data blocker is a device used to ensure that USB cables can only be used to transfer power, not data when chargers and other devices cannot be trusted. An alternative is a USB power-only cable.

#

### Enhanced Security Zones and Secure Areas

Organizations frequently have a need for specific areas to have greater security than the rest of their spaces or areas.

Datacenters are one of the most obvious secure areas for most organizations, as are vaults and safes, which are protected to ensure that unauthorized personnel do not gain access to them. 

Vaults are typically room size and built in place, whereas a safe is smaller and portable, or at least movable.

Datacenters and vaults are typically designed with secure and redundant environmental controls, access controls, and additional security measures to ensure that they remain secure.

In addition to the security features that are built into data centers, environmental controls, including the use of **hot aisles** and **cold aisles**, play into their ability to safely house servers and other devices.

A hot aisle/cold aisle design places air intakes and exhausts on alternating aisles to ensure proper airflow, allowing data center designers to know where to provide cool air and where exhaust needs to be handled.

Hot and cold aisles aren't typically considered secure areas, although the data center where they are deployed usually is.

In some cases, administrative controls like two-person integrity control schemes are put in place to secure safes or vaults. In a two-person control scheme, two trusted staff members must work together to provide access—with dual keys, with passwords, or with two portions of an access control factor.

Additional isolation for systems may be provided by physical controls such as a **Faraday cage**, which blocks electromagnetic fields. 

A Faraday cage is an enclosure made up of conductive mesh that distributes charges from wireless device signals, thus stopping them. High-security facilities may be constructed as a Faraday cage, or they may have one inside them to prevent cell phone and other electronic and wireless communications from occurring. 

Faraday cages are also sometimes used to allow wireless devices to be tested inside them without impacting other production networks and devices.

Faraday cage (more properly a Faraday shield)-style bags are commercially available, often sold as a means of preventing thieves from cloning electronic key fobs for cars. 

They are also useful as part of a technique used by cell phone thieves to prevent phones from being remotely wiped. Thieves put a stolen phone into a bag or container that acts as a Faraday cage. The phone will be unable to “phone home” and can be wiped or accessed without interference.

Network security also plays a role in secure areas, including the use of a screened subnet (also frequently called a demilitarized zone [DMZ]).

Screened subnets can be logical or physical segments of a network that are used to contain systems that are accessible by the outside world or some other less secure population.

Screened subnets rely on network security devices like firewalls to provide segmentation that limits the flow of traffic into and out of the screened subnet, thus keeping higher security zones secure.

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/d3525458-e52d-4efe-8a64-04bffa3c70f0)

The network and other telecommunication lines that an organization uses are also susceptible to attack. That's where **protected cable** distribution schemes come into play.

If organizations are concerned about attacks that tap into cables or that attempt to access them through any means, they may deploy a variety of cable protection techniques. 

Though they are relatively rare in most environments, government installations and other extremely high-security facilities may use locks, secure cable conduits and channels, tamper-evident seals, and even conduit and cables that can detect attempts to access them via pressure changes, changes in shielding conductivity, or other techniques.

When network security is not sufficient, an **air-gap** design may be used.

Air-gap designs physically separate network segments, thus preventing network connectivity. Air-gapped networks require data to be physically transported, typically after careful inspection and approval to enter the secure zone.

#

### Secure Data Destruction

When data reaches the end of its lifespan, destroying the media that contains it is an important physical security measure.

Secure data destruction helps prevent data breaches, including intentional attacks like dumpster diving as well as unintentional losses through the reuse of media, systems, or other data storage devices.

|Destruction method|Description|Notes|
|------------------|-----------|-----|
|Burning|Most often done in a high-temperature incinerator. Primarily used for paper records, although some incinerators may support electronic devices.| Typically done off-site through a third-party service; leaves no recoverable materials.|
|Shredding|Can be done on-site; can support paper or devices using an industrial shredder.| Traditional paper shredders may allow for recovery of documents, even from crosscut shredded documents. For high-security environments, burning or pulping may be required.|
|Pulping|Breaks paper documents into wood pulp, removing ink. Materials can be recycled.|Completely destroys documents to prevent recovery.|
|Pulverizing|Breaks devices down into very small pieces to prevent recovery.|The size of the output material can determine the potential for recovery of data; typically pulverizing results in very small fragments of material.|
|Degaussing|Magnetically wipes data from tapes and traditional magnetic media like hard drives.|Only effective on magnetic media; will not work on SSDs, flash media, optical media, or paper.|

Physical destruction is the most secure way to ensure data destruction, but nondestructive options are often desirable in a business environment to allow for the reuse of media or devices. 

Secure drive or media wiping options can be used when the potential for exposure is low or the risks of remnant data exposure are not a significant concern for the organization.

Wiping drives using a tool like the open source Darik's Boot and Nuke (DBAN) is a common practice for organizations that want to reuse a drive.

Modern SSDs should not be wiped using tools that perform a zero wipe, random fill, or other wiping technique. Instead, SSDs should use the secure erase command if they support it.

An even better option is to encrypt the SSD in use using a full-disk encryption tool for its entire lifespan. When the drive needs to be wiped, simply deleting the encryption key ensures that the data is unrecoverable.

Why is zero wiping problematic? SSDs are overprovisioned, meaning they contain more space than they report. As they wear due to use, that extra space is put into use, with data remaining in the worn sectors that are no longer mapped. Wiping the drive will write only to the active sectors, leaving data potentially accessible using a low-level drive access tool.

A final option that many organizations choose to put into place for secure destruction is the use of third-party solutions.

Contracted document and device destruction companies will pick up and remove sensitive documents and media for shredding at their facility, or they will perform the same service on-site. Organizations may opt for a thoroughly documented destruction process, including photos of the devices and per-device destruction certification depending on their security needs. Third-party destruction services are a good fit for many organizations with typical security needs, because they ensure appropriate destruction without requiring internal investment in the tools and time to securely destroy media and systems.
