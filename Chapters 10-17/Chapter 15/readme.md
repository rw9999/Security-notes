# Digital Forensics

Digital forensics provides organizations with the investigation and analysis tools and techniques to determine what happened on a system or device.

Digital forensics may be carried out to respond to legal holds and electronic discovery requirements, in support of internal investigations, or as part of an incident response process.

Digital forensics even has a role to play in intelligence and counterintelligence efforts.

### Digital Forensic Concepts

Organizations use digital forensics techniques for tasks ranging from responding to legal cases to conducting internal investigations and supporting incident response processes. 

As a security professional, you need to know the basic concepts behind digital forensics; what digital forensics is capable of; and what tools, processes, and procedures organizations put in place to build a digital forensics capability.

A key element of digital forensics is the acquisition and analysis of digital forensic data. That data can be in the form of drives, files, copies of live memory, and any of the other multitude of digital artifacts that we create in the normal process of using computers and networks. 

Since forensic information can be found in many different places, planning forensic information gathering is crucial to having a complete and intact picture of what occurred. Gathering that forensic data is just the start of a process that involves careful documentation and detailed analysis.

Throughout the process, the creation of documentation—including what you have observed, what conclusions can be made from data, and what evidence exists to support those conclusions—is necessary in order to be successful.

You will document timelines and sequences of events, looking for clues as to what occurred and why, and you will use timestamps, file metadata, event logs, and a multitude of clues to piece together a complete picture.

The human side of digital forensics can also be important; interviews with individuals involved in the activity can provide important clues. That means you can't merely be a technical forensics expert in some cases—instead, you have to leverage your knowledge of both technology and human behaviors to complete your forensic efforts.

#

### Legal Holds and e-Discovery

In many cases, forensics starts when litigation is pending or is anticipated.

Legal counsel can send a **legal hold** or litigation hold, a notice that informs an organization that they must preserve data and records that might be destroyed or modified in the course of their normal operations.

Backups, paper documents, and electronic files of all sorts must be preserved.

A key concept for legal holds and preservation is “spoliation of evidence,” which means intentionally, recklessly, or negligently altering, destroying, fabricating, hiding, or withholding evidence relevant to legal matters. 

A legal hold gives an organization notice that they must preserve that data.

Ignoring the notice or mishandling data after the notice has been received can be a negative blow against an organization in court. 

Thus, having a strong legal hold process is important for organizations before a hold shows up.

Legal holds are often one of the first parts of an electronic discovery, or **e-discovery**, process.

Discovery processes allow each side of a legal case to obtain evidence from each other and other parties involved in the case, and e-discovery is simply an electronic discovery process.

In addition to legal cases, discovery processes are also often used for public records, Freedom of Information Act requests, and investigations.

It helps to view electronic discovery using a framework, and the Electronic Discovery Reference Model (EDRM) is a useful model for this. 

The EDRM model uses nine stages to describe the discovery process:

1. Information governance before the fact to assess what data exists and to allow scoping and control of what data needs to be provided

2. Identification of electronically stored information so that you know what you have and where it is

3. Preservation of the information to ensure that it isn't changed or destroyed

4. Collection of the information so that it can be processed and managed as part of the collection process

5. Processing of the data to remove unneeded or irrelevant information, as well as preparing it for review and analysis by formatting or collating it

6. Review of the data to ensure that it only contains what it is supposed to, and that information that should not be shared is not included

7. Analysis of the information to identify key elements like topics, terms, and individuals or organizations

8. Production of the data to provide the information to third parties or those involved in legal proceedings

9. Presentation of the data, both for testimony in court and for further analysis with experts or involved parties

One of the most important and simultaneously most challenging requirements in this process can be preservation of electronic information, particularly when data covered by a legal hold or discovery process is frequently used or modified by users in you organization.

Electronic discovery and legal hold support tools exist that can help, with abilities to capture data for users or groups under litigation hold.

They often come with desktop, mobile device, and server agents that can gather data, track changes, and document appropriate handling of the data throughout the legal hold timeframe. 

