# Invers funksjoner.
Vi kan tenke på ein funksjon som noko som tranformerer eit tall frå eit domene over til eit anna, til dømes $x$ blir til $y$. Ein invers funksjon derimot gjer det motsatte som den normale funksjonen, den går i frå det andre domenet til det første domenet. Til dømes $y$ over til $x$. 
Nokre kjente inverse funksjoner er $sin^{-1}(x)$ denne tar inn eit [[Sinus|forhold]] av den normale $sin=\frac{opp}{hyp}$, og gir ut vinkelen som når vi tar i gjennom $sin$ blir over til forholdet.
Basically vi får vinkelen (vinkeldomenet) ut i frå forholdet (forhold domenet ) når det er normalt frå forhold (forhold domenet) over til vinkel (vinkeldomenet). 

>[!WARNING] VIKTIGT:
>Det er viktig å bemekre seg på at ein invers funksjon er **ikkje** det samme som å settje den til $^{-1}$ grad, altså $\frac{1}{noe}$ likevel vi ofte sier at ein recirprocal ofte er inversen, dette er sjeldant sant. Når vi snakker om invers funksjoner er det annleis og vi snakker om å skifte domener. 
>Vi må gjer algebra rekning for å finne den inversefunksjonen.


### Formell definisjon.
Den formelle definisjonen av inversfunksjoner er 
viss $f^{-1}(f(x))=x$ og $f(f^{-1}(y))=y$
som gir mening fordi å finne y verdien gjennom f(x) gir y og $f^{-1}(y)$ gir x.

Alle inversfunksjoner er òg alltid [[Entydige funksjoner]].
Vertikale asymptotisers telje ikkje da fordi vell dei er udefinert verdier.

Alle oddetall grafer har ein full inversfunksjon, men alle andregrader starter på eit spesifikkpunkt for inversfunksjonen, fordi $\pm \sqrt{noe}$.
og vi bruker berre ein av dei $+\sqrt{noe}$ eller $-\sqrt{noe}$.


Ein viktig ting vi kan sjå er at dersom vi velger eit punkt på ein funksjon og den samsvarenede posisjon i inversfunksjonen kan vi sjå at x og y punktene er berre omvendt. $(a,b)$ er det samme som $(b,a)$ på inversfunksjonen. Berre husk at **alltid** er x først og y andt, dette gjelder òg inversfunksjoner. Dette viser berre sammenhengen.
Dette er vises gjennom at dei er symmetriske rundt linja $y=x$ og er inverse i punkta $(a,b)$.
 


#### Egenskaper til inversfunksjoner.
 * Er ein [[Entydige funksjoner]]
 * $D_f = V_{f^{-1}}$ og $V_f = D_{f^{-1}}$
 * Grafene til $f(x)$ og $f^-1(x)$ er symmetriske om linja $y=x$
 * Viss punktet $(a,b)$ liggjer på $f(x)$ så er punktet $(b,a)$ på $f^{-1}(x)$
 * $f^{-1}(f(x))=x$ og $f(f^{-1}(y))=y$
	 * Gir fullt mening. første finner først y og gir x til y verdien. 
	 * Andre gjer først y verdi over til x og så over til y igjen.
 * $f^{-1}(x)$ er strengt vaksende, viss bare **viss** $f(x)$ er det.
	 * Sjå [[Entydige funksjoner]]
 * $f^{-1}(x)$ er stengt minskende viss og bare **viss** $f(x)$ er det.
 * Vi finner den omvendte funksjonen gjennom å manipulere dei ulike sidene av likninga $y=f(x)$ for å finne $x$ åleine.



 # Rekne ut invers funksjon.
Å rekne ut den inverse funksjonen er ganske lett egentelig, det er berre å drive med lett algebra og litt manipulasjon. Det viktige er å vite kva for noko domene den originale funksjonene går ut på. Til dømes : $y=f(x)$. Viss vi ønsker å finne ut ein $x$ verdi gjennom ein $y$ verdi må vi gjere simpel algebra.

Det vi vil gjere er prøve å gjennom algebra få vårt ønsket inntaks domene satt åleine.
Slik:
$y=F(x)=\frac{2x+5}{4-3x}$
$y=\frac{2x+5}{4-3x}$
$(y)(4-3x)=2x+5$
$4y-3xy=2x+5$
$-2x-3xy=5-4y$
$(x)(-2-3y)=5-4y$
$x=\frac{5-4y}{-2-3y}$
$x=g(y)=\frac{5-4y}{-2-3y}$

