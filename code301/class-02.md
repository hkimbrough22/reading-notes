# Code 301 - Reading Notes

## State and Props

### State
<!-- https://medium.com/@joshuablankenshipnola/react-component-lifecycle-events-cb77e670a093 -->
- Based off the diagram, what happens first, the ‘render’ or the ‘componentDidMount’?
Render
- What is the very first thing to happen in the lifecycle of React?
Mounting - constructor
- Put the following things in the order that they happen: componentDidMount, render, constructor, componentWillUnmount, React Updates
constructor, render, React updates, componentDidMount, componentWillUnmount
- What does componentDidMount do?
After a component mounts/is rendered this method runs.

### Props
<!-- https://www.youtube.com/watch?v=IYvD9oBCuJI -->

- What types of things can you pass in the props?
Arguments to a function. What you want your functions/classes to work with.
- What is the big difference between props and state?
State is inside a component, props is passed to a component and handled outside
- When do we re-render our application?
When state is updated.
- What are some examples of things that we could store in state?
Counters, errors, data types of use (objs, arrays, strings) to be used.

## Things I want to know more about


[BACK TO HOME](../README.md)