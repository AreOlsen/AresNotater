# Improving effiency of recursive functions.
Recursion can be an elegant soloution to a problem and many times lend to recursive implementation. However, recursivee algorithms can be very inffecient in both time and space.

For example in the [[Den faktorielle funksjonen.|recursive factorial function]]: 
These are the number of calls by some examples:

| Line of code   | Recursive calls                                                         | Total calls |
|----------------|-------------------------------------------------------------------------|-------------|
| Factorial(0);  | 0                                                                       | 1 call      |
| Factorial(2);  | Factorial(0)->Factorial(1)                                              | 3 calls     |
| Factorial(5);  | Factorial(4)->Factorial(3) ->Factorial(2)->Factorial(1) -> Factorial(0) | 6 calls     |
| Factorial(10); | Factorial(9)->Factorial(8) … … … Factorial(1)->Factorial(0)             | 11 calls    |



## Memoization.

Memoization makes a trade off between time and space .As long as the lookup is efficient and the function is called repeatedly, the computer can save time by using memory to store the memo, the memo being already computed data.

Memoization of Fibbonaci:
In the case of the factorial function: An algorithm only benefits from the optimization when a program makes repeated calls to a function (during execution). In some cases however memoization can save time for a single call to a recursive function.

An example of fibbonaci:
The first 10 fibbonaci numbers:
0,1,1,2,3,5,8,13,21,34.

A simple recursive algorithm:
```psuedocode
if n equals 0 or n equals 1 return n
else return fibbonaci(n-1)+fibbonaci(n-2)
```


To visualize this multiple recursion function: 
Fibbonaci(5);
<iframe width="688" height="387" src="https://www.youtube.com/embed/214lD7tWkz8" title="Recursive Fibonacci Calls (Diagrammed)" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

>[!NOTE] Note
>Legg merke til at fleire calls til 3,2,1 og 0 blir gjort. Når $n$ blir stor så blir dette svært ueffektivt. Til dømes fibbonaci(30) kaller fibbonaci(2) over ein halv million ganger. Her kan vi bruke memoization til å unngå å kalle til ein allerei utreknet del.

Den memoiserte versjonen av den rekursive fibbonaci algoritmen ser slik ut:
```psuedocode
if n equals 0 or n equals 1 return n;
else if (n is in memo) return memovalue[n];
else 
	calculate  fibbonaci(n-1)+fibbonaci(n-2)
	store result in memo
	return result
```

Now the algorithm looks like this:
Fibbonaci(5);
<iframe width="688" height="387" src="https://www.youtube.com/embed/hbveibMDHfg" title="Memoized Recursive Fibonacci Calls (Diagrammed)" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

The original algorithm required 15 functions calls with $n=5$, the memoized only used 6.
Here is a table showing number of calls bwetween 5 and 10 - n.
| n  | Original | Memoized |
|----|----------|----------|
| 5  | 15       | 9        |
| 6  | 25       | 11       |
| 7  | 41       | 13       |
| 8  | 67       | 15       |
| 9  | 109      | 17       |
| 10 | 177      | 19       |


## Bottom up.
Sometimes the best way to improve a recursive algorithm is to not use one at all.
In the case of the fibbonacci numbers an iterative technique can be better, this technique being called bottom-up. This can save both timr and space. When using a bottom up approach the computer solves the sub problems first and uses the partial results to arrive at the final result.

#### Psuedocode av fibbonacci numbers.

```psuedocode
if n equals 0 or n equals 1 return n;
else 
	create variable twoBehind (remember result of (n-2) init to 0.)
	create variable oneBehind (remember result of (n-1) init to 1.)
	create variable result (store the final result, init to 0.)
	repeat (n-1) times:
		update result to sum of twoBehind+oneBehind
		update twoBehind to store currentValue of oneBehind
		update oneBheind to stare value of result
	return result;
```

This method nevers makes a recursive callm it instead uses iteration to sum up the partial results and calculate the number. This has the same time complexity as the recursive one ([[Big O|O(n)]] but has the space complexity of O(1).

