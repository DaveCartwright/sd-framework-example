## 2 Craft

### 2.1 Test Driven Development

Test Driven Development (TDD) is fundamental practice in which an automated test is written before the feature implementation, thus driving the API design, and encouraging SOLID principles. It has the secondary benefits of verifying that the implementation works, helping the code base communicate intent and providing a regression test suite for safe refactoring.

#### 2.1.1 Proficiencies

<details>
<summary><b> Intermediate </b></summary>

An intermediate software craftsperson…

- Habitually uses TDD when developing software
- Strives to write tests that are simple, maintainable, robust and communicate intent, but may not always succeed
- Writes integration tests to assert interactions with common backing services (other services, databases, file systems, etc)
- Avoids common TDD pitfalls
- May rely too heavily on mock objects / spies, resulting in overly brittle tests and higher maintenance
</details>

<details>
<summary><b>Advanced</b> </summary>

In addition, an advanced software craftsperson…

- Strives to keep the TDD cadence fast
- Consistently writes tests that are simple, maintainable, robust and communicate intent
- Writes integration tests to assert interactions with less common backing services (e.g. message brokers, ftp servers) and for complex scenarios (e.g. those involving time zones, inherent randomness, concurrency, etc)
- Critically evaluates and champions worthwhile testing tools
- Supports less proficient software engineers with TDD
- Encourages TDD within their team
</details>

<details>
<summary> <b>Expert</b> </summary>

An expert software craftsperson…

- Knows when to break the rules
- Encourages TDD beyond their team
- Contributes to the TDD body of work through articles, public speaking, open source, etc
</details>

#### 2.1.2 Resources

