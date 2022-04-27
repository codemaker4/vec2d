# vec2d
A simple 2d vector library for JavaScript.

## usage
Either download cmvec2d.js or import the script with this script tag:

```html
<script src="https://raw.githubusercontent.com/codemaker4/vec2d/master/vec2d.js"></script>
```

## examples
```js
let a = new Vec2d(4,0) // create a vector of length 4
let b = new Vec2d(0,3) // create a purpendicular vector of length 3
let c = a.copy().add(b) // create a new diagonal vector
console.log(c.mag()) // 5
// a^2 + b^2 = c^2
```
```js
let pos = new Vec2d(0,0) // define a postiion
let vel = new Vec2d(0,0) // define a velocity
let grav = new Vec2d(0,9.8) // define a gravitational force

setInterval(()=>{
  vel.add(grav) // apply the force
  pos.add(vel) // move by velocity
},1000/60); // do every frame
```
