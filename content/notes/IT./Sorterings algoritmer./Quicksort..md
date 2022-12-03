# Quicksort.
[[Big theta]]

Likt som [[Mergesort]], bruker også quicksort [[Divide and Conquer.]] strukturen så den er også ein rekursiv algoritme. Men måten quicksort bruker divide and conquer er litt forskjellig i fra mergesort. I mergesort bruker divide steget så vidt noko i det heile, og alt det vanskelige skjer i combine steget. Quicksort derimot er det omvendte, all det vanskelige arbeidet skjer i divide steget. Honestly combine stegt i quicksort gjer avsolutt ingenting, no like seriously.

Quicksort har norke nøkkeldifferanser i frå mergeSort. Quicksort jobber in place. Og dens worst-case running time er like gale som [[Selection sort.]] og [[Insertion sort.]] $\theta(n^2)$. Men dens gjennomsnittlege-case running time er like god som mergeSort sin $\theta(n\times \log_2(n))$. 

Så kvifor tenker vi på quicksort når vi har eit like godt alternativ mergeSort? 
Dette er fordi den konstante faktoren som er gjømt i [[Big theta]] notasjonen for quicksort er ganske god.. I praktisk pleier quicksort å gjøre det betre enn mergeSort og den gjer det mykje betre enn selection sort og insertion sort.

Her kan vi sjå korleis quicksort bruker divide and conquer strukturen. Likt som med mergeSort tenk på ein subarray $array[p..r]$, der den originale subarrayen er $array[0..n-1]$. 
1. Divide ved å velge eit tilfeldig element i subarrayen $array[p..r]$. Kall dette elementet vår pivot point.
	1. Rearranger alle elementene i $array[p..r]$ slik at alle elementene i $array[p..r]$ er mindre eller lik pivotpointen til venstre for den, og alle som er høgere til høgre for den. Dette blir kalt for **partitioning**. På dette punktet er det ikkje viktig kva rekkefølge elementene til venstre av pivotpointet har til felles med kvarandre, eller likt til høgre for pivot pointet. Vi bryr oss berre om kvart element er på rett side av pivotpointet.
	2. Vi oftast pleier å velge vårt pivotpoint som det siste elementet i subarrayen.
2. Conquer, ved å rekursivt sortere subarrayen sin $array[p..q-1]$ (Alle elementer til venstre for pivotpointet, som må vere mindre eller lik pivotpointet) og $array[q+1..r]$ (Alle elementer til høgre for pivot pointet, som må vere større eller lik pivotpointet).
3. Kombiner ved å gjere ingenting, fordi vi har allereie sortert den i gjennom divide og conquer steget. Combine steget i quicksort combine ingenting!

Base-casen er når subararrayen er av størrelse mindre enn to elementer, akkurat som i mergeSort. I merge, ser du aldri ein subarray med 0 elementer, men det kan du gjere i quicksort dersom alle andre elementer er entens til venstre eller høgre for pivotpointet når det sortert.

