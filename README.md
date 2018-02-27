# keyboard

An instance class which hooks into keyup and keydown, and keeps track of all the key pressed.

[![NPM version][npm-image]][npm-url]
[![build status][travis-image]][travis-url]
[![node version][node-image]][node-url]
[![npm download][download-image]][download-url]

[npm-image]: http://img.shields.io/npm/v/@jworkshop/keyboard.svg
[npm-url]: http://npmjs.org/package/@jworkshop/keyboard
[travis-image]: https://img.shields.io/travis/jworkshop/keyboard.svg
[travis-url]: https://travis-ci.org/jworkshop/keyboard
[node-image]: https://img.shields.io/badge/node.js-%3E=_0.10-green.svg
[node-url]: http://nodejs.org/download/
[download-image]: https://img.shields.io/npm/dm/@jworkshop/keyboard.svg
[download-url]: https://npmjs.org/package/@jworkshop/keyboard

## install

[![NPM](https://nodei.co/npm/@jworkshop/keyboard.png)](https://nodei.co/npm/@jworkshop/keyboard/)

## Usage

```javascript
/* Get the container for the keyboard. */
let container = document.getElementById("container");

/* Create a keyboard instance, with the element as its container.
 * This is to allow the keyboard to monitor all key events from the container. */
let keyboard = new Keyboard(container);

/** Append the keyboard to the a DOM element and event handlers to it. */
keyboard.attach(container);

/** Detach the keyboard from DOM element and event handlers from it. */
keyboard.detach();

/** Toggle value for keyboard prevent default on all events. */
keyboard.setPreventDefault(preventDefault);

/** Toggle value for keyboard skipping further key down events. */
keyboard.setPreventHoldDownEvent(preventHoldDownEvent);

/** Bind an event handler to the key down event. */
keyboard.onKeyDown(event => { ... });

/** Unbind an event handler to the key down event. */
keyboard.removeKeyDown(event => { ... });

/** Unbind all event handlers from the key down event. */
keyboard.clearKeyDown();

/** Bind an event handler to the key up event. */
keyboard.onKeyUp(event => { ... });

/** Unbind an event handler to the key up event. */
keyboard.removeKeyUp(event => { ... });

/** Unbind all event handlers from the key up event. */
keyboard.clearKeyUp();

/** Checks if a given keyCode has been pressed. */
keyboard.hasKeyPressed(keyCode);

/** Get the last keyCode that has been pressed. */
keyboard.getLastKeyPressed();
```
