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

Administrators may then supplement this inventory with additional information about the type of system and the information it handles. This information then helps make determinations about which systems are critical and which are noncritical.

Asset inventory and **asset criticality** information helps guide decisions about the types of scans that are performed, the frequency of those scans, and the priority administrators should place on remediating vulnerabilities detected by the scan.

##

### Determining Scan Frequency

Vulnerability scanning tools allow the automated scheduling of scans to take the burden off administrators.

Administrators may designate a schedule that meets their security, compliance, and business requirements.

Administrators should configure these scans to provide automated alerting when they detect new vulnerabilities.

Many different factors influence how often an organization decides to conduct vulnerability scans against its systems:

- The organization's **risk appetite** is its willingness to tolerate risk within the environment. If an organization is extremely risk averse, it may choose to conduct scans more frequently to minimize the amount of time between when a vulnerability comes into existence and when it is detected by a scan.

- **Regulatory requirements**, such as those imposed by the Payment Card Industry Data Security Standard (PCI DSS) or the Federal Information Security Management Act (FISMA), may dictate a minimum frequency for vulnerability scans. These requirements may also come from corporate policies.

- **Technical constraints** may limit the frequency of scanning. The scanning system may only be capable of performing a certain number of scans per day, and organizations may need to adjust scan frequency to ensure that all scanscomplete successfully.
 
 - **Business constraints** may limit the organization from conducting resource-intensive vulnerability scans during periods of high business activity to avoid disruption of critical processes.

 - **Licensing limitations** may curtail the bandwidth consumed by the scanner or the number of scans that may be conducted simultaneously.

## Configuring Vulnerability Scans
