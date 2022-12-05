# Derivanter & Derivasjon.

## Definisjonen av den deriverte.

^a349ff

Den deriverte er [[Polynom terminologi|vekstfaktorane/koeffisienta]] til den [[Momentan vekstfart|momentane/tangent veksfart]] ved $x$ gitt punkt til ein graf. 

Den deriverte funskjonen er ein funskjon som gir stigningstallet/vekstfaktoren til ein tangent/momentan  i eit polynom ved $x$ verdi. Det betyr at når den deriverte funksjonen gir oss ein negativ verdi betyr det at den originale funksjonen minsker i det punktet, og når det er ein positivt verdi betyr det at den originale funksjonen stiger i det punktet. Den deriverte funksjonen er alltid ein [[Polynom terminologi#Grad av polynom|grad]] lavere enn den originale funksjonen. Den deriverte grafen/funksjonen er simpelt sagt ein graf/funksjon som viser korleis den originale grafen/funksjonen utvikler seg over tid. $Y$ Verdien gir oss den momentane vekstfaktoren i den originale funksjonen ved $x$.

 Døme:
 $x^3$ funksjon, sin deriverte funksjon er $3x^2$ (Andre grad)

$7x+2$ funksjon, sin deriverte funksjon er 7. (Stigningstallet er 7 uansett for $x$ verdi).

Kvart nullpunkt i ein derivert funksjon viser eit ekstremalpunkt eller eit stasjonært punkt i den originale funksjonen, då stigningstallet der er alltid $= 0$. Vi kan sjå på dei [[Polynom grafer#Positive og Negative Intervaller|positive og negative intervalla/forteikn skifte]] for å då vite om det er eit topppunkt eller botnpunkt, viss det er ein endring som går i frå negativ til positiv, er det eit botnpunkt, viss det er ein endring i frå positiv til negativ er det eit topppunkt. Viss det er ingen endring i forteikn i intervalla er det eit stasjonært punkt. Viss vi forestiller ein polynom og ser på ekstremalpunkt kan vi lett forestille dette, og vi kan bekrefte dette ved å teste $x$ verdier høgere og lavere enn eit ekstremalpunkt og sjå på dens forteikn og verdi.
Vi veit at dette er ekstremalpunkt då ved nullpunktene til den deriverte funksjonen er verdien til den dertiverte funksjonen $= 0$ dette då betyr av det originale funksjonen har ein momentan vekstfart med ein $0$ i stigningstall ved dette nullpunktet. Når vi går nærmere dette nullpunktet går den originale funksjonen meir og meir i mot $0$ i stigningstall.


 Eit globalt topppunkt/botnpunkt i ein derivert funksjon viser når stigningstallet i den originale funksjonen er på det største/laveste. Likt viser eit lokalt topppunkt/botnpunkt det høgste/laveste stigningstallene i mellom nullpunkt på den originale funksjonen.

Visualisering:
![](http://ibmathstuff.wdfiles.com/local--files/maxandmin/Derivative%20of%20Cubic.png)
Den blåe grafen er den originale funksjonen, den røde er den deriverte.


## Finne den deriverte ved eit punkt.
### [[Gjennomsnittleg vekstfart]] med lav $\Delta \space x$. (Delta $x$).
Viss vi skal finne den deriverte trenger vi egentelig berre å finne stigningstallet til eit presist punkt slik som i [[Momentan vekstfart]], på lik metode som ved [[Gjennomsnittleg vekstfart#^40a02b|gjennomsnittleg vekstfart]] men vi bruker ein veldig lav delta $x$, istaden for intervalla som vi normalt bruker i gjennomsnittleg vekstfart.

Den deriverte finner vi altså slik:
$\frac{f(verdi+0.0001)-f(verdi)}{0.0001}$

Her er $0.0001$ den lave $\Delta \space x$ verdien. (Delta $x$). 

Eksempel:
$f(x)=2x^2$
$f'(2)=\frac{f(2+0.0001)-f(2)}{0.0001}$
$\rightarrow f'(2)=\frac{f(2.0001)-f(2)}{0.0001}$
$\rightarrow f'(2)=\frac{8.00080002-8}{0.0001}$
$\rightarrow f'(2)=\frac{0.00080002}{0.0001}$
$\rightarrow f'(2)=8.0002$
$\rightarrow f'(2)\approx 8$
Den deriverte her er omtrent $8$.

### [[Grenseverdier]] derivasjon.
Dette er den meir mattematiske fine metoden for å finne den deriverte.
I grunn fungerer dette heilt likt som gjennomsnittleg vekstfart metoden.
Men istaden for å ha ein lav konstant $\Delta \space x$ har vi faktisk ein $\Delta \space x$ som nærmer seg uendelig i mot tangenten. I andre ord vi har ein sekant ($f(x_{2})$)som nærmer seg uendelig nærme tangeten ($f(x_{1})$). Denne sekanten kommer til å ende opp med å ha samme vekstfart som tangenten då den går nærmere og nærmere tangenten. 
Vi bruker grenseverdi og settjer $\Delta \space x$ lik 0 (Her representerer $h$ Delta $x$-en). Då den skal vere minst mogleg, og grenseverdier treffer aldri tallet, men går berre uendelig i mot tallet. Vi settjer inn ein verdi for $x$ og får den deriverte av dette punktet.

$f(x)=\lim_{h\rightarrow 0}\frac{f(x+h)-f(x)}{h}$

Vi ofte forkorter dette ned til:
$\large \rightarrow \frac{df}{dx}$

Dermed skriver vi ofte derivanter slik:

$\large \rightarrow \frac{d}{dx}(funksjonen \space f)$


$df$ for $\Delta$ i $y$ verdier. Viser $\Delta \space x$ verdien sin forskjell i $y$ verdier.
Og $dx$ for $\Delta$ i $x$ verdier. Her i grenseverdi derivasjon er dette nærmest $0$.

Visualisering av Grenseverdi derivasjon:
![](https://web.ma.utexas.edu/users/m408n/2014/tangent1.gif)
$Q$ er sekanten, og $P$ er tangenten.
Sekanten nærmer seg uendelig tangenten og gir oss tangenten sin momentane vekstfaktor. **I gjennomsnittleg vekstfart derivasjon, er det nesten likt men der nærmer sekanten seg ikkje uendelig, men heller er sekanten berre svært nær.**

## Korleis finne den deriverte funksjonen.

### Momentan vekstfart.
Den mest tungvinte og dårlige metoden får å få den deriverte funksjonen er å finne fleire ulike mometane stigningstall ved ulike intervaller gjennom bla. [[Derivanter#Finne den deriverte ved eit punkt|gjennomsnittleg vekstfaktor]] og sjå om det er eit felles oppsett for kvar stigningstall ved gitt $x$ kordinat. Viss det er ein sammenheng mellom $x$ og stigningstallet, og dette fungerer for alle intervalla, så er dette den deriverte funksjonen. 
Problemet med denne metoden, er at for det første den er ekstremt tungvint, det er berre sikkert at den fungerer for dei spesifike intervalla. (Den deriverte funksjonen kan vere anneleis, men gi samme svar ved intervalla).

### Grenseverdi derivasjon. 
Heilt lik metode som ved grenseverdi derivasjon, dette gir oss den deriverte funksjonen. I staden for å skifte $x$ ved ein verdi lar vi berre $x$ vere $x$.  

[[Første derivasjonsregel.]]
[[Andre derivasjonsregel - Rasjonale funksjoner.]]



>[!WARNING] Dersom det tall som ikkje er inntaksverdien.
>Dersom det er tall som til dømes $x$ men $t$ er inntaksverdien, så later vi som at $x$ berre eit konstant tall fordi det er ikkje inntaksverdien.
>Til dømes: $g(x)=t^3*x-\pi*t^2+t*x^2+4$
>blir til $g'(x)=3t^2*x-\pi*2*t+x^2$

>[!INFO] Når $\Delta x$ går mot null.
>Når $\Delta x$ går mot null gjennom $\lim_{\Delta x\rightarrow 0} \Delta x$ pleier vi å skrive dette berre som $dx$

