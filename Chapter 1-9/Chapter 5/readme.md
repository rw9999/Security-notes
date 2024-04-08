# Security Assessment and Testing

### Vulnerability Management

**Vulnerability management** programs play a crucial role in identifying, prioritizing, and remediating vulnerabilities in our environments

They use **vulnerability scanning** to detect new vulnerabilities as they arise and then implement a remediation workflow that addresses the highest-priority vulnerabilities.

##

### Identifying Scan Targets

Once an organization decides that it wishes to conduct vulnerability scanning and determines which, if any, regulatory requirements apply to their scans, they move on to the more detailed phases of the planning process.

The next step is to identify the systems that will be covered by the vulnerability scans. Some organizations choose to cover all systems in their scanning process, whereas others scan systems differently (or not at all) depending on the answers to many different questions, including

- What is the data classification of the information stored, processed, or transmitted by the system?

- Is the system exposed to the Internet or other public or semipublic networks?

- What services are offered by the system?

- Is the system a production, test, or development system?

Organizations also use automated techniques to identify the systems that may be covered by a scan. 

Cybersecurity professionals use scanning tools to search the network for connected systems, whether they were previously known or unknown, and to build an **asset inventory**.

Administrators may then supplement this inventory with additional information about the type of system and the information it handles. This information then helps make determinations about which systems are critical and which are non-critical.

Asset inventory and **asset criticality** information help guide decisions about the types of scans that are performed, the frequency of those scans, and the priority administrators should place on remediating vulnerabilities detected by the scan.

##

### Determining Scan Frequency

Vulnerability scanning tools allow the automated scheduling of scans to take the burden off administrators.

Administrators may designate a schedule that meets their security, compliance, and business requirements.

Administrators should configure these scans to provide automated alerting when they detect new vulnerabilities.

Many different factors influence how often an organization decides to conduct vulnerability scans against its systems:

- The organization's **risk appetite** is its willingness to tolerate risk within the environment. If an organization is extremely risk averse, it may choose to conduct scans more frequently to minimize the amount of time between when a vulnerability comes into existence and when it is detected by a scan.

- **Regulatory requirements**, such as those imposed by the Payment Card Industry Data Security Standard (PCI DSS) or the Federal Information Security Management Act (FISMA), may dictate a minimum frequency for vulnerability scans. These requirements may also come from corporate policies.

- **Technical constraints** may limit the frequency of scanning. The scanning system may only be capable of performing a certain number of scans per day, and organizations may need to adjust scan frequency to ensure that all scans complete successfully.
 
 - **Business constraints** may limit the organization from conducting resource-intensive vulnerability scans during periods of high business activity to avoid disruption of critical processes.

 - **Licensing limitations** may curtail the bandwidth consumed by the scanner or the number of scans that may be conducted simultaneously.

## Configuring Vulnerability Scans

Vulnerability management solutions provide administrators with the ability to configure many different parameters related to scans.

In addition to scheduling automated scans and producing reports, administrators may customize the types of checks performed by the scanner, provide credentials to access target servers, install scanning agents on target servers, and conduct scans from a variety of network perspectives.

It is important to conduct regular **configuration reviews** of vulnerability scanners to ensure that scan settings match current requirements.

### Scan Sensitivity Levels

Cybersecurity professionals configuring vulnerability scans should pay careful attention to the configuration settings related to the scan sensitivity level.

These settings determine the types of checks that the scanner will perform and should be customized to ensure that the scan meets its objectives while minimizing the possibility of disrupting the target environment.

Typically, administrators create a new scan by beginning with a template. As administrators create their own scan configurations, they should consider saving common configuration settings in templates to allow efficient reuse of their work, saving time and reducing errors when configuring future scans.

Administrators may also improve the efficiency of their scans by configuring the specific plug-ins that will run during each scan. Each plug-in performs a check for a specific vulnerability, and these plugins are often grouped into families based on the operating system, application, or device that they involve.

Disabling unnecessary plugins improves the speed of the scan by bypassing unnecessary checks and also may reduce the number of false positive results detected by the scanner.

**Intrusive plug-ins** perform tests that may disrupt activity on a production system or, in the worst case, damage content on those systems.

Administrators want to run these scans because they may identify problems that could be exploited by a malicious source.

At the same time, cybersecurity professionals don't want to cause problems on the organization's network and, as a result, may limit their scans to **nonintrusive plug-ins**.

One way around this problem is to maintain a test environment containing copies of the same systems running on the production network and run scans against those test systems first.

### Supplementing Network Scans

Basic vulnerability scans run over a network, probing a system from a distance. This provides a realistic view of the system's security by simulating what an attacker might see from another network vantage point

Intrusion prevention systems and other security controls that exist on the path between the scanner and the target server may affect the scan results, providing an inaccurate view of the server's security independent of those controls

Many security vulnerabilities are difficult to confirm using only a remote scan. Vulnerability scans that run over the network may detect the possibility that a vulnerability exists but be unable to confirm it with confidence, causing a false positive result that requires time-consuming administrator investigation

Modern vulnerability management solutions can supplement these remote scans with trusted information about server configurations

First, administrators can provide the scanner with credentials that allow the scanner to connect to the target server and retrieve configuration information. This information can then be used to determine whether a vulnerability exists, improving the scan's accuracy over noncredentialled alternatives. 

**Credentialed scans** may access operating systems, databases, and applications, among other sources. Credentialed scans typically only retrieve information from target servers and do not make changes to the server itself.

Typically only retrieve information from target servers and do not make changes to the server itself. Administrators should enforce the principle of least privilege by providing the scanner with a read-only account on the server

Some scanners supplement the traditional** server-based scanning** approach to vulnerability scanning with a complementary **agent-based scanning** approach

In this approach, administrators install small software agents on each target server. These agents conduct scans of the server configuration, providing an “inside-out” vulnerability scan, and then report information back to the vulnerability management platform for analysis and reporting

The agent may cause performance or stability issues.If you choose to use an agent-based approach to scanning, you should approach this concept conservatively, beginning with a small pilot deployment that builds confidence in the agent before proceeding with a more widespread deployment

### Scan Perspective

