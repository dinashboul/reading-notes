# How to Building ?

## Custom Hooks

### Hooks are a new addition in React 16.8. They let you use state and other React features without writing a class.

## Lifting State Up

### Several components need to reflect the same changing data. We recommend lifting the shared state up to their closest common ancestor. Let’s see how this works in action.

**In React, sharing state is accomplished by moving it up to the closest common ancestor of the components that need it. This is called “lifting state up**

### Some Notes:

- Instead of trying to sync the state between different components, you should rely on the top-down data flow.

- Lifting state involves writing more “boilerplate” code than two-way binding approaches, but as a benefit, it takes less work to find and isolate bugs.

## React:

**The premier way to build big, fast Web apps with JavaScript.**

### Steps for work  With A Mock :

1- Break The UI Into A Component Hierarchy

2- Build A Static Version in React

3-  Identify The Minimal (but complete) Representation Of UI State
    **To make your UI interactive, you need to be able to trigger changes to your underlying data model.**

4- Identify Where Your State Should Live
**React is all about one-way data flow down the component hierarchy. It may not be immediately clear which component should own what state. This is often the most challenging part for newcomers to understand**

5- Add Inverse Data Flow

## MEMOIZATION

###  is an optimization technique that allows an increase in the performance of a program by storing the results of some expensive function so that we don’t need to call that function when the same inputs are given.

### IMPLEMENT MEMOIZATION IN REACT

**PureComponent and memo hook which allow us to implement memoization in React.**
**React also gives us a memo() hook to apply memoization for functional components.**

### PURECOMPONENT
**PureComponent is similar to Components in React except that PureComponent implements shouldComponentUpdate() with shallow prop and state comparison and Components does not.**

### USE MEMOIZATION
- **We should only use memoization when there is a clear benefit for doing so.**
- **Memoization can increase performance for some functions.**
- **if we use it for every component rendering, it might decrease performance since it stores results that increase memory used for the program.**






