# Polynom Divisjon.

## Kva er polynom divisjon?
Polynom divisjon er berre ein del av [[Polynom aritmetikk]], men står litt ut i frå dei andre. 
Det er ikkje likt som dei andre formene av aritmetikk. Dette har unntak, ingen setninger, eller simpel utrekning, her har vi metoder vi må ta i bruk. Polynom divisjon er som normal divisjon berre med polynomer i staden for tall, og vi kan igjenkjenne nokre normale metoder frå divisjon her i dette polynom feltet.


### Kva er remainders?
For å introdusere dette la oss dele 37 på 6, vi veit at tallet er eit desimaltall då 6 går berre inn i 37 seks ganger før det ikkje følger gangetabellen. Vi har altså 1 igjen etter dei seks gangene, for å oppnå $\large \frac{37}{6}$, må vi få den einen til å bli eit desimaltal som oppgjer divisjonen, dette desimaltallet har ein verdi av $\large \frac{1}{6}$. ($\large \frac{1}{6}\times 6 = 1$). Då vil $\large \frac{37}{6} = 6+\frac{1}{6}$. 
Likt er det med [[Polynom terminologi#Kva er ein polynom|polynomer]], i grunn er dei jo berre tall skjult bak variabler, dermed oppfører dei seg likt! Når vi bruker [[Polynom divisjon#Algebraisk lang divisjon|algebraisk lang divisjon]] oppnår vi ikkje alltid ein fullstendig divisjon, likt som  $\frac{37}{6}$ er ikkje fullstendig. Då pleier vi ofte å bli lagt igjen med remainders, også kjent som tallet som blir lagt igjen før det blir fullstendig (I 37/6 blei 1 lagt igjen).

## Algebraisk lang divisjon.

^4aa794
Først av alt skriv begge polynomene inn i [[Polynom terminologi#Standard form|standard form!]] Både den som blir dividert og den som dividerer. Vi skriver inn polynomet som skal bli dividert, ein linje som går i frå venstre siden av den, og til høyre topp av den. Til venstre av linjen skriver vi polynomet som skal dividere. Vi finner kor mangen ganger det [[Polynom terminologi#Grad av polynom|høgste grad]] [[Polynom terminologi#Term ledd|leddet]] i frå det dividerende polynomet går inn i det  høgste leddet inn i det til å bli dividert polynomet. Vi bruker dette tallet og ganger ut med det dividerende polynomet, deretter [[Polynom aritmetikk#Subtraksjon av polynomer|subtraherer]] vi dette i frå det til å bli dividert polynomet. Vi rekner ut og repiterer denne prosessen med den nye verdien til polynomet er entens heilt utdividert eller vi bli igjenlatt med ein [[Polynom divisjon#Kva er remainders|remainder]]. Referer til bilete under for å forstå dette betre! Det er vanskelig å forklare slike lange prosesser.

![500](https://i.ytimg.com/vi/8lT00iLntFc/maxresdefault.jpg)

### Med remainders.
Når vi har remainders er det egentelig ganske lett, når vi ser at det høgste ledder i frå det dividerende polynomet ikkje går inn i det nåværende verdien i det heile er dette [[Polynom divisjon#Kva er remainders|remainderen]]. Viss vi blir igjenlatt med ein remainder settjer vi berre dette ved siden av det utdividerte polynomet, med ein divisjon på det dividerende polynomet.

Døme/eksempel:
$\large (x+2)+\frac{2}{x+3}$
Her er det dividerende polynomet, $x+3$.
Og remainderen er $2$.
Det utdividerte polynomet er $x+2$.

## Remainder theorem.
### Kva er remainder theorem?
Remainder theorem, er ein teori som viser oss om eit polynom har ein remainder ved ein viss $x =$ verdi.  Det igjenstående tallet er remainderen, viss tallet $= 0$, er det ingen remainder og tallet, viss det er noko annet enn $0$ har vi ein remainder på dette tallet.

$f(x) \leftarrow$ polynom divider med $x-a$
$\rightarrow \text{Remainder} = f(a)$
$f(x) \leftarrow$ polynom divider med $x+a$
$\rightarrow \text{Remainder} = f(-a)$

### Korleis bruke.
Vi simpelt berre settjer inn $x =$ verdien inn i funksjonen, rekner ut, og får remainderen. Dette er ein god metode for å finne ut om eit tall har ein faktor ved $x =$ verdi, då viss det er 0, er tallet ein $x=$ verdi i ein faktor, viss ikkje er det ikkje ein faktor. Viss det er ein faktor kan vi blant anna bruke [[Polynom divisjon#Algebraisk lang divisjon|algebraisk lang divisjon]] for å dividere. 

Eksempel:
$f(x)=x^2+5x+6$
Teste om $-2$ er i ein faktor:
$f(-2)=0$. Dette betyr at polynomet innehalder ein faktor av $x=-2 \rightarrow$ $(x+2)$ 

Teste om 1 er ein faktor:
$f(1)=1+5+6$
$f(1)=11$, remainder av 11, ikkje ein $x=$ verdi i ein faktor.
Viss vi deler på $x=1 \rightarrow (x-1)$ vil vi få eit polynom med ein remainder av av 11.
(Viss funksjonen hadde vore ein [[Polynom terminologi#Rasjonale funksjoner Polynom brøker|rasjonal funksjon (polynom brøk)]], hadde vi hatt ein remainder med $\frac{11}{\text{Det dividerende polynomet}}$)

### Mattematiske beviset.
^dd314c
$f(x) \leftarrow$ polynom divider med $x-a$
$\rightarrow \text{Remainder} = f(a)$
$f(x) \leftarrow$ polynom divider med $x+a$
$\rightarrow \text{Remainder} = f(-a)$


Alle polynomer med remainder kan skrivest som:
Viss $x$ nullpunkt verdien er positiv.
$f(x)=q(x)(x-a)+r$, der $q$ er ein polynom funksjon, $(x + a)$ er inntaks faktoret, og $r$ er er remainderen.
$f(a)=q(a)(a-a)+r$
$\rightarrow f(a) = q(a) \times 0 + r$
$\rightarrow f(a) = r$

Viss $x$ nullpunkt verdien er negativ:
$f(x)=q(x)(x+a)+r$, der $q$ er ein polynom funksjon, $(x - a)$ er inntaks faktoret, og $r$ er er remainderen.
$f(-a)=q(-a)(-a+a)+r$
$\rightarrow f(-a) = q(-a) \times 0 + r$
$\rightarrow f(a) = r$

**$q(x) = \text{Resultat av divisjon av polynom, og inntaksfaktor}$**
Kombinert då med inntaksfaktoret gir oss samme polynom som startet med.



## Unntaka.
Når vi deler på ein polynom som innehalder andre termer enn berre $x$ vil det alltid vere eit unntak for når divisjonen oppholder. Når $x$ verdien i nevnerenenes faktorer kansellere konstantleddet i faktoren vil vi ha [[Polynom terminologi#^f61e26|bryddpunkt]]. Eller viss det er ingen konstantledd då er detnår $x = 0$.  Dette i andre ord betyr at polynomet $=$ null i neveren. Noko som vi ikkje liker å ha i nevneren fordi det betyr at vi deler på 0. Og å dele på 0 er udefinert og vi har ingen verdi som vi kan dele på. Det er her den [[Polynom grafer#^8b580b|vertikale asymptoten]] oppstår.