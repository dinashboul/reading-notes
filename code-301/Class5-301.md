# React Docs - Thinking in React

## What is the single responsibility principle and how does it apply to components

 single responsibility principle, that is, a component should ideally only do one thing. If it ends up growing, it should be decomposed into smaller subcomponents.

Since you’re often displaying a JSON data model to a user, you’ll find that if your model was built correctly, your UI (and therefore your component structure) will map nicely. That’s because UI and data models tend to adhere to the same information architecture. Separate your UI into components, where each component matches one piece of your data model.

## What does it mean to build a ‘static’ version of your application?

renders your data model, you’ll want to build components that reuse other components and pass data using props. props are a way of passing data from parent to child. If you’re familiar with the concept of state, don’t use state at all to build this static version. State is reserved only for interactivity, that is, data that changes over time. Since this is a static version of the app, you don’t need it.

## Once you have a static application, what do you need to add?

using props. props are a way of passing data from parent to child

## What are the three questions you can ask to determine if something is state?

is it passed in from a parent via props? If so, it probably isn’t state.

Does it remain unchanged over time? If so, it probably isn’t state.

Can you compute it based on any other state or props in your component? If so, it isn’t state.

## How can you identify where state needs to live?

* Identify every component that renders something based on that state.
* Find a common owner component (a single component above all the components that need the state in the hierarchy).
* Either the common owner or another component higher up in the hierarchy should own the state.
* If you can’t find a component where it makes sense to own the state, create a new component solely for holding the state and add it somewhere in the hierarchy above the common owner component.

## Higher-Order Functions

## What is a “higher-order function”?

Functions that operate on other functions, either by taking them as arguments or by returning them, are called higher-order functions

## Explore the greaterThan function as defined in the reading. In your own words, what is line 2 of this function doing?

it make function inside function to compare between them

## Explain how either map or reduce operates, with regards to higher-order functions

It builds a value by repeatedly taking a single element from the array and combining it with the current value. When summing numbers

## Things I want to know more about

i need to know about Higher-Order Functions
