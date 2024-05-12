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

- The magnitude of the **impact** that the risk will have on the organization if it does occur. We might express this as the financial cost that we will incur as the result of a risk, although there are other possible measures.

Using these two factors, we can assign each risk a conceptual score by combining the probability and the magnitude. 

This leads many risk analysts to express the severity of a risk using the formula:

Risk Severity = Likelihood * Impact

It's important to point out that this equation does not always have to be interpreted literally. Although you may wind up multiplying these values together in some risk assessment processes, it's best to think of this conceptually as combining the likelihood and impact to determine the severity of a risk.

When we assess the risks of being struck by a bicycle or a meteor on the street, we can use these factors to evaluate the risk severity.

There might be a high probability that we will be struck by a bicycle. That type of accident might have a moderate magnitude, leaving us willing to consider taking steps to reduce our risk. 

Being struck by a meteor would clearly have a catastrophic magnitude of impact, but the probability of such an incident is incredibly unlikely, leading us to acknowledge the risk and move on without changing our behavior.

The laws and regulations facing an industry may play a significant role in determining the impact of a risk.

For example, an organization subject to the European Union's GDPR faces significant fines if they have a data breach affecting the personal information of EU residents. The size of these fines would factor significantly into the impact assessment of the risk of a privacy breach. Organizations must, therefore, remain current on the regulations that affect their risk posture.

#

### Risk Assessment

Risk assessments are a formalized approach to risk prioritization that allows organizations to conduct their reviews in a structured manner.

Risk assessments follow two different analysis methodologies:

- **Quantitative risk assessments** use numeric data in the analysis, resulting in assessments that allow the very straightforward prioritization of risks.
  
- **Qualitative risk assessments** substitute subjective judgments and categories for strict numerical analysis, allowing the assessment of risks that are difficult to quantify.

As organizations seek to provide clear communication of risk factors to stakeholders, they often combine elements of quantitative and qualitative risk assessments. Let's review each of these approaches.

#

### Quantitative Risk Assessment

Most quantitative risk assessment processes follow a similar methodology that includes the following steps:

1.  **Determine the asset value (AV)** of the asset affected by the risk. This asset value (AV) is expressed in dollars, or other currency, and may be determined using the cost to acquire the asset, the cost to replace the asset, or the depreciated cost of the asset, depending on the organization's preferences.

2. **Determine the likelihood that the risk will occur**. Risk analysts consult subject matter experts and determine the likelihood that a risk will occur in a given year. This is expressed as the number of times the risk is expected each year and is described as the **annualized rate of occurrence** (ARO). A risk that is expected to occur twice a year has an ARO of 2.0, whereas a risk that is expected once every one hundred years has an ARO of 0.01.

3. **Determine the amount of damage that will occur to the asset if the risk materializes**. This is known as the exposure factor (EF) and is expressed as the percentage of the asset expected to be damaged. The exposure factor of a risk that would completely destroy an asset is 100 percent, whereas a risk that would damage half of an asset has an EF of 50 percent.

4. **Calculate the single loss expectancy**. The single loss expectancy (SLE) is the amount of financial damage expected each time a risk materializes. It is calculated by multiplying the AV by the EF.

5. **Calculate the annualized loss expectancy**. The annualized loss expectancy (ALE) is the amount of damage expected from a risk each year. It is calculated by multiplying the SLE and the ARO.

It's important to note that these steps assess the quantitative scale of a single risk: that is one combination of a threat and a vulnerability.

Organizations conducting quantitative risk assessments would repeat this process for each threat/vulnerability combination.

Let's walk through an example of a quantitative risk assessment.

Imagine that you are concerned about the risk associated with a denial-of-service (DoS) attack against your email server. Your organization uses that server to send email messages to customers offering products for sale. It generates $1,000 in sales per hour that
it is in operation. 

After consulting threat intelligence sources, you believe that a DoS attack is likely to occur three times a year and last for three hours before you are able to control it.

The asset in this case is not the server itself, because the server will not be physically damaged. The asset is the ability to send email and you have already determined that it is worth $1,000 per hour. The asset value for three hours of server operation is, therefore, $3,000.

Your threat intelligence estimates that the risk will occur three times per year, making your annualized rate of occurrence 3.0.

After consulting your email team, you believe that the server would operate at 10 percent capacity during a DoS attack, as some legitimate messages would get out. Therefore, your exposure factor is 90 percent, because 90 percent of the capacity would be consumed by the attack.

Your single loss expectancy is calculated by multiplying the asset value ($3,000) by the exposure factor (90 percent) to get the expected loss during each attack. This gives you an SLE of $2,700.

Your annualized loss expectancy is the product of the SLE ($2,700) and the ARO (3.0), or $8,100.

Be prepared to explain the terminology of quantitative risk assessment and perform these calculations when you take the Security+ exam. When you encounter these questions, watch out for scenarios that provide you with more information than you may need to answer the question. Question writers 
sometimes provide extra facts to lead you astray!

Organizations can use the ALEs that result from a quantitative risk assessment to prioritize their remediation activities and determine the appropriate level of investment in controls that mitigate risks.

