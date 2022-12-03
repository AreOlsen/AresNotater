# Vektorer, to dimensjoner.
Vektor er egentelig matematisk sett på som ein liste med verdier, men i fysikk gir med disse verdiene ein tilsvarenede verdi på eit kordinatsystem.


## Resulterende.
Den resulterende er det same som verdien vi får når vi addere eller subtrahere to eller fleire vektorer. 


## Vektor komponenter.

Vektor komponenter er dei ulike aksene til vektoren, til dømes $x$, $y$, $z$ akse. Men vektorer kan gå opp i uendelig mange dimensjoner og dermed kan vi ha mange akse verdier.

Her er eit døme av dei to ulike vektor komponentene i 2D, og den tilsvarende vektoren.
![](https://blogmedia.testbook.com/blog/wp-content/uploads/2022/01/image-requirement-maths-articles_tb_fig_3-ac69a67d.png)

$V_x$ går til høgre ein verdi, og så $V_y$ oppover. Og dermed blir $V$ det samme som $V_x+V_y$.
Vi kan tenke på $V_x$ og $V_y$ som eigne vektorer.

Her er vektor komponentene i 3D:
![350](https://upload.wikimedia.org/wikipedia/commons/thumb/e/e7/Velocity-vector-3D-and-components.svg/1831px-Velocity-vector-3D-and-components.svg.png)

Litt meir kompliserte å sjå, men vi kan sjå alle dei tre ulike akse verdiene.
$x$ aksen,  $y$ aksen, og $z$ aksen.

>[!WARNING] NB.
>I 3d dimensjoner så er ikkje $y$ oppover, her er det $z$ som er oppover.
>$y$ er berre oppover i tre dimensjoner.




### Finne vektor komponenter gjennom trigonometri.
Viss vi har ein vektor som vi veit størrelsen på kan vi finne kva dei ulike vektor komponentene er dersom vi har ein eller fleire vinkler gjennom trigonometri.

Til dømes:
![[Vektorer, to dimesjoner. 2022-07-08 19.27.13.excalidraw]]


Vektor sin størrelse er det same som hypotenus, og dermed viss vi har ein vinkel kan vi finne ut kva aksene sine vektor verdier er. Vi må huske å ta i tanke vektoren sin retning når vi settjer verdiene til akse vektorene. Vi kan ikkje akkurat ha ein x vektor som går til høgre, når den normale går til venstre.

Vi kan òg finne kva vinkelen var viss vi har ulike verdier, dette kan vi gjere fordi vi har dei trigonometriske funksjonene sine invers funksjoner.

Og vi kan finne ut kva vektor størrelsen er, ikkje retning, ved å ta i bruk Pytagoras læresetning.


## Vektor addisjon.
Vektor addisjon er ganske simpelt, det er berre å addere dei ulike akse verdiene i alle vektorene som skal bli addert saman med kvarandre. Til dømes:
$C=(5,5), + G=(2,5)$
$C+G=(5+2,5+5)$
$C+G=(7,10)$

Dette er basic game programmering.

Her er koss du gjer det visuellt.
Husk hovudet må alltid gå til ein hale av ein anna vektor dersom vi skal addere.
![](https://i.ytimg.com/vi/0tv92MX2_ro/maxresdefault.jpg)



Vi plasserer tupp av av $F_1$ ved start av $F_2$ drar linjen mellom $F_{1,start}$ og $F_{2,slutt}$ dett er vår adderte vektor.

## Vektor subtraksjon.
Vektor subtraksjon er nesten heilt likt som vektor addisjon men det er ein sterk differanse. Når vi driver med vektor subtraksjon så må vi fjerne den eine vektorenen frå den andre. Dette er det same som å skifte forteiknet til alle verdiene inni vektoren, og så addere.

La oss si at vektoren $C = (5,5,5)$ ($x,y,z$), her i 3D.
Når vi skal fjerne vektoren $G = (5,-5,5)$ så må vi gjere slik:
$(5,5,5)-(5,-5,5) = (5-5,5-(-5),5-5) = (0,10,0)$.
Den ferdige vektoren blir $(0,10,0)$
Vi subtraherer $x$ verdiene med kvarandre, $y$ verdiene med kvarandre, og $z$ verdiene med kvarandre.

2D eksempel:
$C=(5,5) - G=(1,0)$
$C-G = (5-1,5-0)$
$C-G=(4,5)$

Her er korleis ein gjer det visuellt.
Husk å gjer den vektoren som blir subtrahert motsatt, den er jo som sagt negativ.
![[Vektorer, to dimesjoner. 2022-07-08 19.02.49.excalidraw]]



>[!WARNING] Normale feil med vektor addisjon og vektor subtraksjon.
> Når vi gjer vektor addisjon visuellt må alltid eit hode gå inn i ein hale på ein vektor, viss begge hodene går til samme plass så vil ikkje vektor addisjonen /subtraksjonen ha korrekt verdi.  Tenk tilbake på all din game programmering, dette er ganske lett å forstå.
