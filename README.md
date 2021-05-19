# spot.js

**Track mouse position relative to elements in your website.** With spot.js, you
can:

- Add the CSS class "spot-perspective" to any element on a website to
  automatically create a 3D perspective effect with the mouse's position as a
  focus point.
- Add the CSS class "spot-shadow" to any element on a website to automatically
  create dynamic shadows relative to the mouse's position.
- Add the CSS class "spot-rotate" to any element on a website to automatically
  rotate an element to face wherever the mouse is.
- Track mouse angle relative to an element's horizontal axis.
- Track mouse distance relative to an element's center.
- Have an easy time developing with on-screen helpers by adding the CSS class
  "spot-indicator" to any element on a website.
- **Get creative** with mouse events using CSS transforms.

## Installation

> Note: this section is WIP while I rewrite this.

And voila! Now you can add the following classes to any element on your website
to create different effects:

- **spot-perspective**: gives the element a **dynamic perspective and 3D
  rotation** effect which changes on mouse move, to simulate the elements
  "looking at" the mouse cursor. Uses
  `transform: perspective() rotateX() rotateY();`
- **spot-shadow**: gives the element a **dynamic drop-shadow** filter which
  changes on mouse move, to simulate a light coming from your mouse cursor. Uses
  `filter: drop-shadow();`
- **spot-rotate**: this CSS class **rotates** the element to face your mouse
  cursor and updates on mouse move. Uses `transform: rotate;`
- **spot-indicator**: this adds helpful **debugging overlays** to the selected
  element. The info shown stands for distance between the mouse cursor and the
  element's center and the degree (related to the horizontal axis from the
  center of the element) at which your mouse cursor stands in every instant.
- **spot-area**: add this CSS class to any element to restrict where **spot.js**
  will listen to mouse move events. If no element has been given this class, the
  entire window will listen to mouse move events.

## Current development goals

- This is currently undergoing a TypeScript rewrite. See the
  [rewrite tracking issue here](https://github.com/fnune/spot.js/issues/5).
- I'm planning to add many more effects to this library. Feel free to contribute
  with your own ideas.
- There are several performance issues that need to be tackled. This is mostly
  due to the nature of CSS filters but I guess I can also improve my throttling
  function and probably use `requestAnimationFrame();` or something. Suggestions
  are welcome.
- The shadow effect doesn't work well together with the rotation effect. They
  work great separately though.

## License

See the [LICENSE](/LICENSE.md) file for license rights and limitations (MIT).

## Feel free to collaborate!