For example, it would not normally make sense (at least in a strictly financial sense) to spend more than the ALE on an annual basis to protect against a risk. In the previous example, if a DoS prevention service would block all of those attacks, it would make financial sense to purchase it if the cost is less than $8,100 per year.

#

### Qualitative Risk Assessment

Quantitative techniques work very well for evaluating financial risks and other risks that can be clearly expressed in numeric terms.

Many risks, however, do not easily lend themselves to quantitative analysis. For example, how would you describe reputational damage, public health and safety, or employee morale in quantitative terms? 

You might be able to draw some inferences that tie these issues back to financial data, but the bottom line is that quantitative techniques simply aren't well suited to evaluating these risks.

Qualitative risk assessment techniques seek to overcome the limitations of quantitative techniques by substituting subjective judgment for objective data.

Qualitative techniques still use the same probability and magnitude factors to evaluate the severity of a risk but do so using subjective categories.

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/227690b2-ddb3-49cc-a497-6d7a5b06d170)'

For example, the picture shows a simple qualitative risk assessment that evaluates the probability and magnitude of several risks on a subjective Low/Medium/High scale. Risks are placed on this chart based on the judgments made by subject matter experts.

Although it's not possible to directly calculate the financial impact of risks that are assessed using qualitative techniques, this risk assessment scale makes it possible to prioritize risks.

For example, reviewing the risk assessment in the picture, we can determine that the greatest risks facing this organization are stolen unencrypted devices and spearphishing attacks. 

Both of these risks share a high probability and high magnitude of impact. 

If we're considering using funds to add better physical security to the data center, this risk assessment informs us that our time and money would likely be better spent on full disk encryption for mobile devices and a secure email gateway.

Many organizations combine quantitative and qualitative techniques to get a well-rounded picture of both the tangible and intangible risks that they face.

#

### Supply Chain Assessment

When evaluating the risks to your organization, don't forget about the risks that occur based on third-party relationships.

You rely on many different vendors to protect the confidentiality, integrity, and availability of your data. Performing vendor due diligence is a crucial security responsibility.

For example, how many cloud service providers handle your organization's sensitive information? Those vendors become a crucial part of your supply chain from both operational and security perspectives. If they don't have adequate security controls in place, your data is at risk

Similarly, the hardware that you use in your organization comes through a supply chain as well. How certain are you that it wasn't tampered with on the way to your organization?

Documents leaked by former NSA contractor Edward Snowden revealed that the U.S. government intercepted hardware shipments to foreign countries and implanted malicious code deep within their hardware.

Performing hardware source authenticity assessments validates that the hardware you received was not tampered with after leaving the vendor.

#

### Managing Risk

With a completed risk assessment in hand, organizations can then turn their attention to addressing those risks. 

Risk management is the process of systematically addressing the risks facing an organization. 

The risk assessment serves two important roles in the risk management process:

- The risk assessment provides guidance in prioritizing risks so that the risks with the highest probability and magnitude are addressed first.

- Quantitative risk assessments help determine whether the potential impact of a risk justifies the costs incurred by adopting a risk management approach.

Risk managers should work their way through the risk assessment and identify an appropriate management strategy for each risk included in the assessment. 

They have four strategies to choose from: risk mitigation, risk avoidance, risk transference, and risk acceptance.

#

### Risk Mitigation

Risk mitigation is the process of applying security controls to reduce the probability and/or magnitude of a risk.

Risk mitigation is the most common risk management strategy and the vast majority of the work of security professionals revolves around mitigating risks through the design, implementation, and management of security controls. 

Many of these controls involve engineering tradeoffs between functionality, performance, and security.

When you choose to mitigate a risk, you may apply one security control or a series of security controls.

Each of those controls should reduce the probability that the risk will materialize, the magnitude of the risk should it materialize, or both the probability and magnitude.

In our first scenario, we are concerned about the theft of laptops from our organization. If we want to mitigate that risk, we could choose from a variety of security controls.

For example, purchasing cable locks for laptops might reduce the probability that a theft will occur.

We could also choose to purchase a device registration service that provides tamperproof registration tags for devices, such as the STOP tags.

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/913e1e38-0a52-46cc-b3a8-f5ce8be83dc7)

These tags provide a prominent warning to potential thieves when attached to a device.

This serves as a deterrent to theft, reducing the probability that the laptop will be stolen in the first place. If a thief does steal the device and removes the tag, it leaves the permanent residue.

Anyone finding the device is instructed to contact the registration vendor for instructions, reducing the potential impact of the theft if the device is returned.

In our second scenario, a DDoS attack against an organization's website, we could choose among several mitigating controls.

For example, we could simply purchase more bandwidth and server capacity, allowing us to absorb the bombardment of a DDoS attack and thus reducing the impact of an attack. 

We could also choose to purchase a third-party DDoS mitigation service that prevents the traffic from reaching our network in the first place, thus reducing the probability of an attack.

#

### Risk Avoidance

Risk avoidance is a risk management strategy where we change our business practices to completely eliminate the potential that a risk will materialize. 

Risk avoidance may initially seem like a highly desirable approach. There is, however, a major drawback.

Risk avoidance strategies typically have a serious detrimental impact on the business.