In organizations that are frequently operating under legal holds, it is not uncommon for frequent litigation targets like CEOs, presidents, and others to be in a near constant state of legal hold and discovery.

Cloud operations have made e-discovery even more complex.

Cloud vendors provide services and will not permit you to place an intrusive legal hold and discovery agent in their cloud service.

That means that as you adopt cloud services you must address how you would deal with legal holds for those services. 

Tools like Google's Vault provide both email archiving and discovery support, helping organizations to meet their discovery requirements.

## Conducting Digital Forensics

Forensic data is acquired using forensic tools like disk and memory imagers, image analysis and timelining tools, low-level editors that can display detailed information about the contents and structure of data on a disk, and other specialized tools.

The Security+ exam focuses on the key aspects of acquisition, including the order of volatility, and details of how and why data is acquired from common locations and devices.

#

### Acquiring Forensic Data

When a forensic practitioner plans to acquire data, one of the first things that they will review is the order of volatility.

The **order of volatility** documents what data is most likely to be lost due to system operations or normal processes.

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/d9ae6377-6497-4fb3-a45b-2f8e8634fa3c)

Note that frequently changing information like the state of the CPU's registers and cache is first and thus most volatile, and that information about routes, processes, and kernel statistics follows. As the list proceeds, each item is less likely to disappear quickly, with backups being the least likely to change.

Following the rder of volatility for acquisitions—unless there is a compelling and immediate reason to differ from the list—will provide a forensic analyst with the greatest likelihood of capturing data intact.

It is important to remember which items will disappear when a system is powered down or rebooted. 

In general, that occurs at position 4 for temporary files and swap space on this list. Recovering intact temporary files and data from swap space will depend on how the system was shut down and if it was rebooted successfully afterward. 

The Security+ exam expects you to be familiar with the basic concepts for acquisition of information for the following list of forensic targets:

- CPU cache and registers are rarely directly captured as part of a normal forensic effort. Although it is possible to capture some of this information using specialized hardware or software, most investigations do not need this level of detail. The CPU cache and registers are constantly changing as processing occurs, making them very volatile.

- Ephemeral data such as the process table, kernel statistics, the system's ARP cache, and similar information can be captured through a combination of memory and disk acquisition, but it is important to remember that the capture will only be of the moment in time when the acquisition is done. If events occurred in the past, this data may not reflect the state that the system was in when the event occurred.

- The content of random access memory (RAM) can be very helpful for both investigations and incident response. Memory can contain encryption keys, ephemeral data from applications, and information that may not be written to the disk but that can be useful to an investigation.

- Swap and pagefile information is disk space used to supplement physical memory. Much like capturing information from RAM, capturing the swap and pagefile can provide insight into running processes. Since it is actively used by the system, particularly on machines with less memory, it also changes more quickly than many files on disk.

- Files and data on a disk change more slowly but are the primary focus of many investigations. It is important to capture the entire disk, rather than just copy files so that you can see deleted files and other artifacts that remain resident.

- The operating system itself can contain useful information. The Windows registry is a common target for analysis since many activities in Windows modify or update the registry.

- Devices such as smartphones or tablets may contain data that can also be forensic targets.

- Firmware is a less frequently targeted forensic artifact, but knowing how to copy the firmware from a device can be necessary if the firmware was modified as part of an incident or if the firmware may have forensically relevant data. Firmware is often accessible using a hardware interface like a serial cable or direct USB connection, or via memory forensic techniques.

- Snapshots from virtual machines are an increasingly common artifact that forensic practitioners must deal with.

- Network traffic and logs can provide detailed information or clues about what was sent or received, when, and via what port and protocol amongst other useful details.

- Artifacts like devices, printouts, media, and other items related to investigations can all provide additional useful forensic data.

Regardless of the type of forensic data that is obtained or handled, it is important to maintain **chain of custody** documentation if the forensic case may result in a legal case.

In fact, some organizations apply these rules regardless of the case to ensure that a case could be supported if it was necessary. Chain of custody forms are simple sign-off and documentation forms. Each time the drive, device, or artifact is accessed, transferred, or otherwise handled, it is documented as shown on the form.

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/4c8b1f9d-d933-40f0-b3ea-407597bde917)

