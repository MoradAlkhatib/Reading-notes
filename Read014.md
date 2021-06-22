# CSS Transitions and Transforms for Beginners

DESIGN  CSS
This post will introduce you to CSS transitions and CSS transforms:
the CSS power couple. When used together, these properties allow you to create simple animations and add valuable interaction and visual feedback for your users.

Just remember when adding any kind of movement to your project to keep it simple,
subtle, and consistent. The movement you create should convey meaning, always enhancing, not distracting from the interaction for your users.

So what are transforms and transitions? At their most basic level,
transforms move or change the appearance of an element, while transitions make the element smoothly and gradually change from one state to another.

## CSS transitions: an introduction
Let’s start with CSS transitions.
Transitions are the grease in the wheel of CSS transforms.
Without a transition, an element being transformed would change abruptly from one state to another.
By applying a transition you can control the change, making it smooth and gradual.
In this post I’ll be using transitions in conjunction with transforms. However, transitions can also be used elsewhere where elements change from one style to another (e.g., when a button changes color on hover).

There are two properties that are required in order for the transition to take effect:

transition-property
transition-duration
Note: Transition Shorthand
Each transition property can be defined individually, but for cleaner and faster code, it’s recommended that you use the transition shorthand.

Here’s the full shorthand sequence. Again, the first two properties are required.


div {
  transition: [property] [duration] [timing-function] [delay];
}
transition-property (required)
The transition-property specifies the CSS property where the transition will be applied. You may apply a transition to an individual property (e.g., background-color or tranform) or to all properties in the rule-set (i.e., all).

CSS syntax examples for transition-property
div {
  transition-property: all;
  transition-property: transform;
}
## transition-duration (required)
The transition-duration property specifies the time span of the transition. You can specify in seconds or milliseconds.
CSS transforms: an introduction
Now that we reviewed how to make smooth and gradual transitions,
let’s look at CSS transforms - how to make an element change from one state to another.
With the CSS transform property you can rotate, move, skew, and scale elements.
(This post will only cover 2D transforms, but stay tuned for future blog posts on 3D transforms.)

Transforms are triggered when an element changes states,
such as on mouse-hover or mouse-click. The examples in this post will demonstrate transforms on mouse-hover.

For simplicity, I’ll only be using the unprefixed versions in my examples.
However, you may want to include prefixes to ensure it works in modern browsers.
transform-origin
The transform-origin property is separate from the transform property but works in tandem with it.
It allows you to specify the location origin of the transform. By default, the origin is in the center of the element.

For example, if you are using the transform: rotate property but want it to rotate not from the center,
but from the top left corner, you’d use the value 0% 0% or left top.
For the bottom right corner, you would use 0% 100% or right bottom, etc.
