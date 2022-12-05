# Skalering av funksjoner.
[[Forksyvning og refleksjon av funksjoner.]] [[Odd og even polynomer]] [[Polynom grafer]] [[Polynom terminologi]]

Ein skalering av ein funksjon tyder at vi har ein heilt lik funksjon men den har ein koeffisient eit sted som forandrer heile funksjonen, men den halder formen lik.  Vi har hovudsakeleg to ulike former for skalering, den eine skalerer berre aukingen og minsking-ratene i funksjonen, mens nokre skalerer heile grafen. 


## Grunnleggjene første skalerings metode - Vertikal skalering.
Vi settjer ein koeffisient forann heile funksjonen.
Viss vi skal skalerere heile funksjonen vil det se slik ut:
$f(x)=x^2+1$, $g(x)=\frac{1}{2}f(x)$
```desmos-graph
y=x^2+1
y=1/2(x^2+1)
```

Den blåe er den originale den har ein konstant faktor av 1 som tyder at ved $x=0$ er det ein verdi av $1$. Derimot har den grønne ein koeffisient foran heile uttrykket av $\frac{1}{2}$, dette tyder til at den først av alt auker halvparten så raskt, men og at konstantleddet blir halvert. 
Vi kan på denne måten tenke at vi skalerer funksjonen vertikalt, fordi vi òg forandrer på konstantleddet.

## Grunnleggjene andre skalerings metode - Horisontal skalering.
Vi settjer ein koeffisient forann variabel inputten.
Den andre metoden er meir simpel og forandrer berre på ein del av funksjonen og det er detn horisontale skaleringen. For å oppnå dette settjer vi berre ein koeffisent forann alle $x$ verdiene, dette skalerer bredden og derav posisjonen i funksjonen. På denne måten kan vi tenke at vi skalerer grafen horisontalt.
$f(x)=x^2+1$, $g(x)=f(\frac{1}{2}x)$
```desmos-graph
f(x)=x^2+1
g(x)=f(1/2x)
```
Som vi kan sjå har dei begge ein heilt lik konstantledd verdi av $1$ då begge er $1$ ved $x=0$, men vi kan sjå at den grønne (g(x)) auker halvparten så raskt enn den originale (f(x)).

Slik kan vi skalere ein funksjon på to ulike måter.


Her er nokre dømer:
$f(x)=x^2-2$, $g(x)=2\times f(x)$ , $h(x)=f(2\times x)$
```desmos-graph
left=-3;
right=3;
---
f(x)=x^2-2
g(x)=2*f(x)
h(x)=f(2*x)
```

Den originale er den blåe $f(x)=x^2-2$
Den skalerte som omformet heile grafen ikkje berre stigningen er den grønne $g(x)=2\times f(x)$
Den lilla er den som har ein koeffisient forann alle $x$ verdiene $h(x)=f(2\times x)$.
