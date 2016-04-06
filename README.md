# easyWaypoints
This algoithm is built on top of the waypoints.js library. Waypoints is a library that makes it easy to execute a function whenever you scroll to an element. My repo should make it even more painless to use waypoints in your project.

## Installation
npm install waypoints
```js
<script src="easy-waypoints.js"></script>
```

## Usage
Creates a standerd waypoint with the option of custom logic. To pass in the custom logic, just create a function with all the logic you would like to call when the waypoint is activated, then pass just the name of the function into this function without qoutes. Note that these waypoint functions are available to any js file in this project.

Example Single Waypoint:
```js
createWaypoint('.that', 'is-active', '35%', animateThat)
createWaypoint('#this', 'debug', '-55%', animateThis)
```


Below is the loop for standerd waypoint creation. Also has the ability to pass in custom logic, and classToToggle. Both are optional.
Example Multiple Waypoints:
```js
waypointer(['.that', '#that', '#this'], 'resolved', '10%', animate)
waypointer(['.box', '#circle', '#nav'], 'active', '-25%')
```
For any arguments that are not needed just pass in a `null` value
