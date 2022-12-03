# Representere grafer.
Det er mange ulike måter å representere [[Beskrive grafer.|grafer]] på, kvar som har sine fordeler og kvar som har sine ulemper. Nokre situasjoner er det ein måte å representere ein graf på som passer meir til situasjonen. Dei ulike metodene for å representere grafer har sine eigne memory gjennomsnittleg bruk og ulike struktur i koden.

Ein representasjon av ein graf pleier å følge tre ulike kriterier. 
Ein kor mykje memory vi trenger for representasjonen. Og vi kan faktisk bruke [[Asymptotic notation.]] for dette! Jepp asymptotic notation kan brukest til å vise meir enn berre runningtimen. Det er virkelig berre ein måte å vise ein karakterisk med ein funksjon. Dei to andre er 1. Tiden det tar for å finne ut om ein edge er i grafen i det heile. Og den 2. andre er kor lang tid det tar å finne neighborsene av ein vertex.

Det er normalt å identifisere vertices ikkje med eit namn eller ein anna verdi, men heller ved å bruke nummere. Altså numeriske verdier. Der settet av vertices ($|V|$) går i frå $0$ til. $|V|-1$. Her er eit døme på ein graf.

![](https://cdn.kastatic.org/ka-perseus-images/21cd2731928c7c13057eee000e3697de82ccc058.png)

## Edge lister.
Ein simpel måte å representere ein graf er ved berre bruke ein liste av $|E|$ edges, dette kaller vi ein edge list. Å representere ein edge har vi berre ein liste av to vertex nummere, eller ein liste av objekter som inneholder vertex nummerene av verticene som edgsene er tilkoblet. Viss edgesene har weights, så smakker vi berre eit ekstra element til listensom inneholder vekten til edgen. Siden kvar edge har berre to eller tre nummere, blir den totale spacen for ein edge list berre $\theta(E)$. Til dømes kan vi representere ein edge liste i $JavaScript$ for ein graf slik:
```JavaScript
[ [0,1], [0,6], [0,8], [1,4], [1,6], [1,9], [2,4], [2,6], [3,4], [3,5],
[3,8], [4,5], [4,9], [7,8], [7,9] ]
```

Edge lister er simple, men viss vi vil finne om ein graf inneholder ein spesifikk edge så må vi searche gjennom heile edge listen. Viss edgesene i listen blir fremstilt i ingen spesiell rekkefølge så er det berre ein linear search gjennom $|E|$ edges. Det er teoretisk mogleg å organisere dei slik at tar $O(\log E)$, men det er litt vanskelig!

## Adjacency matrister.
For ein graf med $|V|$ vertices er ein adjecency matrise ein $|V|\times |V|$ matrise of $0$ er og $1$ ere. Der ein entry i row $i$ og column $j$ er $1$ dersom og berre dersom edge $(i,j)$ er i grafen. Viss du vil indikere ein edge vekt plasser den i row $i$ og column $j$., og ha ein reserve spesiell verdi som til dømes $null$ for å indikere ein manglende edge. Her er ein adjacency matrise:
![](https://cdn.kastatic.org/ka-perseus-images/549bca1a52774846b25caff86d244d03ee63fd38.png)
Og i javascript
```JavaScript

[ [0, 1, 0, 0, 0, 0, 1, 0, 1, 0],
  [1, 0, 0, 0, 1, 0, 1, 0, 0, 1],
  [0, 0, 0, 0, 1, 0, 1, 0, 0, 0],
  [0, 0, 0, 0, 1, 1, 0, 0, 1, 0],
  [0, 1, 1, 1, 0, 1, 0, 0, 0, 1],
  [0, 0, 0, 1, 1, 0, 0, 0, 0, 0],
  [1, 1, 1, 0, 0, 0, 0, 0, 0, 0],
  [0, 0, 0, 0, 0, 0, 0, 0, 1, 1],
  [1, 0, 0, 1, 0, 0, 0, 1, 0, 0],
  [0, 1, 0, 0, 1, 0, 0, 1, 0, 0] ]

```

Med ein adjacency matrise, kan vi finne ut om ein edge er til staden i konstant tid, berre ved å searche opp den correspondende entry-en i matrisen. Til dømes dersom vi har ein adjacency matrise kalt "graf" kan vi finne ut som om edge ($i,j$) er i grafen ved å searcha opp $graf[i][j]$. 

Det er nokre ulemper med adjacency matrise. Den første er at den tar $\theta(V^2)$ memory, til og med viss grafen har svært få edges. Dette er fordi dei allerfleste verdiene i matrisen vil ha ein verdi av $0$, og vi bruker ganske mykje memory for disse ekstra $0$ene som bidrar ingen viktig shit. tbh 🤮 shrek dick sucking 🐿. Ahrem for det andre viss du vil fine ut kva for nokre vertices som er adjcent til den gitte vertex $i$ så må du sjekke alle $|v|$ innføringer i rad $i$ til òg med viss det er ganske få vertcies som er adjcent til vertex $i$.

For ein undirected graf er adjcency matrisen symmetrisk, rad $i$ og kolonne $j$ innføring er $1$ dersom og berre dersom rad $j$ og kollone $i$ er $1$. For ein directed graf trenger ikkje adjacency matrisen å vere symmetrisk.

## Adjaceny lister 🥰🥰🥰🥰🥰 😈🫦.
Å representere ein graf med ein adjaceny liste kombinerer adjacency matriser med edge lister. For kvar vertex $i$, lagre ein liste av verties tilbkoblet til den. Vi har normalt ein liste av $|V|$ adjcency lister, kvar adjcency list per vertex. Litt confusing, men simpelt sagt ein liste over alle vertices i ein graf, og kvart element i denne listen inneholder ein liste av alle vertices denne noden er koblet til.
Her er ei visualsiering:
![](https://cdn.kastatic.org/ka-perseus-images/cc82379521bd84738e86d6cf9552738ca9138420.png)

Slik kan ein slik liste sjå ut i javascript.
```javascript

[ [1, 6, 8],
  [0, 4, 6, 9],
  [4, 6],
  [4, 5, 8],
  [1, 2, 3, 5, 9],
  [3, 4],
  [0, 1, 2],
  [8, 9],
  [0, 3, 7],
  [1, 4, 7] ]

```

Adjacency lister er ikkje nødvendig at skal visest i noko spesiell rekkefølge men det ofte lurt å liste dei i økende størrelse som i døme over.

Vi kan finne kvar vertex sin adjacency liste i konstant tid fordi vi trenger berre å index inn i ein liste. For å finne ut om ein dege($i,j$) er i listen trenger vi berre å gå til $i$ sin adjacency liste og så søke for $j$ i $i's$ liste. Dette vil ha den verste case runningtimen av å finne ein edge ved $\theta(d)$, der $d$ er mengden vertices tilkoblet til vertex $i$. Denne mengden kan på det verste vere så høg som $|V|-1$, viss alle er tilkbolet til $i$ altså. eller så lavt som $0$ dersom $i$ er ikkje tilkoblet nokon vertices. I ein undirected graf er vertex $j$ i vertex $i$ sin adjacency list berre viss i $i$ er òg i $j$ sin adjacency liste. Basically begge vertecisene må vite at dei er tilkoblet til kvarandre. Dersom dei ikkje er tilkoblet på begge, kan den vere directed. Viss ein graf er weighted så inneholder kvar adjacency liste to verdier for kvart vertex, ein for kva for noko vertex den er tilkoblet og weighten mellom dei.

Du kan bruke for loops til å finne alle vertices ein vertex er tilkoblet slik:
```JavaScript
var i = 5; //Tallet viser kva for ein vertex i grafen det er prat om.
for(var j = 0; j < graph[i].length;j++){//Gå til alle vertices til vertex i
	gjerNoko(graf[i][j]); //gjerNoko med kvar vertex tilkoblet vertex i.
}
```

Kor mykje plass ein adjacency liste tar, varierer litt om først den er undirected eller directed. Og om kvar vertex inneholder ein anna vertex. Nokon inneholder jo nesten alle, og nokre inneholder nesten ingen.
I ein adjacency liste for ein undirected graf inneholder den $2|E|$ elementer, fordi den inneholder 2 edges per vertex som er koblet til i listen. Og viss den er directed så er det $|E|$. Eit element per directed edge.

