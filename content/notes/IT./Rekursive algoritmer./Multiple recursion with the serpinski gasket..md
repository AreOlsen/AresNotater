# Multiple recursion with the serpinski gasket.

So for, the examples of [[Rekurisve algoritmer.|recursion]] that we've taken alook at requires you to make one recursive call each time. But sometimes multiple calls are required. 
A good example is the mathematical fractal known as sierpinksi gasket.

The way the sierpinski gasket works is by dividing a square into multiple smaller squares and choosing the top right top left and bottom right corners and then doing the same recursive call in there. Heres the approach more simplified.

Divide into four squares, and mark the top right, top left and bottom right corners.
Like so:
![250](https://cdn.kastatic.org/ka-perseus-images/3245c7f409cc2b05db1d793a37ec46b9084e6a7a.jpg)

Now continue and do it once more with the crossed out squares.
![250](https://cdn.kastatic.org/ka-perseus-images/5a9680906f1a9b37ebb26630d612841df8295bbf.jpg)

And do it more:
![250](https://cdn.kastatic.org/ka-perseus-images/1ea1273d2a05dc8c5e71e071faac2c768d3b7389.jpg)

Perhaps once more?:
![250](https://cdn.kastatic.org/ka-perseus-images/5ef0e024c7157e8a5772f0277d49d65e62c51da4.jpg)

And we continue so forth until we reach a minimum size for the squares which we decide ourselves. Lets stop here, and of course some colouring would be nice:
![250](https://cdn.kastatic.org/ka-perseus-images/dfd834ca82cc24414aec63f2c86dc9690b19d840.jpg)

We call the same recursive call for each crossed out square which means for each level of depth we go we have to call the recursive function three times for :
* Call for the top left corner
* Call for the top right corner
* Call for bottom right corner.

The multiple recursion calls at the same time makes it multiple recursive.

Heres how we can put this multiple recursion algorithm into psuedocode.
* Determine how small the current square is.
	* If it is below the minmum size we set fill in the cube with colour.
* Otherwise divide the square into uppoer left, upper right, bottom right.
	* recursively solve
		* Draw sierpinski gasket in upper right
		* Draw sierpinski gasket in upper left
		* Draw sierpinski gasket in bottom right

Because you call three recursive calls. It is considered a multiple recursive algorithm.

Here's how to put this algorithm into javascript code.
```js
var dim = 240;
var min = 8;
var drawgasket = function(x,y,dim)
{
	if(dim<=min){
	rect(x,y,dim,dim)
	};
	else {
		var newdim = dim/2;
		drawgasket(x,y,newdim);
		drawgasket(x+newdim,y,newdim);
		drawgasket(x+newdim,y+newdim,newdim);
		}
};
```

