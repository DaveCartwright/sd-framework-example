# Clean Code

Clean Code describes code that is objectively well factored: Functions will be very small (typically less than 6 statements), They should do one thing well and operate at a single level of abstraction, They should not have side effects, They should take few arguments, And they should contain almost no conditional logic except for guard conditions and default assignments.

It can be difficult to imagine writing complex applications with such small functions and little conditional logic, but it is possible.

For an example take a look at [Twiki](https://github.com/acuminous/twiki-gherkish-feature-parser) which parses [BDD](https://cucumber.io/docs/gherkin/reference/) specifications.

- Naming is deliberate and consistent
- The average number of statements per function is under 4
- The biggest class has 114 lines
- There are nine if statements and no else/case statements at all.

Consequently, the code is flat and easy to read.

Twiki achieves this by defining a good domain model and using polymorphism to implement conditional behaviour is required. It can also help to keep conditional logic at the peripheries of the code base. You also need to encapsulate state by minimising public properties, accessors and mutators.

## Proficiencies

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

## Resources

- [Clean Code: A Handbook of Agile Software Craftsmanship](https://www.amazon.co.uk/Clean-Code-Handbook-Software-Craftsmanship/dp/0132350882) by Bob Martin [book]
- [Clean Code](https://www.youtube.com/watch?v=7EmboKQH8lM&t=2411s) [video]
- [It’s probably time to stop recommending Clean Code](https://qntm.org/clean) [article]
- [When is code done?](https://www.timcosta.io/when-is-a-project-done/) [article]
