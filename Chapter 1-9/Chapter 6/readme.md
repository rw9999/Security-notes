# Secure Coding

The process of designing, creating, supporting, and maintaining that software is known as the software development life cycle (SDLC)

## The Software Development Life Cycle

Maps software creation from an idea to requirements gathering and analysis to design, coding, testing, and rollout.

Once software is in production, it also includes user training, maintenance, and decommissioning at the end of the software package’s useful life.

Simply picking an SDLC model to implement may not always be the best choice. Each SDLC model has certain types of work and projects that it fits better than others, making choosing an SDLC model that fits the work an important part of the process

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/6e6d8228-938c-4e19-94d4-515ed358ab4c)

##

### Software Development Phases

A few phases appear in most SDLC models:

1. **Feasibility phase** - where initial investigations into whether the effort should occur are conducted
	
Feasibility also looks at alternative solutions and high-level costs for each solution proposed. It results in a recommendation with a plan to move forward
	
2.** Analysis and requirements definition phase** - customer input is sought to determine what the desired functionality is, what the current system or application currently does and what it doesn’t do, and what improvements are desired. 
	
Requirements may be ranked to determine which are most critical to the success of the project

Security requirements definition is an important part of the analysis and requirements definition phase. It ensures that the application is designed to be secure and that secure coding practices are used
	
3. **Design phase** - design for functionality, architecture, integration points and techniques, dataflows, business processes, and any other elements that require design consideration
	
4. **Development phase** - The actual coding of the application
	
This phase may involve testing of parts of the software, including **unit testing**, the testing of small components individually to ensure they function properly
	
5. **Testing and integration phase** - formal testing with customers or others outside of the development team
   
Individual units or software components are integrated and then tested to ensure proper functionality
	
Connections to outside services, data sources, and other integration may occur during this phase. During this phase **user acceptance testing** (UAT) occurs to ensure that the users of the software are satisfied with its functionality
	
6. **Training and transition phase** - important task of ensuring that the end users are trained on the software and that the software has entered general
	
Sometimes called the acceptance, installation, and deployment phase
	
7. **Ongoing operations and maintenance** - This phase includes patching, updating, minor modifications, and other work that goes into daily support
	
Longest phase
	
8. **Disposition phase** - occurs when a product or system reaches the end of its life
	
Important phase for a number of reasons: shutting down old products can produce cost savings, replacing existing tools may require specific knowledge or additional effort, and data and systems may need to be preserved or properly disposed of

The order of the phases may vary, with some progressing in a simple linear fashion and others taking an iterative or parallel approach

##

### Code Deployment Environments

The names and specific purposes for these systems vary depending on organizational needs, but the most common environments are as follows:

**Development environment** - typically used for developers or other “builders” to do their work

  Some workflows provide each developer with their own development environment; others use a shared development environment
	
**Test environment** - where the software or systems can be tested without impacting the production environment

  In some schemes, this is preproduction, whereas in others a separate preproduction staging environment is used. 
	
  **Quality assurance (QA)** activities take place in the test environment
  	
**Staging environment** - a transition environment for code that has successfully cleared testing and is waiting to be deployed into production
	
**Production environment** - the live system
	
  Software, patches, and other changes that have been tested and approved move to production

This provides accountability and oversight and may be required for audit or compliance purposes as well

## Software Development Models

Formal SDLC models can be very detailed, with specific practices, procedures, and documentation, but many organizations choose the elements of one or more models that best fit their organizational style, workflow, and requirements


### Waterfall

The Waterfall methodology is a sequential model in which each phase is followed by the next phase. Phases do not overlap, and each logically leads to the next.

Waterfall has been replaced in many organizations because it is seen as relatively inflexible, but it remains in use for complex systems

Relatively inflexible, but it remains in use for complex systems. Since Waterfall is not highly responsive to changes and does not account for internal iterative work, it is typically recommended for development efforts that involve a fixed scope and a known timeframe for delivery and that are using a stable, well-understood technology platform

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/d497eb12-518b-4425-b2ce-a8c909b669da)

##

### Spiral

Uses the linear development concepts from the Waterfall model and adds an iterative process that revisits four phases multiple times during the development life cycle to gather more detailed requirements, design functionality guided by the requirements, and build based on the design

Puts significant emphasis on risk assessment as part of the SDLC, reviewing risks multiple times during the development process

The Spiral model shown in uses four phases, which it repeatedly visits throughout the development life cycle:

1. Identification, or requirements gathering, which initially gathers business requirements, system requirements, and more detailed requirements for subsystems or modules as the process continues
	
2. Design, conceptual, architectural, logical, and sometimes physical or final design
	
3. Build, which produces an initial proof of concept and then further development releases until the final production build is produced
	
4. Evaluation, which involves risk analysis for the development project intended to monitor the feasibility of delivering the software from a technical and managerial viewpoint.
	
As the development cycle continues, this phase also involves customer testing and feedback to ensure customer acceptance

Provides greater flexibility to handle changes in requirements as well as external influences such as availability of customer feedback and development staff

