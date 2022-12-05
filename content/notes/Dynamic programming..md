# Dynamic prgramming.

[[Improving efficiency of recursive functions.#Memoization|Memoization]] and [[Improving efficiency of recursive functions.#Bottom up|Bottom-up]] are both techniques from dynamic programming. A problem solving strategy used in Mathematics and Computer Science. (CompSci 🤤🫦). 

Dynamic programming can be used when a problem has optimial substrucutre and overlapping subproblems. Optimal substructure means the optimal soloutions an be created from the optimal soloutions of its subproblems. In other words fib(5) can be solved by fib(4) and fib(3). Overlapping subproblems happen whenever a subproblem is solved multiple times which we saw when fib(5) made multiple calls to the typically recursive fib(3) and fib(4). 

Dynamic programming can be used for a range of problems and involves techniques besides the ones we learned here. If you are working on a problam with optimal substructure and overlapping suproblems, consider whether a dynamic programming implementation may work.
