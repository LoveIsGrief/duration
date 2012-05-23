# duration - Missing extension to JavaScript's Date object

Useful methods for handling time duration in JavaScript

_It was part of [es5-ext](https://github.com/medikoo/es5-ext) project, now it's individual package._

## Installation

To use it with node.js:

	$ npm install duration

You can easily create browser bundle with help of [modules-webmake](https://github.com/medikoo/modules-webmake)

## Example usage:

```javascript
var createDuration = require('duration')

var duration = createDuration(new Date(2000, 6, 7),
	new Date(2010, 8, 13, 3, 23, 8, 456));

console.log("Years: ", duration.years);
console.log("Months: ", duration.months);
console.log("Days: ", duration.days);
console.log("Hours: ", duration.hours);
console.log("Minutes: ", duration.minutes);
console.log("Seconds: ", duration.seconds);
console.log("Milliseconds: ", duration.milliseconds);

console.log("Trailing months: ", duration.month);
console.log("Trailing days: ", duration.day);
console.log("Trailing hours: ", duration.hour);
console.log("Trailing minutes: ", duration.minute);
console.log("Trailing seconds: ", duration.second);
console.log("Trailing milliseconds: ", duration.millisecond);

console.log("Default string representation: ", duration.toString());
console.log("Alternative string representation: ", duration.toString(1));
console.log("Custom string representation: ",
	duration.toString("H: %Hs m: %M"));
```
