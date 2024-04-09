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

### Spiral

Uses the linear development concepts from the Waterfall model and adds an iterative process that revisits four phases multiple times during the development life cycle to gather more detailed requirements, design functionality guided by the requirements, and build based on the design

puts significant emphasis on risk assessment as part of the SDLC, reviewing risks multiple times during the development process

The Spiral model shown in Figure 6.3 uses four phases, which it repeatedly visits throughout the development life cycle:

1. Identification, or requirements gathering, which initially gathers business requirements, system requirements, and more detailed requirements for subsystems or modules as the process continues
	
2. Design, conceptual, architectural, logical, and sometimes physical or final design
	
3. Build, which produces an initial proof of concept and then further development releases until the final production build is produced
	
4. Evaluation, which involves risk analysis for the development project intended to monitor the feasibility of delivering the software from a technical and managerial viewpoint.
	
As the development cycle continues, this phase also involves customer testing and feedback to ensure customer acceptance

Provides greater flexibility to handle changes in requirements as well as external influences such as availability of customer feedback and development staff

Allows the software development life cycle to start earlier in the process than Waterfall does.

It is possible for this model to result in rework or to identify design requirements later in the process that require a significant design change due to more detailed requirements coming to light

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/561472b4-bfd6-4916-aacb-dfa939ea47b5)

### Agile

an iterative and incremental process, rather than the linear processes that Waterfall and Spiral use. 

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