Gjennom denne nye funksjonen $g(y)=f^{-1}(x)$. Viss vi skal finne $f^{-1}(x)$ så er dette heilt lik som $g(y)$ vi berre bruker $x$ som variabel namnet i staden for $y$ , viss vi skifter ut $y$ med $x$ så får vi framleis samme svar. Men viss vi skal gjere det i geogebra må vi ha $y$ som inntaks verdi. Dette med å skifte inntaksvariablene tilbake er kinda viktig, det skifter ingenting med den nye inversfunksjonen, men det er standarisert.

Slik ser disse invers funksjonene ut ved siden av kvarandre
```desmos-graph
y=\frac{2x+5}{4-3x}
x=\frac{5-4y}{-2-3y}

```

Du legger ikkje merke til det, men her er to ulike funksjoner!
Dette er fordi funksjonene ser heilt like ut når vi settjer det inn i eit grafikkfelt, men dei har begge ulike inntaks verdier. Interesannt 😎
Det er jo samme graf, berre ulike inntaksdomener!

[[Polynom grafer]]
[[Polynom aritmetikk]]
[[Polynom terminologi]]
[[Polynom faktorisering]]

### Rekne ut kvadratiske eller høgere funksjoner sine inverser.

Dersom vi vil  ha ein funksjon som har ein høg grød så må vi klare å faktorisere den inn i eit enkelt polynom form, dette betyr ingen konjugatsetning, berre den første kvardatsetningen, og den andre kvadratsetningen.

Deretter kan vi utføre kvadratrot på begge sidene og så isolere $x$ en.


##### Dersom vi ikkje har ein fin polynom.

Dersom vi ikkje har ein fin polynom som kan gå rett inn i ein av dei to kvadrat første setningene så må vi tvinge den til å bli det 😈. Det betyr egentelig at vi ikkje krever nokon [[Polynom faktorisering#ABC Formel Kvadratiske formel|abc formel]]. 
Vi kan nemleg ved å huske oppsettet til setningene til å tvinge dette frem. [[Polynom faktorisering]]


$(a+b)^2=a^2+2ab+b^2$. Dersom vi deler vårt midt term på 2 og $a$ sin koeffisient så kan vi isolere ein $b$. Dette kan vi ta i nytte.

Dersom vi sier at vi tar denne $b$ en vi nettopp har kalkulert og plusser på den i andre grad og deretter minuser i andre grad så kan vi faktorisere ut den første delen, og så har vi ein ekstra del vi ikkje kan faktorisere. Men denne biten kan vi berre flyte over til andre side.

La meg heller vise i staden for å forklare 🗿:
$y=x^2+3x-1$. 

```desmos-graph
y=x^2+3x-1

```



Vi vil ha vår $x$ verdi isolert.
Vi ser at denne følger ingen av kvadratsetningene fint, og vi vil **ikkje** bruke $ABC$ formelen fordi den kan gi svar som ikkje følger første eller andre kvadrat setning. **(Du kjem til å se kvifor vi vil ha dei første eller andre kvadratsetning.)**

Vi omskriver det slik
$y=x^2+3x+(\frac{3}{2})^2-(\frac{3}{2})^2-1$

Vi ser nå at den første delen kan gå inn i første kvadratsetning.
([[Polynom faktorisering]])

$y=(x+\frac{3}{2})^2-(\frac{3}{2})^2-1$

$y+(\frac{3}{2})^2+1=(x+\frac{3}{2})^2$

Nå kan vi berre ta kvadratroten av kvar side.
**Dette er grunnen til at vi virkelig ønsker første eller andre kvadratsetning.**

$\pm \sqrt{y+\frac{3^2}{2^2}+\frac{2^2}{2^2}}=x+\frac{3}{2}$

$\pm \sqrt{(y+\frac{13}{4})}-\frac{3}{2}=x$


>[!WARNING] HUSK $\pm$
>Husk $\pm$ ellers så får vi berre ein del av grafen.



Der har vi vår invers formel, og vi startet med ein andregradsfunksjon.

```desmos-graph
x=\sqrt{y+\frac{13}{4}}-\frac{3}{2}
x=-\sqrt{y+\frac{13}{4}}-\frac{3}{2}
```


Den grønne er den originale funksjonen
og den blåe er omjobbinga av funksjonen, men vi har ikkje skiftet på inntaksvariablene. Dette viser tydeleg korleis grafene henger sammen originalt.

>[!WARNING] Dette er **ikkje** feil. Ikkje mistolk grafen.
>Du forventar kanskje at grafen skal sjå annleis ut i ein graf kalkulator. Men dei er jo heilt like fordi det er jo samme graf vi driver med, men forskjellige inntaksvariabler/domener.



