# Beskrive grafer.
Når vi skal bruke grafer i problemer, kanskje vi skal finne den shorteste pathen mellom to ulike person i eit sosialt nettverk. Eller kanskje vi vil berre representere dette nettverket. 

Her er ein måte å representere dette sosiale nettverket vi har drøftet oss på.
![](https://cdn.kastatic.org/ka-perseus-images/faa1c44e1ab848623096b85b9aa32626b8d8d040.png)
Her betyr ein linje at dei kjenner kvarandre. Viss det er ingen linje kjenner dei ikkje kvarandre. 

Dette sosiale netverket er ein graf. Navnene er det som blir kalt "vertices" av grafen. (Eintall: "vertex"). Kvar linje er det som er kjent som ein "edge", dei. tilkolber to ulike vertices. Vi noterer ein edge ved å lage eit par av $u$ og $v$ som er to ulike vertices i ein graf. I dette dømer fordi dei kjenner kvarandre går disse edgsene begge veger, dette betyr at grafen er "undirected" og dermed gjer at vi kan gå begge veger på denne edgen. Det er ikkje alltid slik: nokre grafer er "directed" som tyder til at e dger ikkje alltid går begge veger, men går berre ein veg, til dømes: bob veit at bill eksiterer, men bill har aldri hørt namnet bob.  I ein udirected graph  ein edge mellom to vertices er incident på dei to verticesene og vis sier at verticsene er conncted med ein edge som er adjcent eller neighbours. Mengden av edges incident på ein vertex er degree av ein vertex.

I vårt graf Audrey og Frank kjenner ikkje kvarandre. Viss Frank ville blitt introdusert til Audrey, måtte dei bli kjent gjennom nokre venner. Frank kjenner Emily som kjenner Bill som kjenner Audrey. Det er dermed ein path av tre edges mellom Frank og Audrey. Faktisk er det den mest direkte veien for Frank å møte Audrey, det er ingen path mellom dei med mindre enn tre edges. Vi kaller ein path mellom to vertices med den minste moglege edges ein shortest path.

![](https://cdn.kastatic.org/ka-perseus-images/d8992fc9232fa32547d362c79fc3319a3b1b6b95.png)


Når ein path som går fra ein viss vertex leder tilbake til seg sjølv så er det ein cycle. Dette sosiale nettverket inneholder mange cycles, ein av dei går frå Audrey til Bill til Emily til Jeff til Harry til Ilana og tilbake til Audrey. Det er mangen cycles her! Det er òg ein kortere cycle om inneholder Audrey.
![](https://cdn.kastatic.org/ka-perseus-images/2b4922a8372b82d83bfb5eb416f338fc38b57d96.png)

Nokre gonger plasserer vi numerisk verdier på edgesene. Til dømes i eit sosialnettverk, kan vi bruke numeriske verdier til å indikere kor godt to individer kjenner kvarandre. Eller vi kan bruke eit vegkart over byet og si at vegene sine distanser er dei numeriske verdiene på edgesene. Da er verticesene byene og edgesene vegene, og dei verdiene på edgesene er veglengden/distansen. Her er eit døme frå Amerika.

![](https://cdn.kastatic.org/ka-perseus-images/8aa21944eef2879cea9080a2ae2fbcb98cec0ddf.png)


Det generelle begrepet vi bruker for eit nummer som er på ein edge er kalt dens weight, og ein graf der edgsene har weights blir kalt ein weighted graf. Til dømes i eit vegkart, viss du vil finne den korteste ruten mellom to lokalisjoner, leter du egentelig for den  pathen med minimum edge weights  totalt mellom dei to ulike verticsene(lokalisjonene). Dette blir kalt [[Rekurisve algoritmer.|shortest path finding algoritmer og dette er ein rekurisv algoritme.]]  Disse edgsene som nemnt i starten går ikkje alltid begge vegene, av og til går dei berre ein veg. Når det berre går ein veg er det kalt ein directed graf, fordi edsgene går i ein retning, dei er nemleg directed.  

Grafer som garantert uansett kva har ingen cycles blir kalt ein directed acyclic graph eller kort DAG. Disse kan sjølvsagt vere weighted. Ein DAG kan aldri vere undirected da har vi mange mange mange cycles, uansett om vi bare hadde hatt 2 vertices hadde det vore ein cycle.

Med directed edges har vi litt anna begrepre. Vi sier at ein edge leave ein vertex og entere ein anna. Viss ein directed edge leave vertex $u$ og entere $v$ så noterer vi dette gjennom $(u,v)$ . Orderen av vertices i pair er ganske viktigt, fordi det noterer ka for ein directed retning den viser går i. 

## Graf størrelse.
Når vi jobber med grafer, er det hjelpfullt å kunne snakke om mengden vertices og edges. VI pleier å notere vertex mengden med notasjonen $V$, og edgsene med $E$. Når vi representerer ein graf eller kjører ein algoritme på ein rgaf, bruker vi ofte ulike størrelse av vertecies og edgeses i vår [[Asymptotic notation.]]. Til dømes viss vi snakker om ein kjøre tid som er linear med mengden vertices. Strengt sagt ville vi sagt at det er $\theta(|V|)$  , og vi bruker notasjonen $|.|$ til å notere størrelse av settet med vertices. Men det blir ganske tungvint. å bruke $|.|$ til kvar einaste gang vi skriver det i asymptotic notasjon, i asymptotic notasjon (og **berre** i asymptotic notasjon) skriver vi heller da utan å bruke $|.|$ vi sier dermed i staden for $\theta(|V|)$ over til $\theta(V)$. 