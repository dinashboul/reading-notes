#  Global state with React

**Different components may need to access and update the same state. This is achieved by introducing the global states in your app. The main purpose of the global state is to share a state among multiple components.**

##  Ways to communication :

- With a child component

- With a parent component

- With a sibling component

### State traveling down
- State traveling down through the hierarchy is best managed using the mutable state at the highest level 

-To determine immutable properties that define the lower-level components. 

- Even when these properties are updated, the lower-level component is updated rather than fully recreated.

### State traveling up

**need to pass down a callback function for a higher-level component to know the state.**

### State traveling sideways

**Various sub-components need to communicate updates between them. This can be achieved by passing state, using callback, up to a common parent component, and then passing it back down.**

## Context

### Provides a way to pass data through the component tree without having to pass props down manually at every level.

## When to Use Context?

- **is designed to share data that can be considered “global” for a tree of React components, such as the current authenticated user, theme, or preferred language**

- **If you only want to avoid passing some props through many levels, component composition is often a simpler solution than context.**

## To solve the prop drilling issue, we have State Management Solutions like Context API and Redux. 

## Context API :

### is a built-in React tool that does not influence the final bundle size, and is integrated by design.

### Steps to create Context :

- Create the Context
>>
    const Context = createContext(MockData);

- Create a Provider for the Context
>>
    const Parent = () => {
    return (
        <Context.Provider value={initialValue}>
            <Children/>
        </Context.Provider>
    )
    }

-  Consume the data in the Context

>> 
    const Child = () => {
    const contextData = useContext(Context);
    // use the data
    // ...
    }

##  What is Redux?

### Redux is a predictable state container for JavaScript apps.It helps you write applications that behave consistently, run in different environments (client, server, and native), and are easy to test.

**Open Source Library which provides a central store, and actions to modify the store.**