Evidence in court cases is typically legally admissible if it is offered to prove the facts of a case and it does not violate the law. 

To determine if evidence is admissible, criteria such as the relevance and reliability of the evidence, whether the evidence was obtained legally, and whether the evidence is authentic, are all applied. 

Evidence must be the best evidence available, and the process and procedures should stand up to challenges in the court.

In addition to these requirements, admissibility for digital forensics requires that the data be intact and unaltered and have provably remained unaltered before and during the forensic process.

Forensic analysts must be able to demonstrate that they have appropriate skills, that they used appropriate tools and techniques, and that they have documented their actions in a way that is reliable and testable via an auditable trail. 

Thus, their efforts and findings must be repeatable by a third party if necessary.

#

### Cloud Forensics

Although on-site forensics have made up the bulk of traditional forensic work, the widespread move to cloud services has created new challenges for forensic analysts.

Along with the need for tools and capabilities that support discovery needs, organizations are increasingly ensuring that they have worked with their cloud providers.

In addition to having an understanding of the high-level concerns about the ability to preserve and produce data from cloud providers that organizations must consider, the Security+ exam specifically includes three concepts:

- **Right-to-audit clauses**, which are part of the contract between the cloud service and an organization.

A right-to-audit clause provides either a direct ability to audit the cloud provider or an agreement to use a third-party audit agency. 

Many cloud providers use standard contracts and may not agree to right-to-audit clauses for smaller organizations. 

In those cases, they may instead provide access to regularly updated third-party audit statements, which may fit the needs of your organization. 

If you have specific audit requirements, you will need to address them in the contract if possible, and decide whether the ability to conduct the audit is a deciding factor in your organization's decision to adopt the cloud provider's services if not.

- **Regulatory and jurisdiction** concerns are also a significant element in the adoption of cloud services.

Regulatory requirements may vary depending on where the cloud service provider operates and where it is headquartered. 

The law that covers your data, services, or infrastructure may not be the laws that you have in your own locality, region, or country. 

In addition, jurisdictional concerns may extend beyond which law covers the overall organization. 

Cloud providers often have sitesaround the world, and data replication and other services elements mean that your data or services may be stored or used in a similarly broad set of locations. 

Local jurisdictions may claim rights to access that data with a search warrant or other legal instrument. 

Organizations that have significant concerns about this typically address it with contractual terms, through service choices that providers make available to only host data or systems in specific areas or countries, and by technical controls such as handling their own encryption keys to ensure that they know if the data is accessed.

- **Data breach notification laws**, like other regulatory elements, also vary from country to country, and in the United States notably from state to state.

Contracts often cover the maximum time that can elapse before customers are notified, and ensuring that you have an appropriate breach notification clause in place that meets your needs can be important.

Some vendors delay for days, weeks, or even months, potentially causing significant issues for customers who are unaware of the breach.

These considerations mean that acquiring forensic data from a cloudprovider is unlikely.

Although you may be able to recover forensic data from logs or from systems and infrastructure you maintain in an infrastructure as a service provider's environment, forensic data from the service itself is rarely handed over to customers. 

Therefore, organizations that use cloud services must have a plan to handle potential incidents and investigations that doesn't rely on direct forensic techniques.

#

### Regulation and Jurisdiction Issues: Nexus and Venue

Although they aren't directly covered on the exam, regulatory and jurisdictional issues also come into play with two other legal concepts. 

The first is venue, which is the location where a case is heard. Many contracts will specify venue for cases, typically in a way that is beneficial to the service provider. If you sign a contract and don't pay attention to venue, legal cases might have to be handled far away in another state. 

At the same time, nexus is the concept of connection. A common example of nexus is found in the decision of whether a company has nexus in a state or locality and must charge tax there. For years, nexus was decided on whether the company had a physical location, distribution center, or otherwise did business physically in a state.

Understanding how and why nexus may be decided can be important when you are considering laws and regulations that may impact your organization.

#

### Acquisition Tools