Allows the software development life cycle to start earlier in the process than Waterfall does.

It is possible for this model to result in rework or to identify design requirements later in the process that require a significant design change due to more detailed requirements coming to light

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/561472b4-bfd6-4916-aacb-dfa939ea47b5)

##

### Agile

An iterative and incremental process, rather than the linear processes that Waterfall and Spiral use. 

Agile is rooted in the Manifesto for Agile Software Development, a document that has four basic premises: 

• Individuals and interactions are more important than processes and tools

•  Working software is preferable to comprehensive documentation
	
•  Customer collaboration replaces contract negotiation
	
• Responding to change is key, rather than following a plan.

Agile methods tend to break up work into smaller units, allowing work to be done more quickly and with less up-front planning.

It focuses on adapting to needs, rather than predicting them, with major milestones identified early in the process but subject to change as the project continues to develop

Work is typically broken up into short working sessions, called sprints, that can last days to a few weeks

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/aa3cb2bd-94f9-441a-a1ca-8a4811de6ddd)

The Agile methodology is based on 12 principles:

- Ensure customer satisfaction via early and continuous delivery of the software.
- Welcome changing requirements, even late in the development process.
- Deliver working software frequently (in weeks rather than months).
- Ensure daily cooperation between developers and businesspeople.
- Projects should be built around motivated individuals who get the support, trust, and environment they need to succeed.
- Face-to-face conversations are the most efficient way to convey information inside the development team.
- Progress is measured by having working software.
- Development should be done at a sustainable pace that can be maintained on an ongoing basis.
- Pay continuous attention to technical excellence and good design.
- Simplicity—the art of maximizing the amount of work not done —is essential.
- The best architectures, requirements, and designs emerge from self-organizing teams.
- Teams should reflect on how to become more effective and then implement that behavior at regular intervals.

Less formally structured than Spiral or Waterfall but that has many opportunities for customer feedback and revision.

It can react more nimbly to problems and will typically allow faster customer feedback—an advantage when security issues are discovered

##

### DevSecOps and DevOps

**DevOps** - combines software development and IT operations with the goal of optimizing the SDLC

Uses collections of tools called **toolchains** to improve the coding, building and test, packaging, release, configuration and configuration management, and monitoring elements of a software development life cycle

**DevSecOps** - describes security as part of the DevOps model

Security is a shared responsibility that is part of the entire development and operations cycle

Integrating security into the design, development, testing, and operational work done to produce applications and services

The role of security practitioners in a DevSecOps model includes threat analysis and communications, planning, testing, providing feedback, and of course ongoing improvement and awareness responsibilities

Requires a strong understanding of the organization’s risk tolerance, as well as awareness of what the others involved in the DevSecOps environment are doing and when they are doing it

DevOps and DevSecOps are often combined with continuous integration and continuous deployment methodologies, where they can rely on automated security testing, and integrated security tooling, including scanning, updates, and configuration management tools, to help ensure security

##

### Continuous Integration and Continuous Deployment

**Continuous integration (CI)** - a development practice that checks code into a shared repository on a consistent ongoing basis

this can range from a few times a day to a very frequent process of check-ins and automated builds. 

The main goal of this approach is to enable the use of automation and scripting to implement automated courses of action that result in continuous delivery of code

It also requires automated testing. It is also often paired with **continuous deployment** (CD) (sometimes called continuous delivery), which rolls out tested changes into production automatically as soon as they have been tested.

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/870ecc30-6dcf-4404-b5cf-c24de2e2ba03)

Requires building **continuous validation** and automated security testing into the pipeline testing process

It can result in new vulnerabilities being deployed into production and could allow an untrusted or rogue developer to insert flaws into code that is deployed and then remove the code as part of a deployment in the next cycle. 

This means that logging, reporting, and **continuous monitoring** must all be designed to fit the CI/CD process

## Designing and Coding for Security

The first chance to help with software security is in the requirements gathering and design phases when security can be built in as part of the requirements and then designed based on those requirements

Later, during the development process, secure coding techniques, code review, and testing can improve the quality and security of the code that is developed

During the testing phase, fully integrated software can be tested using tools like web application security scanners or penetration testing techniques.

 This also provides the foundation for ongoing security operations by building the baseline for future security scans and regression testing during patching and updates. 

Throughout these steps, it helps to understand the common security issues that developers face, create, and discover

##

### Secure Coding Practices

One of the best resources for secure coding practices is the Open Web Application Security Project (OWASP).

Here are OWASP’s top proactive controls for 2018 with brief descriptions:

**Define Security Requirements** - Implement security throughout the development process. 

**Leverage Security Frameworks and Libraries** - Preexisting security capabilities can make securing applications easier. 

**Secure Database Access** - Prebuild SQL queries to prevent injection and configure databases for secure access. 

**Encode and Escape Data** - Remove special characters. Validate All Inputs Treat user input as untrusted and filter appropriately. 

**Implement Digital Identity** - Use multifactor authentication, secure password storage and recovery, and session handling. 

