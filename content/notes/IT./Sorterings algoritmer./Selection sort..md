# Selection sort.

Selection sort fungerer ved å ta å finne den laveste verdien sitte den på første plass så finne andt laveste verdi og sette den på andre plass… …… heilt til arrayen er heilt sortert. 

## Psuedocode.
1. Finn laveste verdi element, swap med første element.
2. Finn nest laveste verdi element, swap med andre element.
3. Finn tredje laveste verdi element, swap med tredje element.
4. …
5. …
6. Repiter til arrayen er sortert, arrayen er sortert når ein skal swappe med samme indexer.

Visualisering av selection sort:
![](https://upload.wikimedia.org/wikipedia/commons/0/0f/Insertion-sort-example-300px.gif?20110419160033)
### Finne den neste laveste verdien.
Ein av stegene i selection sort er. å finne den neste laveste verdi element og plassere den på rette plassen.
Til dømes i arrayen [13,14,18,4] er den laveste verdien 4 med index 3. I selection sort setter vi den på index 0. Det neste hadde vore å finne nest laveste å sette den på index 1

Å finne indexen til neste laveste verdien kan vere litt forvirrende, men det einaste vi trenger å gjere er å finne den laveste verdien i ein subarray som starter på den siste sorterte plasserte plass, altså index+1 $\rightarrow$ til slutten.
Til dømes etter bytte index 0 og 3 på listen over så trenger ein berre å finne laveste verdien mellom index 1 og slutten avlisten, og bytte den laveste verdien med index 1. Så repiter!

## Analyse av selection sort.
Selection sort loope over alle elementer i ein array. Selection sort kaller til indexAvMinimum funksjonen (den som vi forklarte ovenfor) og [[Sortering|swap metoden]]. Ein kan tru at kanskje time complexity er $2n$ i running time fordi to funksjoner blir kalt, men det er ganske feil. Dette er feil fordi funksjonene har kode sjølv. indexAvMinimum funksjonen har òg ein for loop basert på $n$, og evt. ein mindre versjon av $n$. I selection sort med ein array på 8 ganger og blir indexAvminimum tilkalt 8 ganger, mengden totalt tilkalte har ein verdi på $1+2+3+4+5+6+7+8=36$ tilkallinger. $36\ne2\times8$. 
$36$ iterations blir av innholdet til indexAvMinmum blir utført.

>[!Info] Sidenotat.
>For å finne antall tilkallinger av innholdet til indexAvMinimum barre $\Sigma_{x=0}^{n}(n)$, adder alle tall opp til $n$.  Evt adder dei manglende tallene som ikkje lager eit par. Formel av alle tall i mellom 1 og n er det samme som $(n+1)(\frac{n}{2})$.

# Asymptotic analysis av selection sort.


Vi trenger 3 deler til den totale running timen av selection sort.
1. Running timen av alle callsene til indexAvMinimum.
2. Running time for alle calls til swap.
3. Running time til rest av loopen i selection sort.

del 2 og 3 er lette. Det er $n$ tilkallinger til swap, og alle tar konstant tid dermed $\theta(n)$. Likt blir resten av selectionsort kallet $n$ ganger dermed $\theta(n)$. For del 1 har vi allereie gjort den vanskelege delen. Det viktigaste vi trenger å vite er at vi tillkaller indexAvMinimum $n$ ganger og indexAvMinimum går igjennom alle verdiene av $n$. Så den versten tiden vi får av berre tilkallingen av indexAvMinimum er dermed $\theta(n^2)$., fordi vi kaller indexAvMinimum $n$ ganger, og den går igjennom $n$ elementer ($n\times n= n^2$).Av swap og alle andre deler av selection sort så er den verste runningtimen $\theta(n^2)$ så selection sort sin running time er $\theta(n^2)$.

[[Big theta]]