Acquiring a forensic copy of a drive or device requires a tool that can create a complete copy of the device at a bit-for-bit level. The Security+ exam considers a number of tools that can acquire disk images, including dd, FTK Imager, and WinHex.

In Linux, dd is a command-line utility that allows you to create images for forensic or other purposes. The dd command line takes input such as an input location ( if ), an output location ( of ), and flags that describe what you want to do, such as create a complete copy despite errors.

To copy a drive mounded as /dev/sda to a file called example.img, you can execute a command like the following:

    dd if=/dev/sda of=example.img conv=noerror,sync

Additional settings are frequently useful to get better performance, such as setting the block size appropriate for the drive.

If you want to use dd for forensic purposes, it is worth investing additional time to learn how to adjust its performance using block size settings for the devices and interfaces that you use for your forensic workstation.

If you are creating a forensic image, you will likely want to create an MD5sum hash of the image as well. 

To do that, you can run use pipes, the tee command, and md5sum :

    dd if=/dev/sda bs=4k conv=sync,noerror | tee example.img | md5sum> example.md5

FTK Imager is a free tool for creating forensic images. 

It supports raw (dd)-style format as well as SMART (ASR Data's format for their SMART forensic tool), E01 (EnCase), and AFF (Advanced Forensics Format) formats commonly used for forensic tools. 

Understanding what format you need to produce for your analysis tool and whether you may want to have copies in more than one format is important when designing your forensic process.

Physical drives, logical drives, image files, and folders, as well as multi-CD/DVD volumes are all supported by FTK Imager. In most cases, forensic capture is likely to come from a physical or logical drive.

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/afce5e43-23df-46e2-9d5c-771bd98575ae)

Note the matching and validated MD5 and SHA1 hashes, as well as confirmation that there were no bad blocks which would indicate potential data loss or problems with the drive.

In addition to drive imaging tools, forensic analysts are sometimes asked to capture live memory on a system.

In addition to FTK Imager and similar forensic imaging tools, the Security+ exam includes memdump, part of the Volatility framework for Linux memory forensics. 

Memdump is a command-line tool thatcan capture Linux memory using a simple command based on the process ID.

The final tool that the exam outline lists is WinHex, a disk editing tool that can also acquire disk images in raw format, as well as its own dedicated WinHex format.

WinHex is useful for directly reading and modifying data from a drive, memory, RAID arrays, and other filesystems.

If you have experience performing forensic analysis, you've likely noted that this set of tools is lacking major common tools, like EnCase, FTK, and the Volatility framework, as well as common open source forensic tools like the SANS SIFT distribution. You'll also notice a lack of network forensic access toolkits and information about containers and virtual machine capture in the exam outline. The Security+ exam focuses on broad concepts more than on specific tools except for a few examples like those just listed.

#

### Acquiring Network Forensic Data

Network forensics have an increasingly large role to play, whether they are for traditional wired and wireless networks, cellular networks, or others.

Since network traffic is ephemeral, capturing traffic for forensic investigation often requires a direct effort to capture and log the data in advance.

If network traffic isn't actively being logged, forensic artifacts like firewall logs, IDS and IPS logs, email server logs, authentication logs, and other secondary sources may provide information about when a device was on a network, what traffic it sent, and where it sent the traffic.

When forensic examiners do work with network traffic information, they will frequently use a packet analyzer like Wireshark to review captured network traffic.

In-depth analysis of packets, traffic flows, and metadata can provide detailed information about network behaviors and content.

The same taps, span ports, and port mirrors used for network security devices can also be useful for network forensics, allowing copies of network traffic to be sent to collection servers.

Although this can be useful, it can also result in massive amounts of data. Capturing all or selected network traffic is a process that most organizations reserve for specific purposes rather than a general practice.

Instead, most organizations end up relying on logs, metadata, traffic flow information, and other commonly collected network information to support forensic activities.

#

### Acquiring Forensic Information from Other Sources

In addition to the forensic acquisition types you have learned abou so far, two other specific types of acquisition are increasingly common.

Acquisition from virtual machines requires additional planning. 