**Enforce Access Controls** - Require all requests to go through access control checks, deny by default, and apply the principle of least privilege. 

**Protect Data Everywhere** - Use encryption in transit and at rest. 

**Implement Security Logging and Monitoring** - This helps detect problems and allows investigation after the fact. 

**Handle all Errors and Exceptions** - Errors should not provide sensitive data, and applications should be tested to ensure that they handle problems gracefully.

##

### API Security 

**Application programming interfaces (APIs)** - interfaces between clients and servers or applications and operating systems that define how the client should ask for information from the server and how the server will respond

Programs written in any language can implement the API and make requests

API security relies on authentication, authorization, proper data scoping to ensure that too much data isn’t released, rate limiting, input filtering, and appropriate monitoring and logging to remain secure. 

Of course, securing the underlying systems, configuring the API endpoint server or service, and providing normal network layer security to protect the service are also important.

##

### Code Review Models

Helps to share knowledge of the code, and the experience gained in writing is better than simple documentation alone would be since it provides a personal understanding of the code and its functions

Helps detect problems while enforcing coding best practices and standards by exposing the code to review during its development cycle

Ensures that multiple members of a team are aware of what the code is supposed to do and how it accomplishes its task

##

### Pair Programming

An Agile software development technique that places two developers at one workstation.

One developer writes code, while the other developer reviews their code as they write it.

Intended to provide real-time code review, and it ensures that multiple developers are familiar with the code that is written.

The developers are expected to change roles frequently, allowing both of them to spend time thinking about the code while at the keyboard and to think about the design and any issues in the code while reviewing it.

Adds additional cost to development since it requires two full-time developers.

Provides additional opportunities for review and analysis of the code and directly applies more experience to coding problems, potentially increasing the quality of the code.

##

### Over-the-Shoulder

Relies on a pair of developers, but rather than requiring constant interaction and hand-offs

requires the developer who wrote the code to explain the code to the other developer

Allows peer review of code and can also assist developers in understanding how the code works, without the relatively high cost of pair programming

##

### Pass-Around Code Reviews

Known as email pass-around code review, is a form of manual peer review done by sending completed code to reviewers who check the code for issues

May involve more than one reviewer, allowing reviewers with different expertise and experience to contribute

Allow more flexibility in when they occur than an over-the-shoulder review

They don’t provide the same easy opportunity to learn about the code from the developer who wrote it that over-the-shoulder and pair programming offer, making documentation more important

##

### Tool-Assisted Reviews

Rely on formal or informal software-based tools to conduct code reviews

##

### Choosing a Review Method

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/5d42e8de-5789-4bdb-bf69-70820f06ce23)

When code requires more in-depth review than the relatively lightweight, Agile processes like pass-around and over-the-shoulder reviews, formal code review processes are sometimes used.

##

### Fagan Inspection

The primary form of formal code review

Fagan inspection is a form of structured, formal code review intended to find a variety of problems during the development process.

Specifies entry and exit criteria for processes, ensuring that a process is not started before appropriate diligence has been performed, and also making sure that there are known criteria for moving to the next phase.

The Fagan inspection process has six phases of a typical process:

1. Planning, including preparation of materials, attendees, and location
2. Overview, which prepares the team by reviewing the materials and assigning roles such as coder, reader, reviewer, and moderator
3. Preparation, which involves reviewing the code or other item being inspected and documents any issues or questions they may have
4. Meeting to identify defects based on the notes from the preparation phase
5. Rework to resolve issues
6. Follow-up by the moderator to ensure that all issues identified have been found and that no new defects were created during the resolution process

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/827ac2f4-01dd-4574-81fa-32bc751891ff)

Formal methods for verification of software like Fagan inspection and similar formal review processes can sound very expensive, but catching problems early can result in significant savings in time and cost.

Fagan code reviews remain relatively rare since many of the “lightweight” review options are easier to implement, offer many of the same benefits, and are far less costly.

## Software Security Testing

Veracode’s 2019 metrics for applications based on their testing showed that 83 percent of the applications they scanned exhibited at least one security issue during the testing process

##

### Analyzing and Testing Code

The source code that is the basis of every application and program can contain a variety of bugs and flaws, from programming and syntax errors to problems with business logic, error handling, and integration with other services and systems.

It is important to be able to analyze the code to understand what the code does, how it performs that task, and where flaws may occur in the program itself.

This is often done via static or dynamic code analysis along with testing methods like fuzzing. Once changes are made to code and it is deployed, it must be regression tested to ensure that the fixes put in place didn’t create new security issues.

##

### Static Code Analysis

(Sometimes called source code analysis) is conducted by reviewing the code for an application

Can be seen as a type of white-box testing with full visibility to the testers. This can allow testers to find problems that other tests might miss, either because the logic is not exposed to other testing methods or because of internal business logic problems

Static analysis does not run the program; instead, it focuses on understanding how the program is written and what the code is intended to do.

