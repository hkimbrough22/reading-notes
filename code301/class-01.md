# Code 301 - Reading Notes

<!-- All references used were from Code 301 reading assignment 1 
https://www.tutorialspoint.com/software_architecture_design/component_based_architecture.htm

--- and ---

https://itnext.io/what-is-props-and-how-to-use-it-in-react-da307f500da0 
-->

## Introduction to React and Components

### Component-based Architecture

- Focuses on using individual, logical components that use well-defined methods, events, and properties.
- Divides the problem into sub-problems
- Primary objective is to ensure component reusability.

#### What is a component?

- A modular, portable, replaceable, and resuable piece of functionality.
- A software object that interacts with other components
- A unit of composition with a contractually-specified interface and explicit context dependencies.
- Can be object-oriented, conventional, or process-related.

#### What are the charactistics of a component?

- Reusability − in different situations, in different applications.

- Replaceable − freely substituted with other similar components.

- Not context specific − designed to operate in different environments and contexts.

- Extensible − can be extended from existing components to provide new behavior.

- Encapsulated − allow the caller to use its functionality, but doesn't expose details of the internal processes, any internal variables, or state.

- Independent − minimal dependencies on other components.

#### What are the advantages of using component based architecture?

- Ease of deployment − As new compatible versions become available, it is easier to replace existing versions with no impact on the other components or the system as a whole.

- Reduced cost − The use of third-party components allows you to spread the cost of development and maintenance.

- Ease of development − Components implement well-known interfaces to provide defined functionality, allowing development without impacting other parts of the system.

- Reusable − The use of reusable components means that they can be used to spread the development and maintenance cost across several applications or systems.

- Modification of technical complexity − A component modifies the complexity through the use of a component container and its services.

- Reliability − The overall system reliability increases since the reliability of each individual component enhances the reliability of the whole system via reuse.

- System maintenance and evolution − Easy to change and update the implementation without affecting the rest of the system.

- Independent − Independency and flexible connectivity of components. Independent development of components by different group in parallel. Productivity for the software development and future software development.

### React
React is a component-based library which divides the UI into little reusable pieces. In some cases, those components need to pass data to each other. The way this is done is by using props.

#### What is props short for?

- "properties" - used to pass data from one component to another.
- Keyword in React is "props".

#### How are props used in React?

1. Firstly, define an attribute and its value(data)
2. Then pass it to child component(s) by using Props
3. Finally, render the Props Data

#### What is the flow of props?

- Passed in a uni-directional way from parent to child.

## Things I Want To Know More About

- React as a whole
- props
- more efficient ways to use props

[BACK TO HOME](../README.md)