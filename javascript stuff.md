
```javascript

let a = 1

let variation = 0.1
let colorCount = 2.0
let slices = 10 
let grays = []
for( var i = 0 ; i <= slices ;  i++)
{
	let gray = Math.sin((i*Math.PI)/slices)
	console.log("i", i, gray)

}
 // [0,0.1,0.5,0.9,1]
/*
grays.forEach((gray) =>{

let factor = (1.0+((variation/2.0)*((colorCount*gray)-0.5))) ;

console.log("gray", gray,"factor", factor)
})
*/
```
