# Code 301 - Reading Notes

## Passing Functions as Props

### Lists and Keys
<!-- https://reactjs.org/docs/lists-and-keys.html -->
1. What does .map() return?
    - A new index of an array.
2. If I want to loop through an array and display each value in JSX, how do I do that in React?
    - Use .map() to loop through and then assign that value at each index to a rendered element. With '{ }' as well.
3. Each list item needs a unique ____.
    - key
4. What is the purpose of a key?
    - Helps React identify which items have changed, are added, or are removed.
    - Gives elements a stable identity

### The Spread Operator
<!-- https://medium.com/coding-at-dawn/how-to-use-the-spread-operator-in-javascript-b9e4a8b06fab -->
1. What is the spread operator?
    - The spread syntax “spreads” an array into separate arguments for passing.
2. List 4 things that the spread operator can do.
    - Copying an array
    - Concatenating or combining arrays
    - Using Math functions
    - Using an array as arguments
    - Adding an item to a list
    - Adding to state in React
    - Combining objects
    - Converting NodeList to an array
3. Give an example of using the spread operator to combine two arrays.
    - myarr = 1, 2, 3
    - yourarr = 4, 5, 6
    - ourarr = [...myarr, ...yourarr];
    - ourarr = 1,2,3,4,5,6
4. Give an example of using the spread operator to add a new item to an array.
5. Give an example of using the spread operator to combine two objects into one.

### How to Pass Functions Between Components
<!-- https://www.youtube.com/watch?v=c05OL7XbwXU -->
1. In the video, what is the first step that the developer does to pass functions between components?
    - figures out where to create the function to change the state.
2. In your own words, what does the increment function do?
    - loops through and modifies state and then sets the new state.
3. How can you pass a method from a parent component into a child component?
    - props
4. How does the child component invoke a method that was passed to it from a parent component?
    - make sure to use the name that was given in props.

## Things I want to know more about

[BACK TO HOME](../README.md)