- [TDD](https://codemanship.co.uk/tdd_jasongorman_codemanship.pdf) by Jason Gorman [pdf]
- [Test-Driven Development](https://tdd.mooc.fi/) [website]
- [Test Driven Development: By Example](https://www.amazon.co.uk/Test-Driven-Development-Addison-Wesley-Signature/dp/0321146530) by Kent Beck [book]
- [Making a mockery of TDD](https://avdi.codes/making-a-mockery-of-tdd/) [article]
- [The Most Important TDD Rule](https://enterprisecraftsmanship.com/posts/most-important-tdd-rule/) [article]
- [TDD Anti Patterns](https://github.com/cressie176/engineering/wiki/TDD-Anti-Patterns) [collected from Stack Overflow]
- [The Object Mother design pattern](https://martinfowler.com/bliki/ObjectMother.html) [article]
- [Yup By Example](https://www.npmjs.com/package/yup-by-example) [Test data generation Node.js library]
- [Nock](https://www.npmjs.com/package/nock) [HTTP Server mocking Node.js library]
- [zUnit](https://www.npmjs.com/package/zunit) [Unit testing Node.js library]
- [Building a Pragmatic Unit Test Suite](https://www.pluralsight.com/courses/pragmatic-unit-testing) [Pluralsight]

---

### 2.2 Behaviour Driven Development

Behaviour Driven Development (BDD) is an evolution of TDD which aims to improve how unit tests communicate. It has an additional benefit of providing an abstraction layer making it a good choice for using in combination with functional web tests. While useful, you can be a software craftsperson without experience of BDD

#### 2.2.1 Proficiencies

<details>
<summary><b>Intermediate</b></summary>
A software craftsperson with intermediate BDD skills may…

- selectively use BDD to express business rules
- selectively use BDD to create an abstract layer for functional web tests
</details>

#### 2.2.2 Resources

- [Introducing BDD](https://dannorth.net/introducing-bdd/) [article]
- [Cucumber](https://cucumber.io/) [framework]
- [Serenity](https://serenity-bdd.info/what-is-serenity/) [framework]
- [Example BDD Scenario](https://github.com/cressie176/engineering/wiki/BDD-Example) [article]
- [Yadda](https://acuminous.gitbooks.io/yadda-user-guide/content/en/) User Guide [official documentation]
- [BDD and the Page Object Pattern](https://github.com/acuminous/yadda/tree/master/examples/nightwatch) [example]

---

### 2.3 Clean Code

Clean Code describes code that is objectively well factored: Functions will be very small (typically less than 6 statements), They should do one thing well and operate at a single level of abstraction, They should not have side effects, They should take few arguments, And they should contain almost no conditional logic except for guard conditions and default assignments.

It can be difficult to imagine writing complex applications with such small functions and little conditional logic, but it is possible.

For an example take a look at [Twiki](https://github.com/acuminous/twiki-gherkish-feature-parser) which parses [BDD](https://cucumber.io/docs/gherkin/reference/) specifications.

- Naming is deliberate and consistent
- The average number of statements per function is under 4
- The biggest class has 114 lines
- There are nine if statements and no else/case statements at all.

Consequently, the code is flat and easy to read.

Twiki achieves this by defining a good domain model and using polymorphism to implement conditional behaviour is required. It can also help to keep conditional logic at the peripheries of the code base. You also need to encapsulate state by minimising public properties, accessors and mutators.

#### 2.3.1 Proficiencies

<details>
<summary><b>Intermediate</b></summary>
An intermediate software craftsperson…

- Can articulate the Clean Code principles
- Strives to write Clean Code
- Habitually improves the cleanliness of the code base through minor refactors
- May unknowingly introduce or hide complexity when trying to simplify or innovate
</details>

<details>
<summary><b>Advanced</b></summary>

In addition, an advanced software craftsperson…

- Consistently writes Clean Code
- Systematically refactors problem code into Clean Code
- Supports less proficient software engineers writing Clean Code
- Encourages Clean Code within their team
</details>

<details>
<summary><b>Expert</b></summary>

In addition, an expert software craftsperson …

- Encourages Clean Code beyond their team
</details>

#### 2.3.2 Resources

- [Clean Code: A Handbook of Agile Software Craftsmanship](https://www.amazon.co.uk/Clean-Code-Handbook-Software-Craftsmanship/dp/0132350882) by Bob Martin [book]
- [Clean Code](https://www.youtube.com/watch?v=7EmboKQH8lM&t=2411s) [video]
- [It’s probably time to stop recommending Clean Code](https://qntm.org/clean) [article]
- [When is code done?](https://www.timcosta.io/when-is-a-project-done/) [article]

---

### 2.4 Production Readiness

#### 2.4.1 Proficiencies

<details>
<summary><b> Intermediate </b></summary>

An intermediate software craftsperson …

- Logs safely, judiciously and in a structured way
- Builds observability into their software applications
- Anticipates and prevents classic software failure modes
- Avoids wasting system resources, but in doing so, may introduce undesirable complexity
- Ensures all code is managed in source control
- Ensures code artefacts are built in a clean environment, from source control
</details>

<details>
<summary><b>Advanced</b></summary>

In addition, an advanced software craftsperson…

- Writes software which starts up and shuts down gracefully
- Incorporates logging and observability in a non-invasive, testable manner
- Anticipates and prevents situation specific failure modes
- Encourages production readiness within their team and the wider organisation
- Carefully balances optimisation against undesirable complexity
</details>
<details>
<summary><b>Expert</b></summary>

In addition, an expert software craftsperson…

- Makes production readiness the path of least resistance within their team and the wider organisation
</details>

#### 2.4.2 Resources

- [The Twelve-Factor App](https://12factor.net/) [website]
- [Principles of Unix software design](https://paulvanderlaken.com/2019/09/17/17-principles-of-unix-software-design/) [article]
- [Domain Oriented Observability](https://martinfowler.com/articles/domain-oriented-observability.html) [article]
- [The Eight Fallacies of Distributed Systems](https://www.simpleorientedarchitecture.com/8-fallacies-of-distributed-systems/) [article]
- [Thirteen API caching mistakes to avoid](https://tedspence.com/thirteen-api-caching-mistakes-to-avoid-d9b09872f346) [article]

---

---
