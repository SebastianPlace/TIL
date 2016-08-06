# bind and this
Use `bind` to set the context of a function to the parameter value.

For instance

```
let cat = {
  purSound: "squeek",
  makeNoise: function() {
		console.log(this.purSound)
  }
}
let makeCatNoise = cat.makeNoise;
makeCatNoise(); //undefined since purSound does not exist in this context

let boundMakeNoise = cat.makeNoise.bind(cat);
boundMakeNoise(); //works as bind makes `this` equal to cat
```
