# Merge sort - sorterings algoritmen.
Merge sort er ein [[Rekurisve algoritmer.|rekursiv algortime]] basert på [[Divide and Conquer.]] teknikken, den sorterer ein array ganske enkelt. 

Ved å bruke divide and conquer til å sortere trenger vi først å vite korleis våre subproblemer vil se ut som. Det fulle problemet er å sortere ein heil array så la oss si at vår subproblem er å sortere ein subarray. La oss starte subarrayen med index $p$ og slutte på index $r$. La oss gi arreyn ein notasjonen $array[p..r]$ . (Berre psuedocode). Originalt problem sorter : $array[0..n-1]$. 

Merge sort teknikk:
1. Divide ved å finne nummeret "q" ut av posisjonen midt mellom $p$ og $r$. Gjer dette likt som binary search, adder $p$ og $r$, divider med $2$, rund ned til nærast integer.
2. Conquer med å rekursivt sortere kvar subarray i kvar av dei to subproblemene/subarrayene, skapt av den originale divide steget. Sorter $array[p..q]$ og $array[q+1..r]$. 
3. Combine ved å "merge" dei to ulike sortertere subarrayene tilbake til ein singel sortert array $array[p..r]$.

Base case er subarrayen har to eller mindre elementer. Når $p\le r$ siden arrayen med null elementer eller berre ein er allerie sortert. Så dividerer og konkurerer berre når $p\lt r$. Steget av å dividerer og konkurere skjer rekurisvt  - fleire ganger.


Vi tester ut eit eksempel:
Vi har ein $array[14, 7, 3, 12, 9, 11, 6, 2]$. 
I første iterasjon er det heile arrayen vi driver med $p=0,r=7$. Denne arrayen er meir enn to elementer så det er ikkje ein basecase.

1. I divide steget settjer vi $q=3$, $\lfloor \frac{7}{2}\rfloor = 3$.
2. I conquer steget sorterere vi arrayen mellom $array[0..3]$ og $array[4..7]$ . 
	1. $array[0..3]$ blir over til $[3,7,12,14]$ 
	2. $array[4..7]$ blir over til $[2,6,9,11]$.
3. I combine steget drar vi disse to sorterte arrayene sammen. Slik at resultatet blir til slutt.
	1. Slik at $array[0..7]$ blir til $2,3,6,7,9,11,12,14$.

Måten vi sorterer dei to subarrayene skjer på samme metode vi divide og conquere den. 
Så lenge dei ikkje er ein basecase.

Her er ein visualisering over korleis mergesort sortere denne arrayen.

