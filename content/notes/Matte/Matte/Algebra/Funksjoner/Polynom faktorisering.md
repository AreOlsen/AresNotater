# Polynom Faktorisering.

## Kva er polynom faktorisering?

Polynom faktorisering er prosessen av å omskrive polynomer i full form, til dømes: $f(x) = x^2+4x+4$, over til ein lettere form, $f(x)=(x+2)(x+2)$. Denne formen viser [[Polynom terminologi#^74129e|nullpunkta]] til polynomet i dens [[Polynom terminologi#^33d3ba|faktorer]].

## Kvadratsetningene & Konjugatsetningen (Spesielle produkter).

^3e6fd1

Vi har nokre grunnleggende setninger vi kan ta i bruk for å finne dei ulike faktorene i nokre polynom, her er alle A variablene like, alle B variablene like:

1. Første kvadratsetningen $(a+b)^2 = (a+b)(a+b) \rightarrow \underline{a^2+2ab+b^2}, \space A= \sqrt{Første \space term}, \space B= \sqrt{Siste \space term}$

2. Andre kvadratsetning
   $(a-b)^2 = (a-b)(a-b) \rightarrow \underline{a^2-2ab+b^2}, \space A = \sqrt{Første \space term}, \space B= \sqrt{Siste \space term}$

3. Tredje kvadratsetning (Også kalt konjugatsetningen)
   $(a+b)(a-b) = \underline{a^2-b^2}, \space A=\sqrt{Første \space term}, \space B= \sqrt{Siste \space term}$

Vi simpelt finner tallene etter vi igjenkjenner oppsettet i ein polynom og bruker oppsetta/templates for å faktorisere. Husk å sett dei rette forteikna når du bruker oppsetta.
**Når vi finner A og B verdi, ikkje ta med negative forteikn!!!!!**

## Grupperingsmetode.

^64d1ac

Grupperingsmetoden er ein metode for å faktorisere som går på å dele polynomet inn i grupper. Gruppene skal ha lik forhold på kvar side, når gruppene faktoriserest har vi ein felles faktor. Etter på drar vi felles faktoren ut for seg selv. I eit [[Polynom terminologi#^09104c|trinomium]] må vi dele den inn i 4 termer ved å dele midterst term viss vi ikkje allereie har fire termer, og dermed utføre metoden. Metoden kan i teorien bli brukt for alle [[Polynom terminologi#^5d0d05|grader]] av polynomer, men er lettest når polynomet er ein andregrad.

Til dømes:
$f(x)=x^2+x-6$, blir til:
$f(x)=x^2-2x+3x-6$, blir til:
$f(x)=x(x-2)+3(x-2)$, blir til:
$f(x)=(x+3)(x-2)$

Denne metoden fungerer òg med tredjegrader:
$f(x)=x^3+2x^2-4x-8$
$f(x)=(x^3+2x^2)-(4x+8)$
$f(x)=x^2(x+2)-4(x+2)$
$f(x)=(x^2-4)(x+2)$
$f(x)=(x+2)(x-2)(x+2)$
$f(x)=(x+2)^2(x-2)$

Oftast trenger vi berre å gjere som vist over ved å dele det inn i to grupper ein på høgre, og ein på venstre. Og så utføre metoden.
Vi må berre alltid ha minimum to grupper vi kan arbeide med, dermed må vi ofte dele det midterste termet slik at vi har to grupper som har heilt likt forhald. **Forhaldet må vere likt i begge gruppene.**

## Sum Produkt - metode.

Sum Produkt metoden er ein veldig lett metode for å kunne faktorisere andre grad trinomialer, metoden går på å se på det midterste [[Polynom terminologi#^8de091|termet]], og det siste termet. Vi må finne to tall som når addert sammen blir det midterste termet sin koeffisient, og multiplisert sammen blir det siste termet sin koeffisient. Dette er faktorene til tallet når vi setter x foran tallene i ein faktor. Veldig raskt metode, men krever at ein tenker ut tallene, som kan av og ti gi feil.

$(ax^2+bx+c)$,
$b=tall_1+tall_2$,
$c=tall_1\times tall_2.$

Til dømes:
$f(x)=x^2+6x-7$,
$6 = 7-1$,
$-7=7 \times -1$,
$f(x)=(x+7)(x-1)$

## ABC Formel (Kvadratiske formel).

ABC Formelen, i motsetnad til alle andre formelene kan enkelt finne faktorer med desimaltall i nullpunkt. Problemet med denne formelen er at denne berre fungerer for andregrads [[Polynom terminologi#^09104c|trinomialer]], og slurvefeil kan lett oppstå når vi bruker den. Formelen gir oss faktorene sine nullpunkt, eller i andre ord verdien til X per faktor. Vi må etter å ta i bruk formelen skifte forteikn til talla og sette inn i ein paratens for å få ein faktorisert faktor, slik $x=-1, \space x-1=0, \space (x-1)$. Formeler, som kubiske formelen, kan finne polynomer med høgare grader. Det tragiske med ABC Formelen er at den er veldig tungvint å bruke, men gir oss eit svar når vi ikkje klarer å bruke nokon av dei andre metodene. Ikkje alltid gir oss dette eit reellt svar då får vi [[Komplekse tall|komplekse tall]] som svar.

ABC Formelen (Kvadratiske formelen):

$\large \begin{array}{*{20}c} {x_1,_2 = \frac{ - b \pm \sqrt{b^2 - 4ac} }{2a}} & {{\rm{når}}} & {ax^2 + bx + c = 0} \\ \end{array}$

_A = Koeffisient i første term_
_B = Koeffisient i andre term_
_C = Koeffisient i tredje term_

Til dømes:
$f(x)=x^2+x-6$,
$A = 1$
$B = 1$
$C = -6$
$\large x_1,_2=\frac{-1 \pm \sqrt{1^2 - (4 \times 1 \times -6)}}{2 \times 1}$

$\large x_1,_2=\frac{-1 \pm \sqrt{1^2 - (-24)}}{2 \times 1}$

$\large x_1,_2=\frac{-1 \pm \sqrt{1 +24}}{2}$

$\large x_1,_2=\frac{-1 \pm 5}{2}$
$x_1=-3, \space x_2=2$
$(x+3), \space(x-2)$
$f(x)=(x+3)(x-2)$

Veldig tedious!

## Faktorisering med Polynom divisjon (Algebraisk lang divisjon).

Ved å ta i bruk [[Polynom divisjon#^4aa794 | Algebraisk lang divisjon]] kan vi finne faktorer, vi trenger ein kjent faktor i fra før. Vi dermed dividerer ut polynomet med faktoren og viss vi har ingen remainder, veit vi at polynomet kan fullt faktoriserest. Vi setter det utdividerte ved siden av den kjente faktoren. Vi kan berre finne graden lavere enn polynomet med denne metoden, vi kan fortsette og bruke andre metoder som grupperingsmetoden for å fullt faktorisere den. Vi kan også faktorisere med ein remainder, men då blir det eit brøk med den kjente faktoren nederst, og remainderen på toppen.

Til dømes:
$f(x)=x^2+2x-3$
$\text{Kjent faktor : } (x+3)$
$(x^2+2x-3)/(x+3) = (x-1) \space \text{Ta i bruk algebraisk lang divisjon her.}$
$\large (x+3)(x-1) \text{ fullt faktorisert.}$

Døme med remainder:
$f(x)=7x^2+35x+24$
$\text{Faktor : } (x+4)$
$(7x^2+35x+24)/(x+4) = 7x+7, \space \text{med remainder av -4.} \text{ Ta i bruk algebraisk lang divisjon her.}$
$\large (x+4)(7x+7 - \frac{4}{x+4})\text{ faktorisert.}$

P.S Viss dette er ein løsning på ein matteoppgåve i ein prøve er det oftest feil, fordi i VG1 har dei sjeldant slike oppgåver, oftast er dei full faktoriserbare.

## Sjekke om eit tall er ein faktor (Bruke remainder theorem).

For å sjekke om eit tall er ein faktor kan vi ta i bruk [[Polynom divisjon#^dd314c|Polynomial Remainder Theorem]]. Viss $x$ verdien vi tester blir 0 etter vi brukte "theoremet" veit vi at tallet er eit nullpunkt i polynomet. Vi skifter på forteikn med $x$ og tallet testet og får ein faktor, slik $P(-1)=0, x = -1, x + 1 = 0, (x+1) \text{ er ein faktor}$. Vi kan då ta i bruk Algebraisk lang divisjon for å faktorisere om vi ønsker.

## Største felles faktor (Greatest Common Factor, GCF).

Største felles faktor i polynomer er simpelt sagt, den største faktoren vi finner i alle termene.
Vi finner den største felles faktoren ved å primtall faktorisere termene, og dermed finne alle faktorene som er til felles. Deretter multiplisere dei felles faktorene, og få den største felles faktoren.
Oftest er x verdien i den største felles faktoren i ein polynom berre den laveste x verdien (inkl. eksponent), P.S husk at [[Polynom terminologi#^f0c201|konstandledd]], også kjent som 0 grad [[Polynom terminologi#^940144|monomer]], innehalder også $x$ verdier men dei er $x^0$ altså $1$. Då er den laveste $x$ verdien basically ingenting (1), og da er det ingen x verdi i det heile tatt i den største felles faktor. Vi kan bruke største felles faktor i faktorisering, blant anna ved [[Polynom faktorisering#^64d1ac|Grupperingsmetoden]] når vi skal faktorisere ut talla.
