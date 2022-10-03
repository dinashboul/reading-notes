
# What is a Component?

is a modular, portable, replaceable, and reusable
set of well-defined functionality

_A component is a software object, intended to_ _interact with other components_

The primary objective of component-based architecture is to ensure component reusability. A component encapsulates functionality and behaviors of a software element into a reusable and self-deployable binary unit. There are many standard component frameworks such as COM/DCOM, JavaBean, EJB, CORBA, .NET, web services, and grid services. These technologies are widely used in local desktop GUI application design such as graphic JavaBean components, MS ActiveX components, and COM components which can be reused by simply drag and drop operation.

## Views of a Component

Object-oriented view

Conventional view

Process-related view

### Characteristics of Components

Reusability

Replaceable

_Not context specific_
_Extensible_

Encapsulated

Independent
Independent
A component is viewed as a set of one or more cooperating classes. Each problem domain class (analysis) and infrastructure class (design) are explained to identify all attributes and operations that apply to its implementation. It also involves defining the interfaces that enable classes to communicate and cooperate.

Conventional view

It is viewed as a functional element or a module of a program that integrates the processing logic, the internal data structures that are required to implement the processing logic and an interface that enables the component to be invoked and data to be passed to it.

Process-related view

In this view, instead of creating each component from scratch, the system is building from existing components maintained in a library. As the software architecture is formulated, components are selected from the library and used to populate the architecture.

### Advantages

Ease of deployment

Reduced cost

Ease of development

Reusable

Modification of technical complexity

Reliability

System maintenance and evolution

#### Props

_React is a component-based library that divides the UI into little reusable pieces._

#### how it work

_“Props” is a special keyword in React, which stands for properties and is being used for passing data from one component to another._

_But the important part here is that data with props are being_ _passed in a uni-directional flow. (one way from parent to child)_

#### Using Props in React

_Firstly, define an attribute and its value(data)_
_Then pass it to child component(s) by using Props_

_Finally, render the Props Data_
Things I want to know more about
 how it work in real project
