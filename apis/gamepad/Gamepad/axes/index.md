---
title: 'axes'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/Web/Guide/API/Gamepad)'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/gamepad/Gamepad
    href: /apis/gamepad/Gamepad
  return:
    predicate: 'Returns an object of type '
    value: ''
    href: /apis/gamepad/Gamepad
standardization_status: 'W3C Working Draft'
summary: 'Array of values for all axes of the gamepad. Each entry in the array is a floating point value in the range -1.0 - 1.0, representing the axis position from the lowest value (-1.0) to the highest value (1.0).'
tags:
  - API_Object_Properties
  - API
  - Gamepad
uri: apis/gamepad/Gamepad/axes

---
## Summary

Array of values for all axes of the gamepad. Each entry in the array is a floating point value in the range -1.0 - 1.0, representing the axis position from the lowest value (-1.0) to the highest value (1.0).

Property of [apis/gamepad/Gamepad](/apis/gamepad/Gamepad)[apis/gamepad/Gamepad](/apis/gamepad/Gamepad)

## Syntax

**Note**: This property is read-only.

``` js
var result = object.axes;
```

## Return Value

Returns an object of type

array of doubles.

## Examples

The Gamepad API provides a function, [Navigator.getGamepads](/dom/Navigator/getGamepads), that returns a list of all devices currently visible to the web page, as an array of Gamepad objects. When a gamepad is connected, this example reports its index, id, number of buttons, number of axes, and when the gamepad data was updated.

``` js
window.addEventListener("gamepadconnected", function(e) {
  var gp = navigator.getGamepads()[e.gamepad.index];
  console.log("Gamepad connected.");
  console.log("Gamepad index:", gp.index);
  console.log("Gamepad id:", gp.id);
  console.log("Gamepad buttons:", gp.buttons.length);
  console.log("Gamepad axes:", gp.axes.length);
  console.log("Gamepad last updated:", gp.timestamp);
});
```

## Related specifications

[W3C Gamepad Specification](https://dvcs.w3.org/hg/gamepad/raw-file/default/gamepad.html)
:   W3C Working Draft
