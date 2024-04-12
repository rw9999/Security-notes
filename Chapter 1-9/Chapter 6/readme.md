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