Static code analysis can be conducted using automated tools or manually by reviewing the code—a process sometimes called “code understanding.” Automated static code analysis can be very effective at finding known issues, and manual static code analysis helps to identify programmer-induced errors

##

### Dynamic Code Analysis

Relies on execution of the code while providing it with input to test the software

May be done via automated tools or manually, but there is a strong preference for automated testing due to the volume of tests that need to be conducted in most dynamic code testing processes

##

### Fuzzing

Involves sending invalid or random data to an application to test its ability to handle unexpected data

The application is monitored to determine if it crashes, fails, or responds in an incorrect manner. 

Fuzzing is typically automated due to the large amount of data that a fuzz test involves, and it is particularly useful for detecting input validation and logic issues as well as memory leaks and error handling.

Unfortunately, fuzzing tends to only identify simple problems—it does not account for complex logic or business process issues, and it may not provide complete code coverage if its progress is not monitored


## Injection Vulnerabilities

The primary mechanisms that attackers use to break through a web application and gain access to the systems supporting that application

These vulnerabilities allow an attacker to supply some type of code to the web application as input and trick the web server into either executing that code or supplying it to another server to execute

##

### SQL Injection Attacks 

Web applications often receive input from users and use it to compose a database query that provides results that are sent back to a user.

The attacker is able to provide input to the web application and then monitor the output of that application to see the result

### Blind Content-Based SQL Injection 

the perpetrator sends input to the web application that tests whether the application is interpreting injected code before attempting to carry out an attack.

### Blind Timing-Based SQL Injection 

Penetration testers may use the amount of time required to process a query as a channel for retrieving information from a database.

These attacks depend on delay mechanisms provided by different database platforms

##

### Code Injection Attacks

These attacks seek to insert attacker-written code into the legitimate code created by a web application developer.

Any environment that inserts user-supplied input into code written by an application developer may be vulnerable to a code injection attack.

Attackers might embed commands in text being sent as part of a **Lightweight Directory Access Protocol** (LDAP) query, conducting an LDAP injection attack.

They might also attempt to embed code in **Extensible Markup Language** (XML) documents, conducting an XML injection attack.

Commands may even attempt to load dynamically linked libraries (DLLs) containing malicious code in a **DLL injection attack**.

Cross-site scripting is an example of a code injection attack that inserts HTML code written by an attacker into the web pages created by a developer.

##

### Command Injection Attacks

Application code may reach back to the operating system to execute a command

## Exploiting Authentication Vulnerabilities

Applications, like servers and networks, rely on authentication mechanisms to confirm the identity of users and devices and verify that they are authorized to perform specific actions

## 

### Password Authentication

Passwords are the most common form of authentication in use today and most easily defeated

There are many ways that an attacker may learn a user’s password, ranging from technical to social

- Conducting social engineering attacks that trick the user into revealing a password, either directly or through a false authentication mechanism

- Eavesdropping on unencrypted network traffic 

- Obtaining a dump of passwords from previously compromised sites and assuming that a significant proportion of users reuse their passwords from that site on other sites

Attackers may be able to conduct credential brute-forcing attacks, in which they obtain a set of weakly hashed passwords from a target system and then conduct an exhaustive search to crack those passwords and obtain access to the system

Systems often ship with default administrative accounts that may remain unchanged

##

### Session Attacks

Credential-stealing attacks allow a hacker or penetration tester to authenticate directly to a service using a stolen account

**Session hijacking** attacks take a different approach by stealing an existing authenticated session

These attacks don’t require that the attacker gain access to the authentication mechanism; instead, they take over an already authenticated session with a website

Most websites that require authentication manage user sessions using cookies managed in the user’s browser and transmitted as part of the **HTTP header** information provided by a website

The user accesses the website’s login form and uses their credentials to authenticate

If the user passes the authentication process, the website provides the user’s browser with a cookie that may be used to authenticate future requests. 

Once the user has a valid cookie stored in the browser, the browser transmits that cookie with all future requests made to the website.

The website inspects the cookie and determines that the user has already authenticated and does not need to reenter their password or complete other authentication tasks

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/9b19361c-194d-4d20-9223-e8e2dd7429ca)

The cookie is simply a storage object maintained in the user’s browser that holds variables that may later be accessed by the website that created them

You can think of a cookie as a small database of information that the website maintains in the user’s browser. The cookie contains an authentication string that ties the cookie to a particular user session

##

### Cookie Stealing and Manipulation

Cookies serve as a key to bypass the authentication mechanisms of a website

If an attacker is able to steal someone’s cookie, they may then impersonate that user to the website that issued the cookie. 

There are several ways that an attacker might obtain a cookie:

- Eavesdropping on unencrypted network connections and stealing a copy of the cookie as it is transmitted between the user and the website. 

- Installing malware on the user’s browser that retrieves cookies and transmits them back to the attacker. 

- Engaging in a **man-in-the-middle attack**, where the attacker fools the user into thinking that the attacker is actually the target website and presenting a fake authentication form. They may then authenticate to the website on the user’s behalf and obtain the cookie

