# Risk Management and Privacy

Organizations face an almost dizzying array of cybersecurity risks, ranging from the reputational and financial damage associated with a breach of personal information to the operational issues caused by a natural disaster.

The discipline of risk management seeks to bring order to the process of identifying and addressing these risks.

### Analyzing Risk

We operate in a world full of risks. If you left your home and drove to your office this morning, you encountered a large number of risks. You could have been involved in an automobile accident, encountered a train delay, or been struck by a bicycle on the sidewalk. We're aware of these risks in the back of our minds, but we don't let them paralyze us. 

Instead, we take simple precautions to help manage the risks that we think have the greatest potential to disrupt our lives.

In an **enterprise risk management (ERM)** program, organizations take a formal approach to risk analysis that begins with identifying risks, continues with determining the severity of each risk, and then results in adopting one or more **risk management** strategies to address each risk.

Before we move too deeply into the risk assessment process, let's define a few important terms that we'll use during our discussion:

- **Threats** are any possible events that might have an adverse impact on the confidentiality, integrity, and/or availability of our information or information systems.

- **Vulnerabilities** are weaknesses in our systems or controls that could be exploited by a threat.

-  **Risks** occur at the intersection of a vulnerability and a threat that might exploit that vulnerability. A threat without a corresponding vulnerability does not pose a risk, nor does a vulnerability without a corresponding threat.

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/c7ed76f3-99d6-497f-99fb-81d26d638085)

Consider the example from earlier of walking down the sidewalk on your way to work.

The fact that you are on the sidewalk without any protection is a vulnerability.

A bicycle speeding down that sidewalk is a threat.

The result of this combination of factors is that you are at risk of being hit by the bicycle on the sidewalk.

If you remove the vulnerability by parking in a garage beneath your building, you are no longer at risk for that particular threat. Similarly, if the city erects barriers that prevent bicycles from entering the sidewalk, you are also no longer at risk.

Let's consider another example drawn from the cybersecurity domain.

Organizations regularly conduct vulnerability scans designed to identify potential vulnerabilities in their environment.

One of these scans might identify a server that exposes TCP port 22 to the world, allowing brute-force SSH attempts by an attacker. 

Exposing port 22 presents a vulnerability to a brute-force attack. 

An attacker with a brute-force scanning tool presents a threat. 

The combination of the port exposure and the existence of attackers presents a risk.

In this case, you don't have any way to eliminate attackers, so you can't really address the threat, but you do have control over the services running on your systems.

If you shut down the SSH service and close port 22, you eliminate the vulnerability and, therefore, also eliminate the risk.

Of course, we can't always completely eliminate a risk because it isn't always feasible to shut down services. We might decide instead to take actions that reduce the risk.

#

### Risk Identification

The risk identification process requires identifying the threats and vulnerabilities that exist in your operating environment.

These risks may come from a wide variety of sources ranging from hackers to hurricanes. 

As you prepare for the Security+ exam, you should be familiar with the following categories of risk that are specifically mentioned in the exam objectives:

- **External risks** are those risks that originate from a source outside the organization. This is an extremely broad category of risk, including cybersecurity adversaries, malicious code, and natural disasters, among many other types of risk.

- **Internal risks** are those risks that originate from within the organization. They include malicious insiders, mistakes made by authorized users, equipment failures, and similar risks.

- **Multiparty risks** are those that impact more than one organization. For example, a power outage to a city block is a multiparty risk because it affects all of the buildings on that block. Similarly, the compromise of an SaaS provider's database is a multiparty risk because it compromises the information of many different customers of the SaaS provider.

- **Legacy systems** pose a unique type of risk to organizations. These outdated systems often do not receive security updates and cybersecurity professionals must take extraordinary measures to protect them against unpatchable vulnerabilities.

- **Intellectual property (IP) theft** risks occur when a company possesses trade secrets or other proprietary information which, if disclosed, could compromise the organization's business advantage.

- **Software compliance/licensing risks** occur when an organization licenses software from a vendor and intentionally or accidentally runs afoul of usage limitations that expose the customer to financial and legal risk.

However, you're very likely to find questions about risks that fit into these categories as you take the exam.

#

### Risk Calculation

Not all risks are equal.

Returning to the example of a pedestrian on the street, the risk of being hit by a bicycle is far more worrisome than the risk of being struck down by a meteor. 

That makes intuitive sense, but let's explore the underlying thought process that leads to that conclusion.

It's a process called risk calculation.

When we evaluate any risk, we do so by using two different factors:

- The **likelihood of occurrence**, or probability, that the risk will occur. We might express this as the percent chance that a threat will exploit a vulnerability over a specified period of time, such as within the next year.

- 
