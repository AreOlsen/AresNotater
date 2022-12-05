# Ceaser cipher.

Ceaser Cipher er ein ganske gammel metode for å enkryptere og dekrypte beskjeder i [[Kryptografi.]]. Og som namnet hintar til blei det brukt av Julius Ceaser og hans romer menn til å sende hemmelige beskjeder til kvarandre utan at nokon skal kunne forstå beskjedene.


Ein ceaser cipher enkrypsjon fungerer ved å flytte alle bokstavene i beskjeden til høgre med ein bestemt *shift key* i alfabetet. Slik at den som veit kva shift keyen er kan dekryptere ved å flytte til venstre kvar bokstav med samme shift key.

Størrelsen shift keyen kan vere er mellom $0$ der det er ingen shift, og antallet bokstaver i alfabetet-1. Dette er fordi vi kan forskyve heilt opp til den går til slutten, etter da vil den gå tilbake til starten, og vår shift blir berre det samme som ein shift på overskuddet.

Denne enkrypsjon metoden var i bruk fleire århundrer etter Ceaser døyde, og var ganske sikker i lang tid, fordi ingen forstod korleis den fungerte utanom Ceaser sine folk, og at det tar litt å finne shift keyen uansett om ein forstår den eller ikkje.

Metoden derimot etter 800 år i bruk blei øydelagt på eit simpelt papir skrive ein matematiker som viste den letteste måten å kunne dekryptere den på kort tid.


Ein kan visualisere Ceaser Cipheret slik:
![400](https://i.stack.imgur.com/Btyp1.png)


### Enkel matematisk måte å finne keyen.
Kvart språk har eit generelt frekvens av bokstav tall i ein tekst, i Engelsk til dømes er bokstaven $E$ den mest brukte bokstaven til normalt. Dette kan vi lett bruke til å dekryptere ceaser cipher på kort tid.

Dersom vi teller antall ganger ein bokstav oppstår i ein tekst og samanligner den mest brukte med den som er mest brukt i det språket som det er skrivet i så kan vi sjekke kva keyen mest sannsynleg er. Viss vi sjekker forholdet mellom dei to mest brukte bokstavene i teksten og språket, og ser ein viss distanse mellom dei i alftabetet så er antagentligvis keyen distansen.

Her er eit døme.

Enkryptert beskjed:
```
Oruhp Lsvxp lv vlpsob gxppb whaw ri wkh sulqwlqj dqg wbshvhwwlqj lqgxvwub
Oruhp Lsvxp kdv ehhq wkh lqgxvwub'v vwdqgdug gxppb whaw hyhu vlqfh wkh 1500v,
zkhq dq xqnqrzq sulqwhu wrrn d jdoohb ri wbsh dqg vfudpeohg lw wr pdnh d wbsh
vshflphq errn. Lw kdv vxuylyhg qrw rqob ilyh fhqwxulhv, exw dovr wkh ohds lqwr
hohfwurqlf wbshvhwwlqj, uhpdlqlqj hvvhqwldoob xqfkdqjhg. Lw zdv srsxodulvhg lq
wkh 1960v zlwk wkh uhohdvh ri Ohwudvhw vkhhwv frqwdlqlqj Oruhp Lsvxp sdvvdjhv,
dqg pruh uhfhqwob zlwk ghvnwrs sxeolvklqj vriwzduh olnh Dogxv SdjhPdnhu
lqfoxglqj yhuvlrqv ri Oruhp Lsvxp.
```

Vi sjekker frekvensene:
```
A	31
B	18
C	10
D	45
E	64
F	16
G	27
H	73
I	44
J	11
K	21
L	60
M	19
N	45
O	47
P	38
Q	38
R	49
S	58
T	43
U	41
V	44
W	49
X	19
Y	18
Z	6
```

Vi ser at H er mest brukt i teksten, og vi veit at normalt i engelsk er E den mest brukte. Derfor kan vi ta eit tipp på at distansen mellom E og H er det som er keyen. Vi sjekker med ein shift av 3 som er distansen.


Vi tester shift key 3 til venstre og får:

```
Lorem Ipsum is simply dummy text of the printing and typesetting industry.
Lorem Ipsum has been the industry's standard dummy text ever since the 1500s,
when an unknown printer took a galley of type and scrambled it to make a type
specimen book. It has survived not only five centuries, but also the leap into
electronic typesetting, remaining essentially unchanged. It was popularised in
the 1960s with the release of Letraset sheets containing Lorem Ipsum passages,
and more recently with desktop publishing software like Aldus PageMaker
including versions of Lorem Ipsum.
```

Dette er akkurat Engelsk vi har vår korrekte shift key, gjennom å sjekke distanser mellom tall.
Denne metoden for å prøve å dekryptere *keys* heiter "*Frekvens analyse*", (Er funnet i andre området òg).

## Kvifor vi kan bruke frekvens analyse.

Grunnen til at vi kan bruke frekvens analyse her er fordi Ceaser Cipheret har eit gjømt fingeravtrykk, dette tyder til at måten som språket til beskjeden er strukturert på gjer at vi kan lettere kunne dekryptere meldingen ved å analysere fellestrekk i den og samanligne det med den enkrypterte meldingen. Andre krypteringsmetoder forsøker å minske fingeravtrykket som er til staden i språket gjennom dens enkrypteringsmetode.
