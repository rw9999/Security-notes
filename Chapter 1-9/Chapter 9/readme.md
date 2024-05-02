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