**Session replay attack**
![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/f6cea147-199c-447f-9191-d15199bbfa73)

Web developers can protect against cookie theft by marking cookies with the SECURE attribute. **Secure cookies** are never transmitted over unencrypted HTTP connections. Both servers and web browsers understand that they must only be sent over encrypted channels to protect against session replay attacks

The **NTLM pass-the-hash** attack is another form of replay attack that takes place against the operating system rather than a web application

The attacker begins by gaining access to a Windows system and then harvests stored NTLM password hashes from that system. They can then attempt to use these hashes to gain user or administrator access to that system or other systems in the same Active Directory domain

##

### Unvalidated Redirects

Some web applications allow the browser to pass destination URLs to the application and then redirect the user to that URL at the completion of their transaction.

**Unvalidated redirect**, which an attacker may use to redirect the user to a malicious site.

**Validated redirects** that check redirection URLs against an approved list. This list might specify the exact URLs authorized for redirection, or more simply, it might just limit redirection to URLs from the same domain.

## Exploiting Authorization Vulnerabilities

Allows an attacker to exceed the level of access that they are authorized

##

### Insecure Direct Object References

Web developers design an application to directly retrieve information from a database based on an argument provided by the user in either a query string or a POST request

There is nothing wrong with this approach, as long as the application also implements other authorization mechanisms. The application is still responsible for ensuring that the user is properly authenticated and is authorized to access the requested document

If the application does not perform authorization checks, the user may be permitted to view information that exceeds their authority. This situation is known as an **insecure direct object reference**.

##

### Directory Traversal

Some web servers suffer from a security misconfiguration that allows users to navigate the directory structure and access files that should remain secure

These directory traversal attacks work when web servers allow the inclusion of operators that navigate directory paths and filesystem access controls don’t properly restrict access to files stored elsewhere on the server

Directory traversal attacks use attempt to navigate outside of the areas of the filesystem that are reserved for the web server

If the attack is successful, the web server will dutifully display the shadow password file in the attacker’s browser, providing a starting point for a brute-force attack on the credentials

##

### File Inclusion

Instead of simply retrieving a file from the local operating system and displaying it to the attacker, file inclusion attacks actually execute the code contained within a file, allowing the attacker to fool the web server into executing arbitrary code

File inclusion attacks come in two variants: 

- Local file inclusion attacks seek to execute code stored in a file located elsewhere on the web server. They work in a manner very similar to a directory traversal attack

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/5da74cf1-1da4-421a-b7ab-1a7f7d002e42)

	
- Remote file inclusion attacks allow the attacker to go a step further and execute code that is stored on a remote server. These attacks are especially dangerous because the attacker can directly control the code being executed without having to first store a file on the local server

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/33c08b3f-7931-4e9d-8457-2e8d5a556b49)

 
When attackers discover a file inclusion vulnerability, they often exploit it to upload a web shell to the server. Web shells allow the attacker to execute commands on the server and view the results in the browser
	
This approach provides the attacker with access to the server over commonly used HTTP and HTTPS ports, making their traffic less vulnerable to detection by security tools.
	
The attacker may even repair the initial vulnerability they used to gain access to the server to prevent its discovery by another attacker seeking to take control of the server or by a security team who then might be tipped off to the successful attack

##

### Privilege Escalation

Seek to increase the level of access that an attacker has to a target system. They exploit vulnerabilities that allow the transformation of a normal user account into a more privileged account, such as the root superuser account.

## Exploiting Web Application Vulnerabilities

Web applications are complex ecosystems consisting of application code, web platforms, operating systems, databases, and interconnected **application programming interfaces (APIs)**

##

### Cross-Site Scripting (XSS)

Cross-site scripting (XSS) attacks occur when web applications allow an attacker to perform HTML injection, inserting their own HTML code into a web page

##

### Reflected XSS

XSS attacks commonly occur when an application allows **reflected input**.

Consider a simple web application that contains a single text box asking a user to enter their name.

A malicious individual could take advantage of this web application to trick an unsuspecting third party.

When the web application “reflects” this input in the form of a web page, your browser processes it as it would any other web page: it displays the text portions of the web page and executes the script portions.

You could be more malicious and include a more sophisticated script that asks the user to provide a password and then transmits it to a malicious third party.

The key to this attack is that it’s possible to embed form input in a link.

A malicious individual could create a web page with a link titled “Check your account at First Bank” and encode form input in the link. When the user visits the link, the web page appears to be an authentic First Bank website (because it is!) with the proper address in the toolbar and a valid digital certificate. However, the website would then execute the script included in the input by the malicious user, which appears to be part of the valid web page.

When creating web applications that allow any type of user input, developers must be sure to perform **input validation**.

Applications should never allow a user to include the <SCRIPT> tag in a reflected input field.

The best solution is to determine the type of input that the application will allow and then validate the input to ensure that it matches that pattern.

##

### Stored/Persistent XSS

To store cross-site scripting code on a remote web server

