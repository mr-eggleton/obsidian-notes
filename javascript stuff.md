


```javascript

let a = 1

let variation = 0.1
let colorCount = 2.0
let slices = 20
let colorCount = 5
let grays = []
for( var i = 0 ; i <= slices ;  i++)
{
	let gray = i / slices // Math.sin((i*Math.PI)/(slices*2))
	let colour = 
	console.log("i", i, gray)
	grays.push(gray)
}


grays.forEach((gray) =>{
	let factor = (1.0+((variation/2.0)*((colorCount*gray)-0.5))) ;
	console.log("gray", gray,"factor", factor)
})

```

