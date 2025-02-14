
```javascript
let variation = 0.1
let slices = 20
let grays = []
let colours = [0.5, 1, 0 , 0.6, 0.7]
let colorCount = colours.length 

for( var i = 0 ; i <= slices ;  i++)
{
	let gray = i / slices // Math.sin((i*Math.PI)/(slices*2))
	let colourID = Math.round(Math.floor(gray * colorCount)/colorCount)
	let colour = colours[colourID]
	let factor = (1.0+((variation/2.0)*((colorCount*gray)-0.5))) ;
	console.log("i", i, "gray", gray.toFixed(3), "colourID", colourID, "colour", colour, "factor", factor.toFixed(3), "factor * colour", (factor * colour).toFixed(3))
	//grays.push(gray)
}

```