For example, consider the laptop theft risk. We could adopt a risk avoidance strategy and completely eliminate the risk by not allowing employees to purchase or use laptops. 

This approach is unwieldy and would likely be met with strong opposition from employees and managers due to the negative impact on employee productivity.

Similarly, we could avoid the risk of a DDoS attack against the organization's website by simply shutting down the website. 

If there is no website to attack, there's no risk that a DDoS attack can affect the site. 

But it's highly improbable that business leaders will accept shutting down the website as a viable approach. 

In fact, you might consider being driven to shut down your website to avoid DDoS attacks as the ultimate denial-of-service attack.

#

### Risk Transference

Risk transference shifts some of the impact of a risk from the organization experiencing the risk to another entity.

The most common example of risk transference is purchasing an insurance policy that covers a risk. When purchasing insurance, the customer pays a premium to the insurance carrier. In exchange, the insurance carrier agrees to cover losses from risks specified in the policy.

In the example of laptop theft, property insurance policies may cover the risk. If an employee's laptop is stolen, the insurance policy would provide funds to cover either the value of the stolen device or the cost to replace the device, depending on the type of coverage.

It's unlikely that a property insurance policy would cover a DDoS attack. In fact, many general business policies exclude all cybersecurity risks. 

An organization seeking insurance coverage against this type of attack should purchase cybersecurity insurance, either as a separate policy or as a rider on an existing business insurance policy.

This coverage would repay some or all of the cost of recovering operations and may also cover lost revenue during an attack.

#

### Risk Acceptance

Risk acceptance is the final risk management strategy and it boils down to deliberately choosing to take no other risk management strategy and to simply continue operations as normal in the face of the risk.

A risk acceptance approach may be warranted if the cost of mitigating a risk is greater than the impact of the risk itself.

Risk acceptance is a deliberate decision that comes as the result of a thoughtful analysis. It should not be undertaken as a default strategy. Simply stating that “we accept this risk” without analysis is not an example of an accepted risk; it is an example of an unmanaged risk.

In our laptop theft example, we might decide that none of the other risk management strategies are appropriate.

For example, we might feel that the use of cable locks is an unnecessary burden and that theft recovery tags are unlikely to work, leaving us without a viable risk mitigation strategy.

Business leaders might require that employees have laptop devices, taking risk avoidance off the table. And the cost of a laptop insurance policy might be too high to justify. 

In that case, we might decide that we will simply accept the risk and cover the cost of stolen devices when thefts occur. That's risk acceptance.

In the case of the DDoS risk, we might go through a similar analysis and decide that risk mitigation and transference strategies are too costly. In the event we continue to operate the site, we might do so accepting the risk that a DDoS attack could take the site down.

#

### Risk Analysis

As you work to manage risks, you will implement controls designed to mitigate those risks. 

There are a few key terms that you can use to describe different states of risk that you should know as you prepare for the Security+ exam:

- The **inherent risk** facing an organization is the original level of risk that exists before implementing any controls. Inherent risk takes its name from the fact that it is the level of risk inherent in the organization's business.
  
- The **residual risk** is the risk that remains after an organization implements controls designed to mitigate, avoid, and/or transfer the inherent risk.

-  An **organization's risk appetite** is the level of risk that it is willing to accept as a cost of doing business.

These three concepts are connected by the way that an organization manages risk. 

An organization begins with its inherent risk and then implements risk management strategies to reduce that level of risk. 

It continues doing so until the residual risk is at or below the organization's risk appetite.

The world of public accounting brings us the concept of control risk. Control risk is the risk that arises from the potential that a lack of internal controls within the organization will cause a material misstatement in the organization's financial reports.

Information technology risks can contribute to control risks if they jeopardize the integrity or availability of financial information. 

For this reason, financial audits often include tests of the controls protecting financial systems.

Organizations can implement these concepts only if they have a high degree of risk awareness.

They must understand the risks they face and the controls they can implement to manage those risks.

They must also conduct regular risk control assessments and selfassessments to determine whether those controls continue to operate effectively.

As risk managers work to track and manage risks, they must communicate their results to other risk professionals and business leaders. The risk register is the primary tool that risk management professionals use to track risks facing the organization.

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/7245c443-3c46-4742-909f-fdfafb27ba18)

The picture shows an excerpt from a risk register used to track IT risks in higher education.

The **risk register** is a lengthy document that often provides far too much detail for business leaders. When communicating risk management concepts to senior leaders, risk professionals often use a risk matrix, or heat map.

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/f2bd4bae-174a-4eff-a645-83d96bb3e5b2)

#

### Disaster Recovery Planning

No matter how many controls we put in place, the reality is that disasters will sometimes strike our organization and cause disruptions.

Disaster recovery planning (DRP) is the discipline of developing plans to recover operations as quickly as possible in the face of a disaster. The disaster recovery planning process creates a formal, broad disaster recovery plan for the organization and, when required, develops specific functional recovery plans for critical business functions. 

The goal of these plans is to help the organization recover normal operations as quickly as possible in the wake of a disruption.

#

### Disaster Types

Disasters of any type may strike an organization.



