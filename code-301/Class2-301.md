# Class2 Read

## Based off the diagram, what happens first, the ‘render’ or the ‘componentDidMount’?

render

### What is the very first thing to happen in the lifecycle of React?

constructor

### Put the following things in the order that they happen?

When an instance of a component is being created and inserted into the DOM it occurs during the mounting phase. Constructor, static getDerivedStateFromProps, render, componentDidMount, and UNSAFE_componentWillMount all occur in this order during mounting.

### What types of things can you pass in the props?

props can be pass any JavaScript data type from integers over objects to arrays.

 ### What is the big difference between props and state?

The key difference between props and state is that state is internal and controlled by the component itself while props are external and controlled by whatever renders the component.

### When do we re-render our application?

When the state changes in the parent component (in this case, App ), the two Tile components will re-render, even though the second one doesn't even receive any props. The red dots again represent renders. In React, this means calling the render function

### What are some examples of things that we could store in state?

A count, such as a score or time, string ,numbers