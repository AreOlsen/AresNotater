# Transformering av funksjoner.
## Forskyvning
### Forskyvning høgre og ventre.

Når vi driver med ein forskyvning av ein funksjon kan vi ganske lett gjere dette. Det ein må huske er at når vi forskyver så er det egenteleg berre ein forandring av $x$ verdiene i [[Polynom terminologi#Term ledd|termene]]. Dette i andre ord tyder at det einaste vi trenger for å forskyve ein graf høgre eller venstere er å settje ein konstant ledd inn i $x$ verdien ved siden av slik:
$x^2$
vi flytter den 5 til venstre.
$(x+5)^2=x^2+10x+25$
Denne funksjonen til høgre er nøyaktig det samme som $x^2$ berre forskyvet 5 til venstre.
Husk at når vi adderer 5 så går den til vesntre fordi $-5+5=0$ og vi får samme startpunkts som når vi bruker $x^2=0^2$. Vi har berre forflyttet den.

### Forskyving opp og ned.

Det einaste vi trenger å gjere viss vi skal forskyve ein graf opp eller nedover er å introdusere eit ekstra konstant ledd på slutten av heile funksjonen til dømes:
$x^2$, vi vil hade den fem oppover.
$x^2+5$. Den er forskyvet fem oppover.



### Kombinering av høgre og venstre & opp og ned.

Det generelle oppsettet til ein forskyvning kan bli forklart slik
$f(x+a)+b$, for ein alla anna funksjon av $f$ der $a$ er ein forskyvning i $x$, og $b$ er ein forskyvning i $y$ akse.

Viss vi ser på eit døme kan kanksje betre forstå kompleksiteten.
$x^2$, vi forskyver 5 til høgre og 5 oppover.
$(x-5)^2+5$. Her er $f(x)=x^2$
Funksjonen ser slik ut til slutt:

$x^2-10x+30$. Vi har forskyvet $x^2$ her, men den ser ganske ulik ut!


```desmos-graph
top=20;
---
y=x^2
y=x^2-10x+30
```

Den blåe er $x^2$ og den grønne er $(x-5)^2+5$.



## Reflektere ein graf.
### Reflekte under og over $x$ aksen.
Viss vi flippe ein graf rundt dei ulike aksene kan vi bruke litt sunn fornuft for å gjere dette. 
Viss vi har ein funksjon til dømes $f(x)=x^2$, denne vil alltid gi positive svar. Viss vi derimot vil ha ein graf som er heilt likt som denne men vi vil ha negative svar då multipliserer vi berre heile $f(x)$ med $(-1)$ slik :
$(-1)f(x)=-1(x^2)$
Dette vil gjere at grafen blir reflektert under $x$ aksen.

```desmos-graph
y=x^2
y=-1(x^2)
```

Denne grønne er $-1(x^2)$, og den blåe er $x^2$.


>[!INFO] Sidenotat.
>Noko som grenser mot ulovlig matematikk og det er litt diskusjon om det faktisk er lovleg eller ikkje er det ved å settje $\pm$ som eit forteikn dette gjer at vi får både det negative svaret og det positive som gjer at vi har ein funksjon som har ein graf som er reflektert på begge sidene av $x$ aksen. Dei aller fleste grafkalkulatorene aka. program som Geogebra vil gi svar at dette ikkje går, men det er nokre som tillater.

### Reflekere rundt $y$ aksen.
Viss vi ønsker å rotere rundt $y$ aksen så er det ein ting vi kan gjere for å reflektere den. Og det er å settje ein $-1$ foran alle $x$ verdiene slik at når $x$ er negativ vil den faktisk vere positiv. Dette gjer at funksjonen blir reflektert. Vi kan dermed reflektere $f(x)=\sqrt(x)$ ved å bruke funkjsonen $g(x)=f(-x)\rightarrow \sqrt -x$. Som vi veit er berre $\sqrt x$ definert for positive verdier av $x$ så når $x$ er negativ og den har eit negativ forteikn, $(-)(-)=(+)$ vi får vår graf reflektert.

Når vi settjer dette inn i ein graf ser den slik ut:
```desmos-graph
left=-20;
---
y=\sqrt{-x}
y=\sqrt{x}
```
 
Blå er den reflekterte.
Grønn er den originale.

