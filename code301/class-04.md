# Code 301 - Reading Notes

## React and Forms

### Forms
<!-- https://reactjs.org/docs/forms.html -->
1. What is a ‘Controlled Component’?
    - An input form element whose value is controlled by React.
2. Should we wait to store the users responses from the form into state when they submit the form OR should we update the state with their responses as soon as they enter them? Why.
    - Update it as they type so that it updates the value of the state and subsequently the form.
3. How do we target what the user is entering if we have an event handler on an input field?
    - event.target.values

### Conditional Operator
<!-- https://codeburst.io/javascript-the-conditional-ternary-operator-explained-cac7218beeff -->
1. Why would we use a ternary operator?
    - less code, same result
2. Rewrite the following statement using a ternary statement:

  ```javascript
  if(x===y){
 console.log(true);
  } else {
 console.log(false);
  }
  ```

```javascript
x===y ? console.log(true) : console.log(false);
```

## Thing I want to know more about

- I would love to know more about using the react forms.
- I noticed the event handler examples and thought that might have solved my coding problems last night when trying to select something identifiable from my hornedBeast and pass it to my selectedBeast.

[BACK TO HOME](../README.md)