These attacks are described as persistent because they remain on the server even when the attacker isn’t actively waging an attack.

Consider a message board that allows users to post messages that contain HTML code. This is very common, because users may want to use HTML to add emphasis to their posts.

When future users load this message an XSS attack could also be used to redirect users to a phishing site, request sensitive information, or perform another attack.

## Request Forgery

Request forgery attacks exploit trust relationships and attempt to have users unwittingly execute commands against a remote server.

They come in two forms: cross-site request forgery and server-side request forgery.

##

### Cross-Site Request Forgery (CSRF/XSRF)

XSS attacks exploit the trust that a user has in a website to execute code on the user’s computer. XSRF attacks exploit the trust that remote sites have in a user’s system to execute commands on the user’s behalf.

XSRF attacks work by making the reasonable assumption that users are often logged into many different websites at the same time.

Attackers then embed code in one website that sends a command to a second website. When the user clicks the link on the first site, they are unknowingly sending a command to the second site. If the user happens to be logged into that second site, the command may succeed.

Developers should protect their web applications against XSRF attacks by creating web applications that use secure tokens that the attacker would not know to embed in the links.

Another safeguard is for sites to check the referring URL in requests received from end users and only accept requests that originated from their own site.

##

### Server-Side Request Forgery (SSRF)

Server-side request forgery (SSRF) attacks exploit a similar vulnerability but instead of tricking a user’s browser into visiting a URL, they trick a server into visiting a URL based on user-supplied input.

SSRF attacks are possible when a web application accepts URLs from a user as input and then retrieves information from that URL. If the server has access to nonpublic URLs, an SSRF attack can unintentionally disclose that information to an attacker.

## Application Security Controls

Through a combination of secure coding practices and security infrastructure tools, cybersecurity professionals can build robust defenses against application exploits.

##

### Input Validation

Applications that allow user input should perform validation of that input to reduce the likelihood that it contains an attack. 

Improper input handling practices can expose applications to injection attacks, cross-site scripting attacks, and other exploits.

The most effective form of input validation uses **input whitelisting**, in which the developer describes the exact type of input that is expected from the user and then verifies that the input matches that specification before passing the input to other processes or servers.

When performing input validation, it is very important to ensure that validation occurs server-side rather than within the client’s browser. 

Client-side validation is useful for providing users with feedback on their input, but it should never be relied on as a security control. It’s easy for hackers and penetration testers to bypass browser-based input validation.

It is often difficult to perform input whitelisting because of the nature of many fields that allow user input. It would be difficult to write logical rules that describe all valid submissions to that field that would also prevent the insertion of malicious code.

Developers might use input blacklisting to control user input. With this approach, developers do not try to explicitly describe acceptable input but instead describe potentially malicious input that must be blocked.

When performing input validation, developers must be mindful of the types of legitimate input that may appear in a field.

##

### Parameter Pollution

Parameter pollution is one technique that attackers have successfully used to defeat input validation controls.

Parameter pollution works by sending a web application more than one value for the same input variable.

This approach relies on the premise that the web platform won’t handle this URL properly. It might perform input validation on only the first argument but then execute the second argument, allowing the injection attack to slip through the filtering technology.
![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/6d8e9259-b98d-4481-943c-be478eb3aca8)


Parameter pollution attacks depend on defects in web platforms that don’t handle multiple copies of the same parameter properly. 

These vulnerabilities have been around for a while, and most modern platforms are defended against them, but successful parameter pollution attacks still occur today due to unpatched systems or insecure custom code.

##

### Web Application Firewalls

Though developers should always rely on input validation as their primary defense against injection attacks, the reality is that applications still sometimes contain injection flaws. This can occur when developer testing is insufficient or when vendors do not promptly supply patches to vulnerable applications.

WAFs function similarly to network firewalls, but they work at the Application layer.
![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/26433537-baac-44ea-ac04-2c1ab0388019)

A WAF sits in front of a web server and receives all network traffic headed to that server.

It then scrutinizes the input headed to the application, performing input validation (whitelisting and/or blacklisting) before passing the input to the web server.

This prevents malicious traffic from ever reaching the web server and acts as an important component of a layered defense against web application vulnerabilities.

##

### Database Security

Secure applications depend on secure databases to provide the content and transaction processing necessary to support business operations.

Relational databases form the core of most modern applications, and securing these databases goes beyond just protecting them against SQL injection attacks.

##

### Normalization

Database normalization is a set of design principles that database designers should follow when building and modifying databases.

Databases that follow these principles are said to be in normal forms, which are numbered in increasing order of the level of principle followed.

The simplest normal form is the first normal form (1NF) and more advanced normal forms follow sequentially (2NF, 3NF, etc.).

There’s an active and healthy debate in the database community about how closely database designers should follow the normal forms. Some of the advantages of implementing these principles as much as practical include that normalized designs do the following:

- Prevent data inconsistency
- Prevent update anomalies
- Reduce the need for restructuring existing databases, and
- Make the database schema more informative

##

### Parameterized Queries