Unlike a server, desktop, or laptop, a virtual machine is often running in a shared environment where removal of the system would cause disruption to multiple other servers and services. At the same time, imaging the entire underlying virtualization host would include more data and systems than may be needed or appropriate for the forensic investigation that is in progress. 

Fortunately, a virtual machine snapshot will provide the information that forensic analysts need and can be captured and then imported into forensic tools using available tools.

Containers have grown significantly in use and create new challenges for forensic examiners.

Since containers are designed to be ephemeral, and their resources are often shared, they create fewer forensic artifacts than a virtual or physical machine. 

In fact, though containers can be paused, capturing them and returning them to a forensically sound state can be challenging. Container forensics require additional planning, and forensic and incident response tools are becoming available to support these needs.

#

### Validating Forensic Data Integrity

Once you've acquired your forensic data, you need to make sure that you have a complete, accurate copy before you begin forensic analysis.

At the same time, documenting the **provenance** of the data and ensuring that the data and process cannot be repudiated (nonrepudiation) are also important.

The most common way to validate that a forensic copy matches an original copy is to create a hash of the copy and to create a hash of the original drive, and then compare them. If the hashes match, the forensic copy is identical to the original.

Although MD5 and SHA1 are both largely outmoded for purposes where attackers might be involved, they remain useful for quickly hashing forensic images. Providing an MD5 or SHA1 hash of both drives, along with documentation of the process and procedures used, is a common part of building the provenance of the copy. The hashes and other related information will be stored as part of the chain-of-custody and forensic documentation for the case.

Manually creating a hash of an image file or drive is as simple aspointing the hashing tool to it. Here are examples of a hash for a drive mounted as /dev/sdb on a Linux system and an image file in the current directory. The filename selected for output is drive1.hash, but it could be any filename you choose.

    md5sum /dev/sdb> drive1.hash

or
                    
    md5sum image_file.img> drive1.hash

The hash value for a drive or image can also be used as a checksum to ensure that it has not changed. Simply re-hashing the drive or image and comparing the value produced will tell you if changes have occurred because the hash will be different.

Documenting the provenance, or where an image or drive came from and what happened with it, is critical to the presentation of a forensic analysis.

Forensic suites have built-in documentation processes to help with this, but manual processes that include pictures, written notes, and documentation about the chain of custody, processes, and steps made in the creation and analysis of forensic images can yield a strong set of documentation to provide appropriate provenance information. With documentation like this, you can help ensure that inappropriate handling or processes do not result in the repudiation of the images or process, resulting in the loss of a legal case or an inability to support criminal or civil charges.

#

### Forensic Copies vs. Logical Copies

Simply copying a file, folder, or drive will result in a logical copy.

The data will be preserved, but it will not exactly match the state of the drive or device it was copied from.

When you conduct forensic analysis, it is important to preserve the full content of the drive at a bit-by-bit level, preserving the exact structure of the drive with deleted file remnants, metadata, and timestamps.

Forensic copies are therefore done differently than logical copies. 

Hashing a file may match, but hashing a logical copy and a forensic copy will provide different values, thus making logical copies inadmissible in many situations where forensic analysis may involve legal action, or unusable when changes to the drive or metadata and deleted files are critical to the investigation.

#

### Making Sure the Data Doesn't Change

The Security+ exam outline doesn't require you to know about write blockers, but forensic practitioners who need to be able to create legally admissible forensic images and reports must ensure that their work doesn't alter the drives and images they work with. That's the role of a hardware or software write blocker. Write blockers allow a drive or image to be read and accessed without allowing any writes to it. That way, no matter what you do, you cannot alter the contents of the drive in any way while conducting a forensic examination. If you show up in court and the opposing counsel asks you how you did your work and you don't mention a write blocker, your entire set of forensic findings could be at risk.

#

### Data Recovery

In addition to forensic analysis, forensic techniques may be used to recover data from drives and devices. In fact, file recovery is a common need for organizations due to inadvertent deletions and system problems or errors.

The ability to recover data in many cases relies on the fact that deleting a file from a drive or device is nondestructive.

