# Tangenter.

## Kva er tangenter.
Ein tangent er ein rett linje som treffer nøyaktig eit punkt på ein graf.
Tangenter består av den [[Momentan vekstfart]] $\times \space x$ og $+$ eit [[Polynom terminologi#Konstant-term ledd 0 grad monomer|konstant ledd]]. 

Den generelle strukturen til ein tangent
$ax+b$ , der $a =$ stigningstallet, $b =$  konstantleddet.


## Korleis finne tangenter.
## Finne tangenter med Geogebra.

Finn den $x$ verdiene til den deriverte som gjer at vi har samme stigningstall som tangenten vi får oppgitt.

Bruk $tangent(point, function)$ i geogebra, med disse $x$ verdia vi fekk oppgitt ovanfor, og 

Vi settjer saman stignignstallet og konstant leddet til formen vist over.

## Finne stigningstall til tangent.
Dette trenger vi berre den [[Derivanter#Korleis finne den deriverte funksjonen|deriverte funksjonen]]. Eller den originale funksjonen som vi kan finne den deriverte funksjonen ut i frå til å finne.
For å finne stigningstallet til ein tangent er det berre å settje $x$ verdien til punktet vi skal finne tangenten til inn i den deriverte funksjonen. Då er svaret vi får stigningstallet til tangenten.


## Finne konstant ledd.
### Eit punkts formel (One point slope formula.)
Dette krevjer stigningstallet til å kunne jobbe med som ein kan få i frå [[Derivanter#Derivasjons regelen 1|den deriverte]], i tillegg til allereie å vite eit punkt. 

$y-y_{1}=a(x-x_{1})$
$a = \textit{stigningstallet}$
$x_{1} = \textit{Punktet sin x kordinat}$
$y_{1} = \textit{Punktet sin y kordinat.}$

Sett inn både $a$ , $y_{1}$, og $x_{1}$. 

Viss vi ser at tangenten ikkje møter punktet kan vi settje inn $b$ som avsettjer den til å treffe punktet.

> [!INFO]
> Denne er best!
> 
### Andre metode som berre fungerer utan variabler.

Vi kan finne det konstante leddet på ein anna metode, men denne fungerer berre utan variabler, og er mykje mindre consistent i å få rett svar. 
Vi kan seie at konstantleddet er $f(x)-f'(x)$ .
Litt confusing, og jepp du leste rett $f(x)-f'(x)$, dette er fordi det då finner vi tallet vi må addere for å få den opp til grafen sin posisjon igjen. Dette er best å gjere når ein ikkje har eit punkt i frå før, eller viss ein ikkje har noko variabler som $x$ eller $y$ verdi.

Eksempel:
$f(x)=x^2$
$f'(x)=2x$
Tangenten til 1 er:
$f'(1)=2$
$f(1)-f'(1)=1-2 \rightarrow -1$
$\rightarrow \textit{tangenten er:  } 2x - 1$

Geogebra confirms this is correct!