Parameterized queries offer another technique to protect applications against injection attacks. In a parameterized query, the client does not directly send SQL code to the database server. 

Instead, the client sends arguments to the server, which then inserts those arguments into a precompiled query template. This approach protects against injection attacks and also improves database performance.

**Stored procedures** are an example of an implementation of parameterized queries used by some database platforms.

##

### Obfuscation and Camouflage

Maintaining sensitive personal information in databases exposes an organization to risk in the event that information is stolen by an attacker. Database administrators should take measures to protect against **data exposure**.

- **Data minimization** is the best defense. Organizations should not collect sensitive information that they don’t need and should dispose of any sensitive information that they do collect as soon as it is no longer needed for a legitimate business purpose.
  
- **Tokenization** replaces personal identifiers that might directly reveal an individual’s identity with a unique identifier using a lookup table.
  
- **Hashing** uses a cryptographic hash function to replace sensitive identifiers with an irreversible alternative identifier. **Salting** these values with a random number prior to hashing them makes these hashed values resistant to a type of attack known as a rainbow table attack.

## Code Security

Software developers should also take steps to safeguard the creation, storage, and delivery of their code.

### Code Signing

Code signing provides developers with a way to confirm the authenticity of their code to end users. 

Developers use a cryptographic function to digitally sign their code with their own private key and then browsers can use the developer’s public key to verify that signature and ensure that the code is legitimate and was not modified by unauthorized individuals. 

In cases where there is a lack of code signing, users may inadvertently run inauthentic code.

##

### Code Reuse

Many organizations reuse code not only internally but by making use of third-party software libraries and software development kits (SDKs). Third-party software libraries are a common way to share code among developers

Libraries consist of shared code objects that perform related functions.

Instead of having to write the code to perform every detailed function they need, developers can simply locate libraries that contain relevant functions and then call those functions

Organizations trying to make libraries more accessible to developers often publish software development kits (SDKs). SDKs are collections of software libraries combined with documentation, examples, and other resources designed to help programmers get up and running quickly in a development environment. SDKs also often include specialized utilities designed to help developers design and test code

Organizations may also introduce third-party code into their environments when they outsource code development to other organizations. Security teams should ensure that outsourced code is subjected to the same level of testing as internally developed code

Security professionals should be familiar with the various ways that third-party code is used in their organizations as well as the ways that their organization makes services available to others

It’s fairly common for security flaws to arise in shared code, making it extremely important to know these dependencies and remain vigilant about security updates

##

### Software Diversity

Security professionals seek to avoid single points of failure in their environments to avoid availability risks if an issue arises with a single component.

Security professionals should watch for places in the organization that are dependent on a single piece of source code, binary executable files, or compilers. 

Though it may not be possible to eliminate all of these dependencies, tracking them is a critical part of maintaining a secure codebase.

##

### Code Repositories

Centralized locations for the storage and management of application source code

The main purpose of a code repository is to store the source files used in software development in a centralized location that allows for secure storage and the coordination of changes among multiple developers

**Version control** allows the tracking of changes and the rollback of code to earlier versions when required

possible for many people to share work on a large software project in an organized fashion

They also meet the needs of security and auditing professionals who want to ensure that software development includes automated auditing and logging of changes

By exposing code to all developers in an organization, code repositories promote code reuse. Developers seeking code to perform a particular function can search the repository for existing code and reuse it rather than start from ground zero

Code repositories also help avoid the problem of **dead code**, where code is in use in an organization but nobody is responsible for the maintenance of that code and, in fact, nobody may even know where the original source files reside

##

### Integrity Measurement

Cybersecurity teams should also work hand in hand with developers and operations teams to ensure that applications are provisioned and de-provisioned in a secure manner through the organization’s approved release management process

This process should include code integrity measurement. Code integrity measurement uses cryptographic hash functions to verify that the code being released into production matches the code that was previously approved. 

Any deviation in hash values indicates that code was modified, either intentionally or unintentionally, and requires further investigation prior to release.

##

### Application Resilience

When we design applications, we should create them in a manner that makes them resilient in the face of changing demand. We do this through the application of two related principles:

- **Scalability** says that applications should be designed so that computing resources they require may be incrementally added to support increasing demand.

- **Elasticity** goes a step further than scalability and says that  applications should be able to automatically provision resources to scale when necessary and then automatically deprovision those resources to reduce capacity (and cost) when it is no longer needed.

## Secure Coding Practices

A multitude of development styles, languages, frameworks, and other variables may be involved in the creation of an application, but many of the security issues are the same regardless of which you use

### Source Code Comments

Comments are an important part of any good developer’s workflow. Placed strategically throughout code, they provide documentation of design choices, explain workflows, and offer details crucial to other developers who may later be called on to modify or troubleshoot the code.

Comments can also provide attackers with a roadmap explaining how code works. Comments may even include critical security details that should remain secret. Developers should take steps to ensure that commented versions of their code remain secret

Web applications that expose their code may allow remote users to view comments left in the code. In those environments, developers should remove comments from production versions of the code before deployment.

