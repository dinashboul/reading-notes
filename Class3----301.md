# The map() method creates a new array populated with the results of calling a provided function on every element in the calling array.[1]

## What does .map() return?

map() returns a map object, which is an iterator that yields items on demand.

### If I want to loop through an array and display each value in JSX, how do I do that in React?

The map() method is the most commonly used function to iterate over an array of data in JSX.

### Each list item needs a unique key

### What is the purpose of a key? The keys in Map are ordered in a simple, straightforward way: A Map object iterates entries, keys, and values in the order of entry insertion

## The Spread Operator

### What is the spread operator?

The spread operator is a new addition to the set of operators in JavaScript ES6. It takes in an iterable (e.g an array) and expands it into individual elements. The spread operator is commonly used to make shallow copies of JS objects. Using this operator makes the code concise and enhances its readability.o one.

### List 4 things that the spread operator can do

Copying an array
Concatenating or combining arrays
Using Math functions
Using an array as arguments  

### Give an example of using the spread operator to combine two arrays

{  const fruits = ['🍏','🍊','🍌','🍉','🍍']
const moreFruits = [...fruits];
console.log(moreFruits) // Array(5) [ "🍏", "🍊", "🍌", "🍉", "🍍" ]
fruits[0] = '🍑'
console.log(...[...fruits,'...',...moreFruits]) //  🍑 🍊 🍌 🍉 🍍 ... 🍏 🍊 🍌 🍉 🍍}

### Give an example of using the spread operator to add a new item to an array

const fewFruit = ['🍏','🍊','🍌']
const fewMoreFruit = ['🍉', '🍍', ...fewFruit]
console.log(fewMoreFruit)

### Give an example of using the spread operator to combine two objects into one

const objectOne = {hello: "🤪"}
const objectTwo = {world: "🐻"}
const objectThree = {...objectOne, ...objectTwo, laugh: "😂"}
console.log(objectThree) // Object { hello: "🤪", world: "🐻", laugh: "😂" }
const objectFour = {...objectOne, ...objectTwo, laugh: () => {console.log("😂".repeat(5))}}
objectFour.laugh() // 😂😂😂😂😂

### Videos

### How to Pass Functions Between Components

### In the video, what is the first step that the developer does to pass functions between components?

all a method in the child component and pass that method as a prop to the child component

### In your own words, what does the increment function do?

Loop through the array and increase it the value that is maatch.

### How can you pass a method from a parent component into a child component?

using props

### How does the child component invoke a method that was passed to it from a parent component?

Wrap the Child component in a forwardRef.
Use the useImperativeHandle hook in the child to add a function to the Child.
Call the Child's function from the Parent using the ref, e.g. childRef.current.childFunction().
