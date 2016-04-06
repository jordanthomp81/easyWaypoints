# easyWaypoints
This algoithm is built on top of the waypoints.js library. Waypoints is a library that makes it easy to execute a function whenever you scroll to an element. My repo should make it even more painless to use waypoints in your project.

## Installation
npm install waypoints
```js
<script src="easy-waypoints.js"></script>
```

## Usage
Creates a standerd waypoint with the option of custom logic. To pass in the custom logic, just create a function with all the logic you would like to call when the waypoint is activated, then pass just the name of the function into this function without qoutes. Note that these waypoint functions are available to any js file in this project.

Example Single Waypoint: `createWaypoint('.that', 'is-active', '35%', animateThat)`
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

A loop for standerd waypoint creation. Also has the ability to pass in custom logic, and classToToggle. Both are optional.
Example Multiple Waypoints: `waypointer(['.that', '#that', '#this'], 'resolved', '10%', animate)`
```js
function waypointer(elementArray, classToToggle, offset, cb) {
  for (var i=0; i < elementArray.length; i++) {
    createWaypoint(elementArray[i], classToToggle, offset, cb);
  }
  return true;
}
```