##

### Error Handling

Developers must understand this and write their code so that it is resilient to unexpected situations that an attacker might create in order to test the boundaries of code.

Developers must anticipate unexpected situations and write error-handling code that steps in and handles situations in a secure fashion. Improper error handling may expose code to unacceptable levels of risk.

Overly verbose error handling routines may also present risk. If error handling routines explain too much about the inner workings of code, they may allow an attacker to find a way to exploit the code.

##

### Hard-Coded Credentials

Developers may include usernames and passwords in source code. There are two variations on this error.

First, the developer may create a hard-coded maintenance account for the application that allows the developer to regain access even if the authentication system fails.

This is known as a backdoor vulnerability and is problematic because it allows anyone who knows the backdoor password to bypass normal authentication and gain access to the system.

If the backdoor becomes publicly (or privately!) known, all copies of the code in production are compromised.

The second variation of hard-coding credentials occurs when developers include access credentials for other services within their source code.

If that code is intentionally or accidentally disclosed, those credentials then become known to outsiders.

This occurs quite often when developers accidentally publish code to a public code repository, such as GitHub, that contains API keys or other hardcoded credentials.

##

### Memory Management

Applications are often responsible for managing their own use of memory, and in those cases, poor memory management practices can undermine the security of the entire system.

##

### Resource Exhaustion

Systems may consume all of the memory, storage, processing time, or other resources available to them, rendering the system disabled or crippled for other uses.

**Memory leaks** are one example of resource exhaustion.

If an application requests memory from the operating system, it will eventually no longer need that memory and should then return the memory to the operating system for other uses.

In the case of an application with a memory leak, the application fails to return some memory that it no longer needs, perhaps by simply losing track of an object that it has written to a reserved area of memory.

If the application continues to do this over a long period of time, it can slowly consume all the memory available to the system, causing it to crash. 

Rebooting the system often resets the problem, returning the memory to other uses but if the memory leak isn’t corrected, the cycle simply begins anew.

##

### Pointer De-referencing

**Memory pointers** can also cause security issues. Pointers are a commonly used concept in application development. They are simply an area of memory that stores an address of another location in memory.

One particular issue that might arise is if the pointer is empty, containing what programmers call a null value.

If the application tries to de-reference this null pointer, it causes a condition known as a null pointer exception.

In the best case, a null pointer exception causes the program to crash, providing an attacker with access to debugging information that may be used for reconnaissance of the application's security.

In the worst case, a null pointer exception may allow an attacker to bypass security controls. Security professionals should work with application developers to help them avoid these issues.

##

### Buffer Overflows

Buffer overflow attacks occur when an attacker manipulates a program into placing more data into an area of memory than is allocated for that program’s use.

The goal is to overwrite other information in memory with instructions that may be executed by a different process running on the system.

Buffer overflow attacks are quite commonplace and tend to persist for many years after they are initially discovered.

Integer overflow - This is simply a variant of a buffer overflow where the result of an arithmetic operation attempts to store an integer that is too large to fit in the specified buffer.

##

### Race Conditions

Race conditions occur when the security of a code segment depends upon the sequence of events occurring within the system.

The **time-of-check-to-time-of-use (TOCTTOU or TOC/TOU)** issue is a race condition that occurs when a program checks access permissions too far in advance of a resource request.

To prevent this race condition, the developer should evaluate access permissions at the time of each request rather than caching a listing of permissions.

##

### Unprotected APIs

Organizations often want other developers to build upon the platforms that they have created.

To enable this type of innovation, services often create application programming interfaces (APIs) that enable automated access.

If not properly secured, unprotected APIs may lead to the unauthorized use of functions.

An API that does not use appropriate authentication may allow anyone with knowledge of the API URLs to modify a service. 

APIs that are not intended for public use should always be secured with an authentication mechanism, such as an API key, and accessed only over encrypted channels that protect those credentials from eavesdropping attacks.

##

### Driver Manipulation

**Device drivers** play an important role in computing. They serve as the software interface between hardware devices and the operating system.

Device drivers require low-level access to the operating system and run with administrative privileges. If an attacker can convince a user to install a malicious driver on their computer, that malware can gain complete control of the system.

One way that attackers might do this is by **refactoring** an existing driver. If they have access to the driver’s source code, they can modify it to also include malware elements. This is very difficult to pull off in practice, however, because it’s not easy to get access to the source code for drivers.

Attackers without access to the driver source code can use a technique called **shimming**. This takes a legitimate driver and wraps a malicious driver around the outside of it. The malicious driver, known as the shim, receives requests from the operating system and simply passes them on to the legitimate driver so that the device functions normally. However, the driver can also carry out its malware payload in the background.

Fortunately, modern operating systems all contain protections against malicious drivers. The most important of these protections is code signing.

Device manufacturers write drivers and then apply digital signatures to them so that the operating system can verify their authenticity. If the driver is not digitally signed, the operating system may warn the user of the suspicious driver or prevent its installation outright.

