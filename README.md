# easyWaypoints
This algoithm is built on top of the waypoints.js library. Waypoints is a library that makes it easy to execute a function whenever you scroll to an element. My repo should make it even more painless to use waypoints in your project.

## Installation
===========
npm install waypoints
```js
<script src="easy-waypoints.js"></script>
```

## Usage
```js
function createWaypoint(element, classToToggle, offset, cb) {
  return jQuery(element).waypoint(function(direction) {
    jQuery(element).toggleClass(classToToggle);
    if (typeof cb !== "undefined") {
      cb(element, classToToggle, offset, direction);
    }
  }, { offset: offset });
}
```