Slik utvikler quicksort seg:
![](https://cdn.kastatic.org/ka-perseus-images/9876d4dc59e01a4742860ae1831c20f654ed7959.png)

Vi velger eit pivotpoint, vi rearrangerer, vi velger eit nytt pivot point, vi rearrangerer, repiter til vi har ein subarray av element størrelse lavere enn 2. Sorter denne, det er jo berre å sjekke kass av dei to som er størst og plassere riktig. 

## Linear-time partiotioning.
Det virkelige arbeidet av quicksort skjer i løpet av divider steget, som partione $array[p..r]$ rundt eit pivot point dratt i frå subarrayen. Likevel vi kan velge kva enn som helst element i subarrayen som pivot pointet, er det enklest å partione viss vi velger det høgste index elementet av subarray $array[p..r]$. 

Etter at vi har vårt pivot point kan vi partione subarrayen ved å gå gjennom den frå venstre til høgre og samenligne kvart element med pivoten, har har to indices $q$ og $j$ in i subarrayen som dividerer den opp i $4$ grupper. Vi kan bruke variabeln $q$ fordi indexen vil eventuellt vere på vårt pivot point. Vi kan bruke $j$ fordi det er ein teller variabel og variabelen blir kastet vekk når vi er ferdig.

* Alle elementer i $array[p..q-1]$ er gruppe "L", som består av elementer kjent til å vere mindre eller lik til pivoten.
* Alle elementer i subarrayen $array[q..j-1]$ er gruppe "G" som består av elementer kjent til å vere større enn pivoten.
* Elementer i subarray $array[j..r-1]$ er kjent som gruppe "U", og består av elementer som sitt forhold til pivtoen er ukjent, fordi dei har ikkje enda blitt compared.
* $array[r]$ er gruppe "P", pivot pointet.

Originalt er både $q$ og $j$ lik som $p$. Ved kvart steg, samanliknar vi $array[j]$, den mest venstre elementet i gruppe "U" med pivoten. Viss $array[j]$ er større enn pivoten så $j++$, slik at linjen som dividerer gruppe "G" og gruppe "U" går ein posisjon over til høgre.
![](https://cdn.kastatic.org/ka-perseus-images/557d3afb93f7ba9abb3a9e845113fcf9ce1e56d8.png)

Når vi kommer til pivoten så er gruppe "U" tom. Vi deretter swapper pivoten med den mest venstre elementet i gruppe "G": swap $array[r]$ med $array[q]$. Dette plasserer pivoten mellom gruppene "L" og "G" og gjer den rette tingen til og med viss gruppe "L" eller gruppe "G" er tom.

Denne "partition" funksjonen som implementerer denne ideen returner og index $q$ der den endte opp med å plassere pivoten, slik at $quicksort$ funksjonen, som blir kalt, veit kor partitionsene er.

Her er dei første stegene i partione subarray $[12,7,14,9,10,11]$ i $array[4..9]$

![](https://cdn.kastatic.org/ka-perseus-images/53692155715c9f26ec927cb2d40e70ce6c460e86.png)

Å partionene ein subarray med $n$ element vil ta $\theta(n)$ tid. Kvart element $array[j]$ er compared ein gang med pivoten. $array[j]$ kanskje eller kanskje ikke blir swapper med $array[q]$, og $q$ kanskje eller kanskje ikkje blir inkrementert, og $j$ blir alltid inkrementert. Den totale nummeret av linjer executer per element av subarrayen er konstant. Siden subarrayen har $n$ vil den totale partition tiden vere $\theta(n)$: linear-time partioning.


# Analyse av quicksort.
Satan fuck deg quicksort. 🤯.

Quicksort sin verse case sceneario og gjennomsnittleg scenario er forskjellig på grunn av metoden vi finner vårt pivot-point som lar oss redusere tidsbruken ganske mykje.
Viss vi er ganske uheldig og partition størrelse er jævlig ubalansert, i vertste tilfelle der den eine er $0$ og den andre $n-1$ , alle utanom pivotpointet, så vil det vere [[Rekurisve algoritmer.|rekurisve tilkallinger på størrelser av n-1 og 0.]]. Likt som i [[Mergesort]] er denne tidne det samme som $\theta(n)$ på ein array av størrelse $n$. I mergesort er det tiden for meging, men i quicksort er det **berre** tiden for partitioning.

## Verste-case sceneario running time.
Når quicksort alltid har den mest ubalanserte partitionene mogleg så er den originale tilkallingen $cn$ tid for ein konstant av $c$, og der er $n-1$ rekurisve tilkallinger, den første vil dermed vere $c(n-1)$ den neste $c(n-2)$ …… til det er $c(1)$. Slik vil denne subproblem grafen sjå ut.
![](https://cdn.kastatic.org/ka-perseus-images/7da2ac32779bef669a6f05decb62f219a9132158.png)

Når vi tar og adderer alle dei ulike running-timene vil det sjå slik ut:
$cn+c(n-1)+c(n-2)……+2c=c(n+(n-1)+(n-2)+(n-3)……)=c((n+1)(\frac{n}{2})-1)$.
Den siste linjen $1+2+3…………+n$ er ein aritmetikk serier, og som vi såg når vi analyserte [[Selection sort.]]  (Vi subtraherer 1 fordi for quicksort, starter summasjonen på 2, og ikkje 1). Vi har nokre lavere order termer og konstante koeffisienter, men når vi bruker [[Big theta]] notasjon så ignorer vi dem fordi dei er konstante verdier og lavere termer. I [[Big theta]] notasjon er quicksort sin verste kjøre tid $\theta(n^2)$.

## Beste-case sceneario running time.

Quicksort sin beste case skjer når partionene er så gjevnt som mogleg, der deirast sider er entens like eller med ein distanse av 1 i størrelse av kvarandre. Casen med ingen forskjell i forskjell skjer når subarrayen har eit oddetall nummer av elementer og pivoten er rett i midten etter partionering, og kvart partition har $\huge \frac{n-1}{2}$ elementer. Den andre casen, skjer viss subarrayen har eit partall nummer av elementer og pivoten den eine siden/partionen har $\huge \frac{n}{2}$ elementer, mens den andre har $\huge \frac{n}{2}-1$ elementer. I kvar av disse casene har partionen på det meste $\huge \frac{n}{2}$ elementer, og dens tre/graf av subproblemene sine størrelse ser meir ut som treet for subproblemer i [[Mergesort]], med dens partionerings tider liknande til merging tidene:
![](https://cdn.kastatic.org/ka-perseus-images/21cd0d70813845d67fbb11496458214f90ad7cb8.png)

Vi bruker [[Big theta]] notasjon og får det samme resultatet som for mergesort $\theta(n\times \log_2(n))$.

## Gjennomsnittleg-case scenario running-time.
For å vise at den gjennomsnittlege running timen er òg $\theta(n\times \log_2(n))$ krever det faktisk nokre ganske avansert matematikk så vi går ikkje der. Men vi kan forstå litt betre korleis denne algoritmen sin generelle kjøre tid er dersom vi ser på nokre ulike dømer.

Først la oss forestille oss at vi ikkje alltid får heilt perfekte balanserte partitionser, vi får til dømes på det verste ein split av $3$ til $1$. Det er betyr den eine siden får $\frac{3}{4}\times n$ elementer, og den andre $\frac{1}{4} \times n$ elementer. (Vi ignorer pivot pointet her for å holde matte ren, men den gjer at vi ikkje får egentelig ein perfekt 3 til 1 split). Da vil treet av subproblemer og partition tidene se slik ut:
![](https://cdn.kastatic.org/ka-perseus-images/130b2d2a1fe897253def054f4c3aa7bd94cb6cf2.png)


Venstre childen av ein node representerer eit subproblem av størrelse $\frac{1}{4}$ av forrige, og childen til høgre viser $\frac{3}{4}$ av forrige. Viss vi følger venstre sidene vil vi raskt minske ned til basecasen av $1$ fordi vi har mykje mindre elementer per iterasjon, mens derimot viss vi følger berre til høgre vil vi mykje saktere komme til basecasen av $1$. Som figuren viser etter $\log_4(n)$ leveler kjemer vi ned til størrelsen av $1$ viss vi følger til venstre. Det er enklest å forestille seg kvifor $\log_4(n)$  viss vi starter med $1$ og går opp med $4\times$ om gangen  til vi når $n$. Så i andre ord spør vi kva verdi av $x$ vi får $4^x=n$, og svaret er jo da sjølvsagt $\log_4(n)$. Derimot når vi går nedover til høgre kvar iterasjon vil svaret vere $\log_\frac{4}{3}(n)$ til vi kommer ned til basecasen av $1$. For å førestille seg kvifor akkurat $\log_\frac{4}{3}(n)$ er det lett å tenke at kvart barn er $\frac{3}{4}$ av den øvre noden sin størrelse, kvar øvre node er  dermed $\frac{4}{3}$ av barnets størrelse. Viss vi dermed starter med ein basecase av $1$ og multiplserer med $\frac{4}{3}$ til vi når $n$ så har vi multiplisert $\log_\frac{4}{3}(n)$ ganger. 

Den verste runningtimen av $\log_4(n)$ og $\log_\frac{4}{3}(n)$ er $\log_\frac{4}{3}(n)$ så vi fokuserer berre på er $\log_\frac{4}{3}(n)$.For kvart av dei første $\log_4(n)$ nivåene er det $n$ elementer (inkludert pivotpointer som i realiteten ikkje blir partionet.) og så den totale partition tiden er for kvar av disse nivåene berre $cn$ for ein konstant av $c$.  Og dei siste nivåene har mindre enn $n$ noder og så for kvar av disse levelene er det på det meste $cn$ runningtime. Til sammen er det $\log_\frac{4}{3}(n)$ eveler, og så den totale partition tiden er $O(n \times \log_\frac{4}{3}(n))$. 

Og det er eit matematisk bevis som nemner at $\log_a(n)=\frac{\log_b(n)}{\log_b(a)}$., som tyder at vi berre har ein konstant faktor mellom dei ulike tallene og vi kan egentelig berre bestemme kva enn som helst base vi ønsker å ha når vi noterer ned runningtimen. Så vi pleier å bruke $2$ for basen. Dermed er quicksort sin running time $O(\log_2(n))$, likevel vi faktisk har ein høgere konstant faktor som er høgere enn den beste case running timen.

Kor ofte vi burde forvente å see ein split som er $3$ til $1$ eller betre? Det kjemer heilt ann på korleis vi velger våre pivot-points. Viss vi forestiller oss at pivotpintenhar ein like stor sjanse for å lande på kva enn som helst index av ein $n$ elementer liste. Da må vi pivotpointen lande i midten av arrayen for å oppnå ein split som er $3$ til $1$ eller betre.
![](https://cdn.kastatic.org/ka-perseus-images/a77e296baf334b577328a5f15ab294a652ad6b96.png) 

Så viss pivot-pointen har ein like stor sjanse for å lande kor enn som helst i arrayen etter partitioning er det ein $50\%$ sjanse for at vi får på det verste ein split av $3$ til $1$.

Viss vi tar eit anna døme og ser på dømet der vi får ein alternerende split av $3$ til $1$ og den verste case scenario, og vi tenker på ein node i eit tre med $k$ elementer i dens subarray. Da vil treet sjå slik ut:
![](https://cdn.kastatic.org/ka-perseus-images/1f6a230039af38419453096c58bfd3ab5ac77b0f.png)

I staden for å sjå slik ut:
![](https://cdn.kastatic.org/ka-perseus-images/656ca0d8ab950299dcc2800e6b2a52cc7ea6ffd5.png)


Dermed viss vi får den verste case splitten halvparten av tiden og ein split som $3$ til $1$ halvparten av tiden vil runningtimen vere dobbel så stor av det å få ein runningtime av $3$ til $1$ kvar gang. Igjen så er dette berre ein konstant faktor som blir absorbert inn i [[Big O]] notasjonen, dermed er òg running timen i denne scenarioet $O(n\times \log_2(n))$.

