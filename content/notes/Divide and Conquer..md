# Divide and conquer algoritmer.

Både [[Selection sort.]] og [[Insertion sort.]] har den verste kjøretiden av [[Big theta]] ($n^2$). Det finnes bedre sorterings algortimer. [[Mergesort]] kjører i $\theta(n\times\log(n))$, og [[Quicksort.]] kjører i $\theta(n\times\log(n))$ på det beste og som oftast, men kjører i verste tid $\theta(n^2)$. Begge er betre enn selection sort og insertion sort.


## Divide and conquer algoritme struktur.
Både quick og merge-sort bruker eit algoritme paradigme basert på [[Rekurisve algoritmer.|rekursjon]]. Denne paradigme "divide and conquer" bryter eit problem ned inn i mindre sub-problemer som liknar på den originale, den rekursivt løyser sub-problemene og så kombinerer svarene på subproblemene for å forme sluttsvaret. Kvart problem må vere mindre enn den originiale, og ha ein base case for subproblemet.

1. Divide, divider problemet inn i mindre sub-problemer. Subproblemene er mindre enn den originale.
2. Conquer, løys sub-problemene rekursivt. Viss dei er små nok kan ein ofte berre løyse dei direkte utan å gjere det rekurstivt, da er sjølve sub-problemene base-casen.
3. Combine, Kombiner svarene til sub-problemene til å finne den endelige løysingen. (Final soloution, lmao, sieg heil). 

Her er ein oversikt over strukturen til ein divide and conquer algortime.
![](https://cdn.kastatic.org/ka-perseus-images/98c02634ee7f970a6bfb0812cc1495bacb462282.png)

Viss vi løyser subproblemene rekursivt:
![](https://cdn.kastatic.org/ka-perseus-images/db9d172fc33b90e905c1213b8cce660c228bb99c.png)


>[!INFO] Sidenotat.
>Fordi divide and conquer gjer minst to rekursive calls kan vi seie at divide and conquer algoritmer er [[Multiple recursion with the serpinski gasket.|multiple recursion]].
