# Software Design Patterns Simplified

**A design pattern is only a description or template for how to solve a problem! that can be used in many different situations. So every design pattern provide a solution to commonly occurring software design problems. Patterns are formalized best practices that the Software Developer can use to solve common problems when designing an application.**

## Below is thew difference between, Programming Paradigms, Architectural Patterns, Design Patterns and Design Principles:

- Programming Paradigms: A way to classify programming languages based on their coding styles and features. Some paradigms are concerned mainly with implications for the execution model of the language (Procedural, Functional, Object-oriented…).

-Architectural Patterns: Reusable solution to a commonly occurring problem in software architecture within a given context. They are similar to software design pattern but have a broader scope (MVC, Micro-services, Layered...).

- Design Patterns: Reusable solution to a commonly occurring problem in software design within a given context. It is a description or template for how to solve a problem that can be used in many different situations (Bridge, Builder, Strategy…).

- Design Principles: Represent a set of guidelines that help developers to avoid having a bad design. Writing code according to proven principles helps achieving code maintainability and simplicity(KISS, Liskov Substitution, Inversion of Control…).

### There is 3 major types of design patterns:

#### Creational Patterns:
- Factory Method. 
- Singleton
- Abstract Factory

#### Structural Patterns:
- Facade
- Adapter
- Decorator

#### Behavioral Patterns:
- Observer
- Mediator
- Chain of Responsibility.


### What is Risk Analysis in Software Testing and how to perform it?

**In Software Testing, risk analysis is the process of identifying the risks in applications or software that you built and prioritizing them to test. After that, the process of assigning the level of risk is done. The categorization of the risks takes place, hence, the impact of the risk is calculated.**

#### Why use Risk Analysis?

**After knowing about the risk areas, it helps the developers and managers to mitigate the risks. When a test plan has been created, risks involved in testing the product are to be taken into consideration along with the possibility of the damage they may cause to your software along with solutions.**

### possible risks 

- Use of new hardware

- Use of new technology

-Use of new automation tool

- The sequence of code

- Availability of test resources for the application

####  risks that are unavoidable

- The time that you allocated for testing

- A defect leakage due to the complexity or size of the application

- Urgency from the clients to deliver the project

- Incomplete requirements

#### points can be taken care

- Conduct Risk Assessment review meeting

- Use maximum resources to work on high-risk areas

- Create a Risk Assessment database for future use

- Identify and notice the risk magnitude indicators: high, medium, low.

#### risk magnitude indicators

- High: means the effect of the risk would be very high and non-tolerable. The company might face loss.

- Medium: it is tolerable but not desirable. The company may suffer financially but there is a limited risk.

- Low: it is tolerable. There lies little or no external exposure or no financial loss.



#### Risk Identification

**There are different sets of risks included in the risk identification process. Those are as follows:**

- Business Risks: This risk is the most common risk associated with our topic. It is the risk that may come from your company or your customer, not from your project.

-Testing Risks: You should be well acquainted with the platform you are working on, along with the software testing tools being used.

- Premature Release Risk: a fair amount of knowledge to analyze the risk associated with releasing unsatisfactory or untested software is required

- Software Risks: You should be well versed with the risks associated with the software development process.

#### The perspective of Risk Assessment

There are three perspectives of Risk Assessment:

- Effect

- Cause

- Likelihood

## Dependency Injection

**transferring the task of creating the object to someone else and directly using the dependency is called dependency injection.**

###  There are basically three types of dependency injection:

- constructor injection: the dependencies are provided through a class constructor.

- setter injection: the client exposes a setter method that the injector uses to inject the dependency.

-interface injection: the dependency provides an injector method that will inject the dependency into any client passed to it. 

Clients must implement an interface that exposes a setter method that accepts the dependency.

#### responsibilities

- Create the objects

- Know which classes require those objects

- And provide them all those objects

#### Benefits of using DI
- Helps in Unit testing.

- Boiler plate code is reduced, as initializing of dependencies is done by the injector component.

- Extending the application becomes easier.

- Helps to enable loose coupling, which is important in application programming.

#### Disadvantages of DI

- It’s a bit complex to learn, and if overused can lead to management issues and other problems.

- Many compile time errors are pushed to run-time.

- Dependency injection frameworks are implemented with reflection or dynamic programming. This can hinder use of IDE automation, such as “find references”, “show call hierarchy” and safe refactoring.


### Libraries and Frameworks that implement DI
- Spring (Java)

- Google Guice (Java)

- Dagger (Java and Android)

- Castle Windsor (.NET)

- Unity(.NET)









