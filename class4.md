
# What is a ‘Controlled Component’?

the input's value is always driven by the React state. While this means you have to type a bit more code,you can now pass the value to other UI elements too, or reset it from other event handlers.

form elements such as input, textarea, and select typically maintain their own state and update it based on user input. In React, mutable state is typically kept in the state property of components, and only updated with setState().

## Should we wait to store the users responses from the form into state when they submit the form OR should we update the state with their responses as soon as they enter them? Why.

The state is kept in sync with the input’s value, meaning that changing the input will update the state, and updating the state will change the input.


## How do we target what the user is entering if we have an event handler on an input field?

Since handleChange runs on every keystroke to update the React state, the displayed value will update as the user types.

With a controlled component, the input’s value is always driven by the React state. While this means you have to type a bit more code, you can now pass the value to other UI elements too, or reset it from other event handlers.

## The Conditional (Ternary) Operator Explained

 ## Why would we use a ternary operator?

Shorten your if statements into one line of code with the conditional operator

## Rewrite the following statement using a ternary statement: 

if(x===y){
  console.log(true);
} else {
  console.log(false);
}

### X==Y ? console.log(true) : console.log(false)

# Things I want to know more about

i need to know about modal