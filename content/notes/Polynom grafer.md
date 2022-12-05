# Polynom Grafer.



## Korleis faktorer påvirke grafen.
[[Polynom terminologi#^33d3ba|Faktorene]] bestemmer alt om grafen. Dens [[Polynom terminologi#^74129e|nullpunkt]], dens [[Polynom grafer#^7164ea|end behaviour (slutt oppførsel)]] $\dots$ 

Faktorene bestemmer når grafen krysser $x$ aksen. Nullpunkt og faktorer er egentelig det samme, nullpunkt er berre $x$ sin verdi i ein faktor. I alle nullpunkt er $y$ verdien 0. 

Eksponentene til faktorene bestemmer om nullpunktet krysser $x$ aksen og skifter forteikn.
Ein faktor som har eit partall i eksponent verdi, vil aldri krysse $x$ aksen i nullpunktet til faktoren og skifte forteikn, den berre dylter borti. Derimot vil faktorer som har oddetall i eksponent alltid krysse $x$ aksen i faktorens nullpunkt og skifte forteikn. 

Faktorene bestemmer grafens [[Polynom grafer#^7164ea|end behaviour.]] Likt som eksponentene til faktorer bestemmer når og om dei krysser $x$ aksen, bestemmer også eksponentene korleis grafen oppfører seg når den når uendelig i $x$. [[Polynom grafer#^7164ea|Referer til dette.]]



## Positive og Negative Intervaller.
### Kva betyr dette?
Viss vi veit [[Polynom terminologi#^74129e|nullpunkta/faktorer]] til eit polynom kan vi vite for kva $x$ verdier grafen har sine positive forteikn, og for kva $x$ verdier grafen har sine negative forteikn. 
Simpelt sagt veit vi når grafen er positiv og når grafen er negativ. Dette kan hjelpe oss å visualisere grafen.


### Finne gjennom testing av eit tall (Forteiknsmultiplisering).
Viss vi tester eit tall mellom to ulike nullpunkt, kan vi finne ut kva for noko forteikn resten av grafen har, og når. Viss vi rekner ut forteiknet til eit polynom for $x =$ verdi, $x \ne \text{nullpunkt}$. Får vi entens eit positivt eller negativt tall tilbake. Vi kan gjere det lettere ved å berre sjå på kva forteikn kvar faktor får når vi settjer inn tallet, og dermed berre multiplisere dei forteikna til faktorene. Som nemnt tidligere, i mellom to nullpunkt vill alltid forteiknet vere likt, og viss eksponenten til ein faktor er oddetall veit vi at grafen skifter forteikn i det nullpunktet i $x$ aksen. Viss eksponent til ein faktor er partall vil ikkje det krysse $x$ aksen og skifte forteikn, då veit vi korleis den oppfører seg til alle $x$ verdier, berre ut i frå å teste ein $x$ verdi. 

[[Polynom grafer#^81de8a|Referer til eksempel bilete under.]]


### Finne gjennom forteiknslinje.

^e0d1fe

Vi kan også finne ut kva for nokre forteikn ein graf har for alle $x$ verdier gjennom ein forteiknslinje. 

Forteiknslinjer fungerer ved å settje faktorene på linjer paralell med ein linje av $x$.
Vi deretter krysser faktorlinjene, med faktorenes nullpunkter og teikner av dei positive forteikna og dei negative forteikne i linjene. [[Polynom terminologi#^74129e|Nullpunkt]] har eit symbol av 0. I mens [[Polynom terminologi#^11a079|Bryddpunkt]] har eit X som symbol. Til slutt for å sjå på heile polynomet sitt forteikn kan vi sette polynomet på ein eigen linje, for å finne forteikne her; multipliserer alle faktorene sine linjer for å finne denne linjens forteikn. Viss det er ein brøk kan vi gjere det samme der vi deler linjene på kvarandre for å finne brøkens forteiknslinje; skal vere heilt lik som å multiplisere.

Ein forteiknslinjer ser slik ut:
![](http://i.stack.imgur.com/gncg2.png)

Her i dette eksempelet er $x \ge 0$ (positiv) når $x \in \left\langle \leftarrow, -1 \right] \space \cup \space \left[   1, \rightarrow \right\rangle$ 

Eksempel (Positive og negative intervaller i eit polynom): ^81de8a

![](https://cdn.kastatic.org/googleusercontent/69tq0M6j5vJU_ERxil6tV4teGe8jREgSLoHQPn71ACqF41nIYTOs5W3LZsGlvAkszRJSmPEmagLLagHCc2AF3nOX)


## Asymptoter.

^f2d0d6

Ein asymptote er ganske enkelt forklart ein linje ein graf nærmer seg når $x$  beveger seg. Asymptoter kan gå i alle retninger, den kan gå skrått oppover, rett ned, skrått nedover, $\dots$ Asymptoter oppstår når ein [[Polynom divisjon|polynom blir delt og har eit konstantledd]]. Når ein deler oppstår det som regel to asymptoter, ein vertikal ein, og ein horisontal/skrå ein. Men asymptotene kan også vere heilt forskjellige retninger, som nemnt tidligere. Blant anna i Sigmoid funksjonen har vi to horisontale paralelle asymptoter. . Den horisontale asymptoten oppstår når $x$ går til uendelig og nærmer seg ein $y$ verdi. Den vertikale asymptoten oppstår når $x$ nærmer seg [[Polynom terminologi#^74129e|nullpunkt-et/ane]] i nevneren til brøken. Då går $y$ verdien til det uendelige, for å dividere på 0, gir oss eit udefinert svar, og ingen veit kva $y$ verdien skal vere når vi deler 0. ^8a35c9

#### Vi kan rekne ut den vertikale asymptoten: ^8b580b

Den vertikale asymptoten oppstår når nevneren i brøken sin verdi $=$ 0 og telleren er $\ne 0$. Då er det ganske openbart for korleis vi finner den vertikale asymptoten sin posisjon i $x$ aksen.
Det einaste vi trenger å gjere er å dra konstantleddet over $= 0$ slik at det blir $x = \text{konstantledd}$. Her ligger den vertikale asymptoten i denne $x$ verdien.

Eksempel:
$\large f(x)=\frac{(x+3)(x-2)}{x+10}$
Vertikale asymptote sin $x$ akse posisjon:
$x+10 \rightarrow x=-10$. 
Posisjon sin verdi $= -10$.

#### Vi kan rekne ut den horisontale/skråe asymptoten:

Den horisontale asymptote oppstår når $x$ verdien går i mot det uendelige. 
Vi kan rekne denne asymptoten sin $y$ verdi ved å ta i bruk limits, dette fungerer når det er fleire enn ein faktor i teller, og i nevner. I motsetnad til å berre dele den første termen i telleren med den første termen i nevneren fungerer dette med fleire faktorer. Vi bruker limits, og deler alle termene på $x$. Dermed tenker vi ut verdiene til alle termene som delest. Viss ein term er til dømes: $\frac{1}{x}$ blir dette 0 fordi $x$ går til det uendelige og denne verdien minsker. Viss det er $\frac{x}{x}$ blir dette 1, fordi alt dividert på seg sjølv $=$ 1.
Viss telleren har lavere grad funksjon enn nedre delen vil $y$ verdien alltid vere = 0. 

###### Eksempel med limits (Fungerer for fleire faktorer, og skråe):
$\large f(x)=\frac{x+2}{x+10}$
Horisontale sin $y$ akse posisjon:
$\large \lim_{x \to \pm \infty} \frac{x+2}{x+10}$

$\LARGE \lim_{x \to \pm \infty} \frac{\frac{x}{x}+\frac{2}{x}}{\frac{x}{x}+\frac{10}{x}}$
$\large \frac{1+0}{1+0} \rightarrow \frac{1}{1} \rightarrow 1$
Posisjon sin verdi $= 1$.

>[!INFO] Når det er ein polynom og ein skrå asymptote, bcuz høgere oppe enn nede $\rightarrow$ vi kan få feil!
>Betyr dette at vi **må** gjer [[Polynom divisjon]] for å finne den skråe asymptoten. Deretter sjekke om nokon [[Polynom terminologi#Term (ledd).|termer]] går i mot $0$ med [[Grenseverdier]].


##### Eksempel med simpel deling (NB! Fungerer berre når det er berre binomiale polynomer og berre for horisontale asymptoter, ikkje skråe):
$\large f(x)=\frac{x+2}{x+10}$
Horisontale asymptote sin $y$ akse posisjon:
$\large \frac{x}{x} \rightarrow 1$
Posisjon sin verdi $= 1$.
	

![400](https://useruploads.socratic.org/f6yJd4BfStuKbYWfKO21_assymptote.bmp)

## End behaviour (Slutt oppførsel).

^7164ea

End behaviour eller slutt oppførsel er korleis enn graf sine ender oppfører seg når vi går i mot det uendelige i $\pm \space x$ verdi. For å finne slutt oppførselen trenger vi berre å sjå på det [[Polynom terminologi|ledende termet]] og dens eksponenter, og forteikn. Grunnen til at vi berre trenger å se på dette termet og dens eksponenter er fordi eksponenten kommer til å eventuellt bli så sterk at den overtar alle andre termer sin *styrke*.

Polynomer som har ein ledende term med  $x$ som er opphøgd i eit oddetall vil ende opp i det uendelige + der $x$ auker for evig, og inn i det uendelige - der $x$ går i negativ for evig.

Omvendt er polynomer som har ein ledende term med $x$ er opphøgd i eit partall. Disse vil ende opp i det uendelige + uansett $x$ retning. 

Men! Viss ein polynom sin ledende term har ein [[Polynom terminologi|koeffisient]] som er negativ vil grafen vere omvendt frå det normalet. Der oddetall eksponenter (i $x$ ledende term) minsker der $x$ verdi går positivt for evig, og auker der $x$ går for evig inn i det negative. Likt er det når det er partall i eksponenten til det ledende termet sin $x$. Her i staden for det normalet, går den inn i det uendelig negativ der $x$ går i mot $\pm$ uendelig.

Vi veit ikkje korleis dei nærmest delen til 0 i ein polynom oppfører seg (grunna nullpunkta) men vi veit korleis den oppfører seg når den nærmer seg uendelig.

Eksempel på end behaviour (Trur polynomet er $f(x)=(x-2)(x+1)(x+4) \rightarrow f(x)=x^3+3x^2-6x-8$, positivt forteikn i ledende term koeffisient og oddetall eksponent!):

![](https://www.calculushowto.com/wp-content/uploads/2018/11/end-behavior-1-1.png)

