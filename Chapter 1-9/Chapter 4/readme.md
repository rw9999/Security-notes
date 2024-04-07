# Chapter 4 Social Engineering, Physical, and Password Attacks

### Social Engineering

The practice of manipulating people through a variety of strategies to accomplish desired actions. Social engineers work to influence their targets to take actions that they might not otherwise have taken.

Key principles:

- **Authority** relies on the fact that most people will obey someone who appears to be in charge or knowledgeable, regardless of whether or not they actually are.

&emsp;&emsp; i.e. A social engineer using the principle of authority may claim to be a manager, a government official, or some other person who would have authority in the situation they are operating in.
  
- **Intimidation** relies on scaring or bullying an individual into taking a desired action. The individual who is targeted will feel threatened and respond by doing what the social engineer wants them to do.
  
- **Consensus-based** social engineering uses the fact that people tend to want to do what others are doing to persuade them to take an action.

&emsp;&emsp;i.e. A consensus-based social engineering attack might point out that everyone else in a department had already clicked on a link, or might provide fake testimonials about a product making it look safe. Consensus is called “social proof” in some categorization schemes
  
- **Scarcity** is used in scenarios that make something look more desirable because it may be the last one available.
  
- **Familiarity-based** attacks rely on you liking the individual or even the organization the individual is claiming to represent.

- **Trust** much like familiarity, relies on a connection with the individual they are targeting. Unlike familiarity, which relies on targets thinking that something is normal and thus familiar

&emsp;&emsp;i.e. social engineers who use this technique work to build a connection with their targets so that they will take the actions that they want them to take
  
- **Urgency** relies on creating a feeling that the action must be taken quickly due to some reason or reasons.
  
These social engineering principles work because they cause the target to react to a situation, and that may make the target nervous or worried about a result or scenario. Social engineering relies on human reactions, and we are most vulnerable when we are responding instead of thinking clearly

Social engineering efforts in the real world combine multiple principles into a single attack. A key part of social engineering is understanding the target, how humans react, and how stress reactions can be leveraged to meet a goal.



## Social Engineering Techniques

### Phishing

A broad term used to describe the fraudulent acquisition of information often focused on credentials like usernames and passwords, as well as sensitive personal information like credit card numbers and related data.

Phishing is most often done via email, but a wide range of phishing techniques exist

**Smishing** - phishing via SMS (text)

**Vishing** - phishing via telephone

**Spear phishing** targets specific individuals or groups in an organization in an attempt to gather desired information or access

**Whaling**, much like spear phishing, targets specific people, but whaling is aimed at senior employees like CEOs and CFOs—“big fish” in the company

One of the most common defenses against phishing of all types is awareness. Teaching staff members about phishing and how to recognize and respond to phishing attacks, and even staging periodic exercises, are all common means of decreasing the risk of successful phishing attacks.

Technical means also exist, including filtering that helps prevent phishing using reputation tools, keyword and text pattern matching, and other technical methods of detecting likely phishing emails, calls, or texts.

##

### Credential Harvesting

The process of gathering credentials like usernames and passwords

Credential harvesting is often performed via phishing attacks but may also be accomplished through system compromise resulting in the acquisition of user databases and passwords, use of login or remote access tools that are set up to steal credentials, or any other technique that will gather credentials for attackers

Once credentials are harvested, attackers will typically leverage them for further attacks, with financial attacks a top target

Although credential harvesting can be difficult to completely stop, multifactor authentication (MFA) remains a strong control that can help limit the impact of successful credential harvesting attacks.

User awareness, technical tools that can stop harvesting attacks like phishing emails or related techniques, and strong monitoring and response processes can all help with credential harvesting and abuse of harvested credentials.

##

### Website Attacks

**Pharming attacks** redirect traffic away from legitimate websites to malicious versions. Pharming typically requires a successful technical attack that can change DNS entries on a local PC or on a trusted local DNS server, allowing the traffic to be redirected

**Typosquatting** is when typo squatters use misspelled and slightly off but similar to the legitimate site URLs to conduct attacks

Typo squatters rely on the fact that people will mistype URLs and end up on their sites, thus driving ad traffic or even sometimes using the typo-based website to drive sales of similar but not legitimate products

Watering hole attacks don't redirect users; instead, they use websites that target frequent users to attack them.

These frequently visited sites act like a watering hole for animals and allow the attackers to stage an attack, knowing that the victims will visit the site.

Once they know what site their targets will use, attackers can focus on compromising it, either by targeting the site or deploying malware through other means such as an advertising network.

##

### Spam

Sometimes called unsolicited or junk email, may not immediately seem like a social engineering technique, but spam often employs social engineering techniques to attempt to get recipients to open the message or to click on links inside of it.

Spam relies on one underlying truth that many social engineers will take advantage of: if you send enough tempting messages, you're likely to have someone fall for it

(SPIM) Spam over Instant Messaging 

##

### In-Person Techniques

**Dumpster Diving** - retrieving potentially sensitive information from a dumpster

Organizations that want to avoid this will secure their dumpsters, use secure disposal services for documents, and will otherwise seek to ensure that their trash really is trash without anything useful in it

**Shoulder Surfing** - the process of looking over a person's shoulder to capture information like passwords or other data

Preventing shoulder surfing requires awareness on the part of potential targets, although tools like polarized security lenses over mobile devices like laptops can help prevent shoulder surfing in public spaces.

**Tailgating** - a physical entry attack that requires simply following someone who has authorized access to an area so that as they open secured doors you can pass through as well

**Eliciting Information** - a technique used to gather information without targets realizing they are providing it 

Techniques like flattery, false ignorance, or even acting as a counselor or sounding board are all common elements of an elicitation effort. Talking a target through things, making incorrect statements so that they correct the person eliciting details with the information they need, and other techniques are all part of the elicitation process

**Prepending** can mean one of three things:

1. Adding an expression or phrase, such as adding “SAFE” to a set of email headers to attempt to fool a user into thinking it has passed an antispam tool
   
2. Adding information as part of another attack to manipulate the outcome
   
3. Suggesting topics via a social engineering conversation to lead a target toward related information the social engineer is looking for

## 

### Identity Fraud and Impersonation

**Pretexting** - the process of using a made-up scenario to justify why you are approaching an individual

Pretexting is often used as part of impersonation efforts to make the impersonator more believable.

An aware target can ask questions or require verification that can help defeat pretexting and impersonation attacks.

**Identity Fraud** - the use of someone else's identity

**Impersonation** where you act as if you are someone else, can be a limited form of identity fraud. Impersonation is less specific, and the social engineer or attacker who uses it may simply pretend to be a delivery driver or an employee of a service provider rather than claiming a specific identity

**Hoaxes** - intentional falsehoods

Come in a variety of forms ranging from virus hoaxes to fake news. Social media plays a large role in many modern hoaxes, and attackers and social engineers may leverage current hoaxes to assist in their social engineering attempts.

**Invoice scams** - involve sending fake invoices to organizations in the hopes of receiving payment. Invoice scams can be either physical or electronic, and they rely on the recipient not checking to see if the invoice is legitimate.

##

### Reconnaissance and Impersonation

