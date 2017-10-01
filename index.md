### Before Starting
* Understand the [Agile Principles](http://agilemanifesto.org/)
* Understand the [Lean Principles](https://www.lean.org/WhatsLean/Principles.cfm)
* Understand what [DevOps](https://aws.amazon.com/devops/what-is-devops/) is, and its [principles and practices](https://dzone.com/articles/devops-devops-principles)
* Understand what [MVP](http://blog.crisp.se/2016/01/25/henrikkniberg/making-sense-of-mvp) is
* Understand what [Product Ownership](https://www.youtube.com/watch?v=502ILHjX9EE) is (**14:10** if your organisation doesn’t like truth and honesty, you won’t like Agile)
* Follow the [12-factor](https://12factor.net/) app techniques.
* Understand the [Testing Pyramid](https://martinfowler.com/bliki/TestPyramid.html)
* Bake-in quality and security into your product

> You build it, you run it; you break it, you fix it

### UX
* Make sure the UX is an integral part of your team
* Experiment. Experiment. Experiment
* Prototype. Prototype. Prototype. 
* Get involved in ideation, user surveys, research and design facilitation
* Involve and experiment with real users
* Your customers and users are also your stakeholders
* Improve and grow your [Design Literacy](https://blogs.adobe.com/creativecloud/3-keys-to-improving-design-literacy-for-non-designers/)
* Collect data for insight on how successful the product actually is

> Usability makes or breaks your product

### Architecture
* Follow the [Evolutionary Architecture](https://www.thoughtworks.com/radar/techniques/evolutionary-architecture) concept
* Follow the [Ten Commandments](https://centerbrook.com/blog/2010/03/the-ten-commandments-of-architecture/) of Architecture
* [Ivory-tower](http://www.agilemodeling.com/essays/enterpriseModelingAntiPatterns.htm#IvoryTowerArchitecture) architecture **doesn’t work**
* Do architecture often and in collaboration
* Remove hard-coupling and dependencies 
  * [OAS](https://swagger.io/) based APIs and microservices, consider using Swagger
  * Contracts based development for both internal and external components - use mocks and stubs as part of unit testing
* [Microservice](https://martinfowler.com/articles/microservices.html) architecture is [not the silver bullet](https://martinfowler.com/articles/microservice-trade-offs.html)
* Consider other options e.g. [serverless](https://martinfowler.com/articles/serverless.html), PaaS
* [Design for failure](https://blog.risingstack.com/designing-microservices-architecture-for-failure/)
* Think self-monitoring, self-regulating and self-healing mechanisms
* Use the the [Technology Radar](https://www.thoughtworks.com/radar) from Thoughtworks to guide your team’s architecture decisions

> Can’t do architecture without programming, and can’t do programming without architecture

> *Martin Fowler*

### Development environment 
* Choose a well-known (and free) IDE (unless it’s .Net or C# - use Visual Studio)
* Documented, easy and quick to set up
* Repeatable, rebuildable everytime - no snowflake setup
* No special tweaks here or there ,use tools out-of-the-box and standardise
* Use automated build tool e.g. Maven or Cake and Fake

### Repositories
* Git is preferred - github, gitlab or BitBucket
* [Learn](https://try.github.io/levels/1/challenges/1) git, follow [best practices](https://sethrobertson.github.io/GitBestPractices/)
* Understand how to use git, and understand how distributed repo works
* Implement Versioning [policy](http://semver.org/)
* Use Trunk Based Development and Short-Lived Branches [strategies](https://barro.github.io/2016/02/a-succesful-git-branching-model-considered-harmful/)

### Coding convention 
* Conventions for [different languages](https://en.wikipedia.org/wiki/Coding_conventions), Google’s [Java](https://google.github.io/styleguide/javaguide.html) style
* Conventions should be standardised across the organisation
* Follow the convention and include it in code quality check 
* Consistency in the codebase is a must; code individualisation is *unacceptable*
* Make sure everyone in the team understands and follows the agreed coding convention

### Security - DevSecOps
* Security engineer needs to be part of the team
* Check for vulnerabilities on own code and all dependencies 
* 2nd Factor - on dependencies
* 3rd Factor - on configuration parameters
* Implement [OWASP](https://www.owasp.org/index.php/OWASP_Proactive_Controls) Proactive Controls (the list is ordered in importance)
* Self-service security, and make it part of the build: [snyk](https://snyk.io/), [Brakeman](https://brakemanscanner.org/), [dependency checks](https://www.owasp.org/index.php/OWASP_Dependency_Check) 
* [Security scan[(https://blog.docker.com/2016/05/docker-security-scanning/) your containers and do dependency checking
* Carry out targeted [DAST](https://www.owasp.org/index.php/Category:Vulnerability_Scanning_Tools) at Acceptance or UAT 
* Automated functional and integration testing of security features 
* Automated security attacks, using [Gauntlt](http://gauntlt.org/) or other tools
* Automated infrastructure security testing e.g. [InSpec](https://www.inspec.io/)
* Carry out targeted manual Penetration Testing

