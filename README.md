# easyWaypoints
My algorithms built on top of the Waypoints.js library designed to make the use of waypoints as simple as possible


```function createWaypoint(element, classToToggle, offset, cb) {
  return jQuery(element).waypoint(function(direction) {
    jQuery(element).toggleClass(classToToggle);
    if (typeof cb !== "undefined") {
      cb(element, classToToggle, offset, direction);
    }
  }, { offset: offset });
}```

Creates a standerd waypoint with the option of custom logic. To pass in
the custom logic, just create a function with all the logic you would
like to call when the waypoint is activated, then pass just the name of the
function into this function without qoutes. Note that these waypoint functions are
available to any js file in this project
Example Single Waypoint: 
`createWaypoint('.that', 'is-active', '35%', animateThat)`
`createWaypoint('.that', 'is-active', '35%')`
