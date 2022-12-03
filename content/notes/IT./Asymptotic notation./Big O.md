# Big O notation.

[[Big theta]] brukes når ein vil bounde running timen mellom to uike konstanter, men av og til vil vi berre ha den bounden mellom ein $konstant\times n$ og $0$.
Til dømes er det feil å si at binary search har ein running time av $\theta(\log_2(n))$ fordi i beste tilfelle er det $\theta(1)$. Da passer Big O notation aller best. 
For store verdier av $n$ er Big O på det meste $K\times n$ for ein eller anna verdi av $K$.

Big O er  asymptotically upper bound som betyr at  for store verdier av $n$ er alltid runnning timen under $K\times n$. 
Dette kan vi da bruke til å seie at running timen til binary search er det samme som $O(\log_2(n))$.  I tillegg kan vi seie at alle algoritmer som har ein running time i Big $\theta$ har den samme running timen i Big O. Men dette funker ikkje omvendt!

Visuelt bilete:

![](https://cdn.kastatic.org/ka-perseus-images/501211c02f4c6765f60f23842450e1151cfd9c89.png)


Binary search kjører alltid i $O(\log_2(n))$, men ikkje alltid i $\theta(\log_2(n))$.

>[!Mistolkinger!]
>Ofte så mistolker ein at Big O er det alltid nærme den aktuelle verste sceneario av ein algoritme. Men dette er feil!
>Vi kan til dømes si at binary search òg kjører i $O(n)$ fordi vi veit at binary search kjører alltid  lavere enn denne verdien,  men denne verdien er ikkje nærme den worst case scenario-et som er faktisk på $O(\log_2(n))$.  Likevel er begge like gyldig å si!