![](https://cdn.kastatic.org/ka-perseus-images/ace963383bea8d154f6abd1322a06a73b56b4628.png)

Dei fleste stegene i mergesort er ganske lette, vi kan lett dividere, og ganske lett finne midpointet. Den vanskelege delen er å merge dei ulike subarrayene når det trengst.


## Merge to subarrays, aka linear time merging.
Den igjenstående delen av mergesort er å merge subarrayer. 
Å merge to subarrayer kan vi gjere i linear-time som tyder den har ein $\theta(n)$.

Det første vi gjer å kopiere dei ulike subarrayene inn i nye variabeler slik at vi kan tulle med subarrayene for å merge dei sammen.

Først: 
1. Alloker to midlertidige arrayer: laveHalve, høgeHalve.
2. Kopier $array[p..q]$ inn i laveHalve, og $array[q+1..r]$ inn i høgeHalve.
	1. I vårt tidligere eksempel tyder dette av laveHalve har ein verdi av $[3,7,12,14]$ og høgeHalve $[2,6,9,11]$.
3. Så merger vi dei!
	1. Vi itererer over antallet elementer som skal vere
	2. Vi tar den minste verdien av index $i$ på laveHalve og index $j$ på høgeHalve og settjer den minste inn i vår aktuelle nye array.




# Analyse av mergesort.

Me veit at merge funksjonen kjører i $\theta(n)$ når vi merger $n$ elementer, men kvifor er da mergeSort i $\theta(n\times \log_2(n))$. Vi kan starte ved å sjå på runningtimen til dei tre ulike stegene i [[Divide and Conquer.]]. Vi ser litt nærmere:
1. Divide - divider steget tar ein konstant tid, uansett kva størrelsen av subarrayen er. Etter alt så er det einaste divider steget gjer å komputere midpunkt verdien $q$ av indexene $p$ og $r$. I [[Big theta]] indikerer vi ein konstant tid av $\theta(1)$.
2. I conquer steget gjer vi ein rekursiv sorterting av to subbarrays av omtrent $\frac{n}{2}$ elementer. Det tar litt tid, men vi tar hensyn til den tiden når vi holder på med subproblemene.
3. Når vi merger eit totalt av $n$ elementer gjennom vår merge funksjon tar det $\theta(n)$

Når vi tenker på divider og kombiner stegene sammen, vil den $\theta(1)$ running-timen for divider steget vere ein lav order term i forhold til $\theta(n)$ av running-timen til kombiner steget. Så la oss tenke at divider og kombiner stegene sin running time kombinert er $\theta(n)$. Litt meir konkret tar dei ein total running-time av $c\times n$ for ein eller anna konstant verdi av $c$.

Viss vi halder det simpelt og sier at viss $n\lt1$ da er $n$ alltid eit partall, så det gjer at vi kan tenke at $\frac{n}{2}$ er òg ein integer. (Og partall). Tilfellet der $n$ er eit oddetall skifter ikkje [[Big theta|Big Theta]] av funksjonen. Så vi kan tenke at runnningtimen for mergeSort er summen av of 2 gange runningtimen av mergeSort på ein subarray av $\frac{n}{2}$ størrelse (for conquer seget), $+cn$. (for divide and combine stegene).

Nå må vi finne ut runningtimen av to rekursive tilkalling på $\frac{n}{2}$ elementer. kvar av disser rekursive tilkallingene tar dobbelt så lang tid av running timen av mergeSort på ein array av $\frac{n}{4}$ størrelse (vi halverer $\frac{n}{2}$ blir til $\frac{n}{4}$), plus $\frac{cn}{2}$ til å merge. VI dermed har to subproblemer av størrelse $\frac{n}{2}$ som begge tar $\frac{cn}{2}$ tid til å merge. Så vi kan sie at den totale tiden for å merge alle subproblemene hittil av størrelse $\frac{n}{2}$ er det same som $\frac{cn}{2}\times 2$. 

Vi kanteikne ut merging tidene i eit tre.
![](https://cdn.kastatic.org/ka-perseus-images/808e1b1b992aef56270b3fc2b9ecc1a68eba8988.png)


Informatikk vitskapsmenn teikner trer oppned frå korleis trer normalt vokser. Eit tre er ein graf utan nokon sykluser (sykluser er veger som starte og slutte på samme sted). Dei ulike delene av eit kaller vi for treets nodes. Root node-n er på toppen, her er root-noden merket med $n$ for arrayen sin originale størrelse. Under finner vi nodesene som har ein subarray størrelse av $\frac{n}{2}$.

kvart av subproblemene av størrelse $\frac{n}{2}$ rekursivt sorterer to subarrayer av størrelse $\frac{n}{4}$. Fordi vi har to subproblemer av størrelse $\frac{n}{2}$ så har vi fire subproblemer av størrelse $\frac{n}{4}$. 
Og merge tiden for kvar av disse subproblemene av størrelse $\frac{n}{4}$ er det samme som $\frac{cn}{4}$ og summert blir dei til saman $4\times \frac{cn}{4}=cn$. 

![](https://cdn.kastatic.org/ka-perseus-images/6a59f0e9973778cd9a157d8f92d5301dcf619417.png)

Vi fortsetter slik heilt til $n==1 || n==0$ . Etter hvert som subproblemene blir mindre blir nummeret av subproblmer dobblet kvar gang det går ein iterasjon nedover i rekursjonen. Dobblingen og halvering kanselerer seg ut og gjer at vi får ein total merging time kvar gang av $cn$. Til slutt kjemer vi til base casen, der $n==1$, og fordi vi om vi er komt til base casen eller ikkje gjennom $p\le r$ så tar dette litt tid. Kor mange subarrayer av størrelse 1 er det. Siden vi starter med ein array av størrelse $n$ så gjer det at vi ein mengde $n$ subproblemer med ein størrelse av subarray 1. SIden kvar basecase tar tid $\theta(1)$ så kan vi si at alle base casene tar til sammen $cn$ tid.
![](https://cdn.kastatic.org/ka-perseus-images/5fcbebf66560d8fc490de2a0d8a0e5b1d65c5c54.png)


Nå som vi veit kor lang tid merging tar for kvart subproblem. Den totale tiden for mergeSort til å kjøre er den totale mengden merging tider for alle levelene. Viss det er $l$ leveler i treet så er tiden $l\times cn$. Viss vi skal finne ut kva $l$ er så må vi så på korleis vi går nedover, kvar gang vi går nedover så halverer vi i størrelse, nett likt som vi gjer når vi har binary-search, derfor kan vi si at tiden er $l=log_2(n)+1$, akkurat som i binary search. Siden 1 er eit uviktig tall så kan vi ignorere denne når det kjemer til den endelige running tiden, i tillegg fordi $c$ er konstant så kan vi òg ignorere denne.
Dette gjer at vår running time dermed er $\theta(n\times \log_2(n))$.

Ein anna ting om mergeSort som er viktig å legge merke til, den tar å kopierer ein kopi of heile mens den blir sortert, med den eine delen i lowHalf og den eine delen i highhalf. Fordi den kopierer meir enn ein konstant nummer av elementer samtidig, så sier vi at mergeSort jobber ikkje "in place". derimot både [[Selection sort.]] og [[Insertion sort.]] jobbe in place, siden dei aldri lager ein kopi av ein størrelse som ikkje er konstant. Fordi nokre systemer er det ikkje stor mengde fri plass av memory så liker vi ofte å ta dette i hensyn og bruke heller in-place algoritmer når dette er scenearioet.

