# Code 201 - Reading Notes
<!-- All notes were taken from Reading assignment 14 references in Jon Duckett's book and online references -->
## Transform, Transitions, Animations
### Transform
- The `transform` property comes in two different settings, two-dimensional and three-dimensional. Each of these come with their own individual properties and values.

- Syntax is `transform` property followed by the value. The value specifies the transform type followed by a specific amount inside parentheses.

``` css
div {
  -webkit-transform: scale(1.5);
     -moz-transform: scale(1.5);
       -o-transform: scale(1.5);
          transform: scale(1.5);
}
```

- The `transform` property accepts a handful of different values. The `rotate` value provides the ability to rotate an element from 0 to 360 degrees.

  - Using a positive value will rotate an element clockwise, and using a negative value will rotate the element counterclockwise. The default point of rotation is the center of the element, 50% 50%, both horizontally and vertically. Later we will discuss how you can change this default point of rotation.

- Using the `scale` value within the `transform` property allows you to change the appeared size of an element. 
  - The default scale value is 1, therefore any value between .99 and .01 makes an element appear smaller while any value greater than or equal to 1.01 makes an element appear larger.

### Transitions
- The easiest way for determining styles for different states is by using the `:hover`, `:focus`, `:active`, and `:target` pseudo-classes.

- There are four transition related properties in total, including `transition-property`, `transition-duration`, `transition-timing-function`, and `transition-delay`. Not all of these are required to build a transition, with the first three are the most popular.

In the example below the box will change its background color over the course of 1 second in a linear fashion.

```css
.box {
  background: #2db34a;
  transition-property: background;
  transition-duration: 1s;
  transition-timing-function: linear;
}
.box:hover {
  background: #ff7b29;
}
```
  - `transition-property` - The transition-property property determines exactly what properties will be altered in conjunction with the other transitional properties. By default, all of the properties within an element’s different states will be altered upon change. However, only the properties identified within the transition-property value will be affected by any transitions.

  - `transition-duration` - The duration in which a transition takes place is set using the transition-duration property. The value of this property can be set using general timing values, including seconds (s) and milliseconds (ms). These timing values may also come in fractional measurements, .2s for example.
  
  - `transition-timing-function` - The `transition-timing-function` property is used to set the speed in which a transition will move. Knowing the duration from the `transition-duration` property a transition can have multiple speeds within a single duration. A few of the more popular keyword values for the `transition-timing-function` property include `linear`, `ease-in`, `ease-out`, and `ease-in-out`.

  - `transition-delay` - The `transition-delay` property sets a time value, seconds or milliseconds, that determines how long a transition should be stalled before executing. As with all other transition properties, to delay numerous transitions, each delay can be declared as comma separated values.

  - ***There is a shorthand property, transition, capable of supporting all of these different properties and values. Using the transition value alone, you can set every transition value in the order of transition-property, transition-duration, transition-timing-function, and lastly transition-delay. Do not use commas with these values unless you are identifying numerous transitions.***

- When transitioning multiple properties you can set multiple durations, one for each property. As with the transition-property property value, multiple durations can be declared using comma separated values. The order of these values when identifying individual properties and durations does matter. For example, the first property identified within the transition-property property will match up with the first time identified within the transition-duration property, and so forth.


[BACK TO HOME](../README.md)