# Towers of Hanoi.

## Introduction.
You are given three pegs and $n$ disks, and they are all sorted on one of the pegs. Goal: move all $n$ disks from start peg to goal peg. The disks being labeled from $1$ up to $n$.
Sounds easy? However we have two rules which makes it harder, especial for the monks (we we will get on to that later, don't ask why yet). 
Rules:
1. You can only move one disk at a time.
2. You can never have a disk lying on top of a smaller value disk. 
3. You can only move the top disks.


## Problemsolving.
First let's see how wer can solve this recursively. Base case $n==1$. When we have $n\gt1$ we have to use [[Rekurisve algoritmer.|recursion]]. You can move the top disk to any to any tower from any tower as long as it obides the rules.

When solving $n==3$ you need to expose the bottom disk, and to do that you had to move all the disks above it (2 and 1). By: moving disk 1  to peg 2 from peg 1. Move disk 2 from peg 1 to peg 3. Move disk 1 from peg 2 to peg 3. 

More to the point, you just solved a subproblem. Moving disks $1$ to $n-1$ from peg $1$ to $3$.

Now to finish up you need to recursively solve subproblem of moving disk $1$ through disk $n-1$ back to peg $2$. And you are done.

And you knew this was coming: is there something special you did when you moved disks $1$ through $3$? (Any special from-s and to-s?). You could have moved them to any peg. For example from peg 2 to peg 3.

* Recursively solve subproblem of moving disks 1 and 2 from peg 2 to peg 1.
* Now that disk 3 is exposed on peg 2, move it to peg 3.
* Recursively solve the subproble of moving disks 1 and 2 from peg 1 to peg 3. 

No matter how you slice it, you can move disks 1 through 3 from any peg to any peg. Moving disks seven times.
Notice that you move disks 3 times for each of the two times that you recursively solve the subproblem of moving disk 1 and 2 + one for moving disk 3.

How about $n==4$? Because you can recursiely solve the subproblem of moving disks 1 through 3 from any peg to another pe you can solve the problem for $n==3$. 
* Recursively solve the subproblem of moving disks 1 through 3 from peg 1 to peg 3, moving 7 times.
* Move disk 4 from peg 1 to peg 2.
* Recursively solve the subproble of moving disks 1 through 3 to peg 2 from peg 3. Moving 7 times.

This soloution moves disks 15 time (7+1+7=15).

At this point you might have picked up on two patters. First solve the towers of Hanoi recursively unless $n==1$. Because then just move disk 1. Otherwise when $n\ge2$ follow these steps.
* Recursively move disks 1 through $n-1$ from start peg to spare peg.
* Move fisk $n$ from start peg to goal peg.
* Recurisvely move disks 1 through $n-1$ from spare page to goal peg.


>[!INFO] Moving count formula.
>Solving a problem of hanoi for $n$ disks requires $2^n-1$ moves.

## Psuedocode.

## Proper code.


## THE MONKS.
As i said early on in the begin the monks are important as they are the founding fathers of this puzzle, wait is it spelled pussle or puzzle, I don't remember, whatever is more cool 🍸🎩. 

If they move 1 disk a second it would take them longer than the entire life of the sun to move them all. They would……… all die before finishing. If i recall correctly it would take them approxiamately $100$ times longer than the left timespan of the sun to finish…