In other words, when a file is deleted, the fastest way to make the space available is to simply delete the file's information from the drive's file index and allow the space to be reused when it is needed.

Quick formatting a drive in Windows only deletes the file index instead of overwriting or wiping the drive, and other operating systems behave similarly. So, recovering files with a recovery tool or by manual means requires reviewing the drive, finding files based on headers or metadata, and then recovering those files and file fragments.

In cases where a file has been partially overwritten, it can still be possible to recover fragments of the files.

Files are stored in blocks, with block sizes depending on the drive and operating system. If a file that is 100 megabytes long is deleted, then partially overwritten by a 25 megabyte file, 75 megabytes of the original file could potentially be recovered.

Forensic analysts rely on this when files have been intentionally deleted to try to hide evidence, and they refer to the open space on a drive as **slack space**. 

Slack space analysis is critical to forensic analysis because of the wealth of data about what has previously occurred on a drive that it can provide.

Antiforensic techniques and data security best practices are the same in this circumstance and suggest overwriting deleted data. Secure delete tools are built into many operating systems or are available as standalone tools. If a file has been deleted securely and thus overwritten, there is very little chance of recovery if the tool was successful.

#

### Forensic Suites

The Security+ exam considers a single forensic suite: Autopsy.

Autopsy is an open source forensic suite with broad capabilities.

Forensic activities with a tool like Autopsy will typically start creating a new case with information about the investigators, the case, and other details that are important to tracking investigations, and then import files into the case.

Timelining capabilities like these rely on accurate time data, and inaccurate time settings can cause problems for forensic timelines.

Incorrect time settings, particularly in machines in the same environment, can cause one machine to appear to have been impacted an hour earlier than others, leading practitioners down an incorrect path. 

Always check to make sure that the timestamps for files and time settings for machines are what you expect them to be before jumping to conclusions about what happened at a specific time.

Forensic suites have many other useful features, from distributed cracking of encryption to hash cracking, steganographic encoding detection to find data hidden in images, and a host of other capabilities that are beyond the scope of the Security+ exam.

Although the Security+ exam only deals with one computer forensic suite, there are two major commercial forensic packages that security professionals need to be aware of: FTK, the Forensic Toolkit from AccessData, and EnCase from Guidance Software. Both are complete forensic tools, including acquisition, analysis, automation and investigation tools, and reporting capabilities. Although some organizations use Autopsy, and open source tools are heavily used by analysts who need forensic capabilities for incident response, these commercial packages see heavy use in police, legal, and similar investigations. If you're interested in forensics as a path forward in your security career, you should expect to become familiar with one or both tools.

#

### Reporting

Although the analysis of digital artifacts and evidence is important to the forensic process, the report that is produced at the end is the key product.

Reports need to be useful and contain the relevant information without delving into every technical nuance and detail that the analyst may have found during the investigation.

A typical forensic report will include

- A summary of the forensic investigation and findings.

- An outline of the forensic process, including tools used and any assumptions that were made about the tools or process.

- A series of sections detailing the findings for each device or drive. Accuracy is critical when findings are shared, and conclusions must be backed up with evidence and appropriate detail.

- Recommendations or conclusions in more detail than the summary included.

Forensic practitioners may also provide a report with full detail of the analysis as part of their documentation package.

#

### Digital Forensics and Intelligence

Although digital forensics work in most organizations is primarily used for legal cases, internal investigations, and incident response, digital forensics also plays a role in both strategic intelligence and counterintelligence efforts.

The ability to analyze adversary actions and technology, including components and behaviors of advanced persistent threat tools and processes, has become a key tool in the arsenal for national defense and intelligence groups. 

At the same time, forensic capabilities can be used for intelligence operations when systems and devices are recovered or acquired, allowing forensic practitioners to recover data and provide it for analysis by intelligence organizations.

Many of the tools that are used by traditional forensic practitioners are also part of the toolset used by intelligence and counterintelligence organizations.

In addition to those capabilities, they require advanced methods of breaking encryption, analyzing software and hardware, and recovering data from systems and devices that are designed to resist or entirely prevent tampering that would be part of a typical forensic process.
