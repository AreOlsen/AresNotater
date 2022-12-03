# Sinusformet funksjoner (Sinusoidal functions).


# Kva dei er
Sinusformet funskjoner er funksjoner som liknar på ein av dei to trigonometriske funksjonene : sinus og cosinus.
Vi kan altså dermed lage ein funksjon som er lik til denne grafen ved å ta i bruk disse to funksjonene.

Eit døme på ein sinusformet funksjon:
![](https://mathbooks.unl.edu/PreCalculus/images/imagesChap14/negsinGraph.png)


# Amplitude
## Kva det er
Amplituden til ein sinusformet graf er kor langt ekstremalpunkta til grafen er i frå likevektslinjen, det tyder altså i andre kor mykje den trigonometriske funksjonen blir multiplisert med.

Eit døme på ein ampltiude i ein likning er som følgende:
$f(x)=5\times \sin(x)$.
Her er amplituden 5. Den går i andre ord 5 enheter på y aksen i frå likevektslinjen.


## Rekne ut amplitude frå likning.

Viss vi har botnpunktet og topppunktet henholdsvis: (5,-1) og (6,1). 
Da kan vi rekne ut amplituden ved å addere den absolutte verdien av forskjellen på y aksene, og så dele på 2.
Til dømes, viss vi har eit botnpunkt (5,-1) og eit anna topppunkt (6,1). Så kan vi finne amplituden slik
$\frac{2}{2}=1$, den absolutte verdien av distansen mellom dei ulike ekstremalpunkta er 2, og sådeler vi på 2.

# Midline (Likevektslinje)
## Kva det er
Midlinen eller som det heiter på norsk likevetkslinjen er det y verdien der den sinusformet grafen reflekterest. Vi kan tenke på dette som posisjonen heile grafen er forskyvet på y aksen med. 
Her er eit bilete som viser likevektslinjen.
![](https://cdn.kastatic.org/googleusercontent/e-KuFPdzsUaDF39JIYWxVHbEdW2bNT7xWhTHM5wj7RxLPGIMhHMs39JaTee_MOZLqOJUu1jbIubqjSP1owDmGnw)
## Rekne ut midline (Likevektslinje) frå likning.
For å rekna ut midlinen kan vi faktisk ta i bruk amplituden. Som vi nemnte i amplitude så er amplituden det samme som distansen frå eit av ekstremalpunkta til likevektslinjen. Det går sjølvsagt å bruke ann å bruke andre metoder, men denne føler eg gir mest mening og er finest.
* Viss vi har eit botnpunkt så adderer vi amplituden og får likevektslinjen sin y verdi.
* Viss vi har eit topppunkt så subtraherer vi amplituden og får likevektslinjen sin y verdi.

Til dømes: vi har amplituden 5 og topppunkt (5,5). 
$\text{topppunktet sin y verdi}-\text{amplituden}= 5-5 = 0$.
Likevektslinjen sin y verdi er 0.


# Periode.
## Kva det er.
Ein periode er $x$ verdiene det tar for å komme seg tilbake til det originale startpunktet på [[The unit circle|enhetssirkelen.]] Normalt er altså perioden $2\pi$. Men denne kan variere frå graf til graf, og det er her vekstfaktoren til ein graf komme inn i tanke, men det snakker vi om litt seinare. 

Ein kan tru at perioden er egentelig berre $\pi$ fordi ein får nøyaktig samme y verdi når vi driver med sinus fordi det har samme y verdi, og likt med cosinus kvar $\pi$ etter $\frac{\pi}{2}$, men tenk på det har vi kommet tilbake til samme punkt på enhetssirkelen, nei! Vi har komt til ein som har samme verdi, men er ikkje på samme punkt. Dette er òg noko som vi leggjer merke til når vi ser på grafen, det er samme y verdi, men vi går i den nøyaktig omvendte retningen som tyder til at vi ikkje har kommet tilbake til det samme punktet på enhetssirkelen.

Her er eit bilete som betre visualiserer perioden: (Berre fokuser på perioden. Peak to peak amplitude er ikkje noko vi faktisk pleier å bruke! Når vi snakker om amplitude er det berre peak amplitude vi snakker om.)
![](https://www.desolutions.com/blog/wp-content/uploads/2013/04/Vib4-13Fig-1.jpg)
# Phase-shift.
Phase shifting er kanskje det mest irriterande/kompliserte med sinusformet grafer. Av og til er grafer ikkje der dei normalt pleier å starte. Av og til kan sinusformet grafer faktisk starter på heilt uforventa punkter til dømes starter kanskje ein cosinusfunksjon der ein sinusfunksjon pleier å starter. Dette er unormalt for cosinusfunksjoner!
Dette er fordi vi har ein konstant faktor som forandrar verdien til $x$ inni den trigonometriske funksjonen, som gjer at når vi har $x=0$ så har vi faktisk ein anna verdi inni den trigonometriske funksjonen!
Ein negativ phase-shift drar grafen til høgre, og ein positiv ein drar den til venstre. 
Her er eit døme:
$\sin (x-\frac{\pi}{2})$, sinus funksjonen pleier å starte ved 0, men her starter den faktisk med $\frac{\pi}{2}$ fordi vi har phase-shifted den. 
Dette betyr at når $x=0$ så har vi faktisk ein negativ verdi inni sinusfunksjonen på $\frac{-\pi}{2}$ som gir tallet $-1$ som ikkje er det sinus funksjonen pleier å starte med!

Her er ein illustrering av ein phase-shifted graf:
Som vi kan sjå er den forskyvet $\frac{\pi}{4}$ til venstre.

![](https://www.onlinemath4all.com/images/phaseshiftintriggraph.png)

# Growth factor. (Vekstfaktor).
Som nemnt tidligere har ofte ein sinusformet graf ein periode som ikkje er på den normale $2\pi$ dette er fordi inni den trigonometriske funksjonen er den vekstfaktor som blir multiplisert med alt og gjer at grafen går raskere med verdien av faktoren.

Eit døme på ein vekstfaktor:
$\sin (2x)$. 
Denne sinus funksjonen nå går plutseleg dobbelt så raskt i periode fordi den blir multiplisert inni grafen, det er blitt kortere i bølgelengde/periode.

Dette kan bli kombinert med til dømes ein phase-shift då vil det så nokelunde likt som:
$sin(a(x+b))$
kan òg for så vidt vere cos, men eg brukte berre sin i eksempelet.
Her er $a$ vekstfaktoren, og $b$ phase-shiften.

Viss vekstfaktoren er lavere enn 1, vil grafen ha ein lengre periode enn det normale.


Dei tidlegare nemnte eksempela har ein verdi som alltid vil ha sine ekstremalpunkt ved noko $\pi$ verdi, enheten på $x$ aksen er altså fortsatt $\pi$.
Men nokon ganger vil vi ikkje ha $\pi$ som enheten, av og til vil vi reine tall som til dømes: 1 eller 2.

Da må vi sikkre at vi har perioden $2\pi$ som ein del av vekstfaktoren.
Viss vi vil ha ein periode på nøyaktig ein så må vekstfaktoren vere 1 fordi då etter 1x, har vi gått ein heil periode på $2\pi$. 
Likt kan vi òg ha ein ny periode som ikkje har enhet av $\pi$ heller, ved ha ein vekstfaktor som er å dele $2\pi$ på $\textit{den ønsker perioden}$. Slik $\frac{2\pi}{\textit{ønsket periode}}$.

Dette vil fungere fordi etter vår ønsket periode vil vi da ha gått nøyaktig $2\pi$ i lengde.

Eit døme på ein sinusformet graf med periode av 3 ser slik ut:
$cos(\frac{2\pi}{3}(x+b))$. Der $b$ er phase-shiften (kan òg vere $0$).

# Å modellere ein sinusfunksjon frå nokre punkter.


Etter alt vi har gått igjennom i dette bilete så kan vi prøve å modellere ein sinusgraf i frå berre nokre par punkter.
Alt vi trenger er eit av ekstremalpunkta og likevektslinjen, eller begge ekstremalpunkta. Begge punkta må vere ved siden av kvarandre!

1. Vi finner amplituden
2. Vi finner likevektslinjen.
3. Vi finner vekstfaktoren.
4. Vi finner phase-shiften.
5. Vi settjer alt sammen til ein funksjon.