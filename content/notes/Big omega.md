# $\text{Big } \Omega$ / Big Omega notation.


Av og til vil vi si at ein algoritme har tar minimum ein mengde tid utan å si noko om maksimumen. For Big $\Omega$ viss vi har ein stor $n$ kan vi seie at ein algoritme vil ta minimum $K\times n$, for ein eller anna verdi av $K$. Vi sier at Big $\Omega$ er asymptotically lower bound fordi den bounde veksten av running timen frå botn når det er store verdier av $n$.
Visualisering:

![](https://cdn.kastatic.org/ka-perseus-images/c02e6916d15bacae7a936381af8c6e5a0068f4fd.png)

Akkurat som $\theta(f(n))$ tuder til at $O(f(n))$ er sant tydet det også til at $\Omega(f(n))$ er sann, så vi kan seie at det verste scenarioet for binary search er $\Omega(\log_2(n))$. 

>[!Note]
> Vi kan også seie at binary search har ein worst case running time av $\Omega(1)$, fordi vi veit at binary search tar i vertfal ein konstant fart. Det er heilt korrekt, men svært upresist!