The motivation behind is to provide a very broad overview of what are usually present or feed into successful product delivery work.  

The very basics of software development, object-oriented programming, design patterns or hygienne factors of a technical team or prodcut team are not covered, as the expectation is that the team are already aware of these and other standard industry practices.

### Before Starting
* Understand [Agile Principles](http://agilemanifesto.org/)
* Understand [Lean Principles](https://www.lean.org/WhatsLean/Principles.cfm)
* Understand [DevOps](https://aws.amazon.com/devops/what-is-devops/), and its [principles and practices](https://dzone.com/articles/devops-devops-principles)
* Understand [MVP](http://blog.crisp.se/2016/01/25/henrikkniberg/making-sense-of-mvp)
* Understand [Product Ownership](https://www.youtube.com/watch?v=502ILHjX9EE) 
> if your organisation doesn’t like **truth and honesty**, they won’t like Agile
* Follow the [12-factor](https://12factor.net/) app techniques.
* Understand [Testing Pyramid](https://martinfowler.com/bliki/TestPyramid.html)
> Build quality and security in

> You build it, you run it; you break it, you fix it

### UX
* Make sure the UX is an integral part of your team
* Experiment. Experiment. Experiment
* Prototype. Prototype. Prototype. 
* Early customer feedback loops
* Get involved in ideation, user surveys, research and design facilitation
* Involve and experiment with real users
* Your customers and users are also your stakeholders
* Improve and grow your [Design Literacy](https://blogs.adobe.com/creativecloud/3-keys-to-improving-design-literacy-for-non-designers/)
* Collect data for insight on how successful the product actually is

> Usability makes or breaks your product

### Architecture
* Follow the [Evolutionary Architecture](https://www.thoughtworks.com/radar/techniques/evolutionary-architecture) concept
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

> "Can’t do architecture without programming, and can’t do programming without architecture" - Martin Fowler

### Development environment 
* Choose a well-known (and free) IDE
* Documented, easy and quick to set up
* Repeatable, rebuildable everytime - no snowflake setup
* No special tweaks if bit required,use tools out-of-the-box and standardise
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
* Follow the convention and include it in [code quality check](#static-code-analysis) 
* Consistency in the codebase is a must; code individualisation is *unacceptable*
* Make sure everyone in the team understands and follows the agreed coding convention

### Security - DevSecOps
* Security engineer needs to be part of the team
* Check for vulnerabilities on own code and all dependencies 
* From 12-Factor App:
	* follow the 2nd Factor - dependencies
	* follow the 3rd Factor - configuration parameters
* Implement [OWASP](https://www.owasp.org/index.php/OWASP_Proactive_Controls) Proactive Controls (the list is ordered in importance)
* Self-service security, and make it part of the build: [snyk](https://snyk.io/), [Brakeman](https://brakemanscanner.org/), [dependency checks](https://www.owasp.org/index.php/OWASP_Dependency_Check) - plugin for [SonarQube](https://github.com/stevespringett/dependency-check-sonar-plugin)
* [Security scan](https://blog.docker.com/2016/05/docker-security-scanning/) containers - from [Thoughtworks' Tech Radar](https://www.thoughtworks.com/radar/techniques/container-security-scanning)
* Carry out targeted [DAST](https://www.owasp.org/index.php/Category:Vulnerability_Scanning_Tools) at Acceptance or UAT 
* Automated functional and integration testing of security features 
* Automated security attacks, using [Gauntlt](http://gauntlt.org/) or other tools
* Automated infrastructure security testing e.g. [InSpec](https://www.inspec.io/)
* Carry out targeted manual Penetration Testing

### Quality 
* [TDD](https://martinfowler.com/bliki/TestDrivenDevelopment.html) - you need to understand this
* Automate. Automate. Automate
* Follow the principles of [Testing Pyramid](https://martinfowler.com/bliki/TestPyramid.html)
* Beware of the [Testing Cupcake](https://www.thoughtworks.com/insights/blog/introducing-software-testing-cupcake-anti-pattern)
* Determine the layers of the pyramid for your application - [start simple](https://testing.googleblog.com/2015/04/just-say-no-to-more-end-to-end-tests.html) 
* Manual/exploratory testing (the cloud on top of the pyramid) will need to be kept to the minimum, and as necessary.
![Testing Pyramid](https://dgunawan.github.io/product-delivery-ingredients/images/Testing Pyramid.jpg)		
* For automated tests
	* [JavaScript](https://medium.com/powtoon-engineering/a-complete-guide-to-testing-javascript-in-2017-a217b4cd5a2a) - see below for list of frameworks
	* “Record and playback testing” is **unacceptable** as these will create non-deterministic tests.
	* Understand [Stubbing and Mocking](https://martinfowler.com/articles/mocksArentStubs.html) 
	* [BDD](https://cucumber.io/blog/2016/07/20/where_should_you_use_bdd) should be used "in all the places where the business has reason to have opinions about the behaviour."
* Understand what [Test Coverage](https://martinfowler.com/bliki/TestCoverage.html) is, and determine the right coverage as part of your static code analysis
* Never have [non-deterministic](https://martinfowler.com/articles/nonDeterminism.html) test
* Test based on Risk Assessment 
* Do load and performance testing
* [Gatling](http://gatling.io/), JMeter, SoapUI
* Do security and penetration tests
* Automate. Automate. Automate

### Static code analysis
* Use SonarQube or similar tools
* Include [code convention](#coding-convention) as part of the check
* Agree on the metrics your team should start with
* Monitored and adjusted as your team matures
* Include it in the CI pipeline and fail the build when your quality metrics  drop

### Development practices
* Always do peer review through Pull Requests mechanism
* Pair-programming could reduce the need for extensive peer-review
* Do documentation in Readme file in the repo
* [Self-documenting](https://www.martinfowler.com/bliki/CodeAsDocumentation.html) code is necessary
* Follow the Boy Scout rules - Clean Code book p14
* No Broken Windows - Clean Code book p8
* Understand what [Refactoring](https://www.agilealliance.org/glossary/refactoring/#q=~(filters~(postType~(~'page~'post~'aa_book~'aa_event_session~'aa_experience_report~'aa_glossary~'aa_research_paper~'aa_video)~tags~(~'refactoring))~searchTerm~'~sort~false~sortDirection~'asc~page~1)) is and Just Do It
* Understand what [Technical Debt](https://martinfowler.com/bliki/TechnicalDebt.html) is, and incur when appropriate
* Alignment to architectural and technology governance

> “[Keep the Codebase Healthy](https://www.thoughtworks.com/talks/agile-architecture-rethink-2014)” - Martin Fowler

### Continuous Integration
* Automated build and notifications
* When a build should be activated, at every commit?
* Build should stop at ANY test failure - no excuse
* Build should stop at a predetermined decrease of code quality - use SonarQube or similar tool to check
* Roll your own, Jenkins, Hudson, Octopus etc.
* SaaS: Codeship, Travis CI, Bamboo, Hudson, GoCD 

### Continuous Delivery/Deployment
* [Infrastructure as Code](https://www.thoughtworks.com/insights/blog/infrastructure-code-reason-smile), include unit tests!
* Automatically build the release package
* Automatically deploy to intended environments
* Treat servers as cattle, not pets
* Release package will be promoted to the next stage only on successful build
* Consistent server build and environment, no snowflake or pets server or environment
* 10th Factor - all environments should be very similar, dev, test, UAT, QA, prod. 
* Utilise containers i.e. Docker
* Utilise an orchestration manager e.g. Kubernetes, Docker Swarm, Apache Mesos
* Utilise a configuration manager, Infrastructure as Code, e.g. Ansible, Chef, Puppet, even on PaaS
* Consider the right deployment technique:
	* A/B testing
	* Red/Blue deployment
	* Canary
	* Feature toggles
	* Dark launches
* [Decouple](https://www.thoughtworks.com/radar/techniques/decoupling-deployment-from-release) deployment from release

### Data(base)
* Should have a strategy to optimise data usage and storage
* [Evolutionary](https://martinfowler.com/articles/evodb.html) database design
* Data obsfucation or masking **must** be part of the workflow to protect private and sensitive data
* Build in metrics to provide data to the business and for health monitoring
* Consider support scenario
* Be Data Informed - Use data to help your team make decisions
* Use data to make your life easier

### Support - Monitoring
* Consider the principle of Least Privilege for access control
* Consider support requirements
* Put monitoring everywhere, prioritise alerting on component’s importance, resiliency, set-up, backup etc.
* New Relic, OMS, Splunk, ELK, Raygun
* Build a dashboard which will be useful for all support levels, consider Splunk, Grafana

### Support - Alerting
* Consider the application’s SLA
* Consider the support agreements
* Consider Segregation of Duties
* Determine the metrics that will trigger alerts
* Alert types e.g. Info, Warning etc.
* Select the appropriate tools to make your life easy: IM, SMS, email, flashing lights, sirens etc.


### Resources
* [https://guide.freecodecamp.org/](https://guide.freecodecamp.org/)
* [https://github.com/mr-mig/every-programmer-should-know](https://github.com/mr-mig/every-programmer-should-know)
* [https://stevewedig.com/2014/02/03/software-developers-reading-list/](https://stevewedig.com/2014/02/03/software-developers-reading-list/) 
* [https://martinfowler.com](https://martinfowler.com)
* [https://www.thoughtworks.com](https://www.thoughtworks.com)
* Beware of framework/language/technology’s [Hype Cycle](http://www.gartner.com/technology/research/methodologies/hype-cycle.jsp)
* [https://trello.com/b/lw96ei6d/books](https://trello.com/b/lw96ei6d/books)
* [https://www.safaribooksonline.com/library/view/lean-ux-2nd/9781491953594/](https://www.safaribooksonline.com/library/view/lean-ux-2nd/9781491953594/)
* [DevOpsSec](http://www.oreilly.com/webops-perf/free/files/devopssec.pdf)
* JavaScript Testing
	* Sinon - mocking and stubbing
	* Protactor - end to end tests (use with Selenium)
	* Jasmine framework 
	* Mocha framework
	* Chai - assertion library
	* Karma test runner - run tests in browsers - can run in BrowserStack or SauceLabs
	* Protractor for Angular (end-to-end test framework)
	* [Nightwatch](http://nightwatchjs.org/) end-to-end for automated browser based apps 
* AWS Device Farm alongside BrowserStack and SauceLabs
* PaaS
	* VSTS - Azure App Services
	* CodeStar - AWS
	* OpenShift - RedHat
* Tools
	* Jira
	* Wiki
	* Chat/IM - slack, hipchat
