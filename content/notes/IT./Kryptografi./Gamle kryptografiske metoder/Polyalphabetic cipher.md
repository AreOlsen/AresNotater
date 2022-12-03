# Polyalphabetic cipher

For å unngå at språket sin frekvens av bokstaver kan bli brukt til å [[Kryptografi.|dekryptere]] våre beskjeder slik som den kan i [[Ceaser cipher]] så kan prøve å minske fordelingen, altså gjere frekvensene i den enkrypterte meldingen sine tegn meir gjemne slik at det er mindre samanlignbart med språket sitt. Ein slik krypteringsmetode er polyalphabetic cipher, eller på norsk Polyalfabetisk cifer.

Eit slik polyalfabetisk cifer er egentelig berre mange ceaser cifere som er strukturert på ein måte som gjer det vanskeligere å kunne finne ut kva keyen er.

Eit polyalfabetisk cifer funger slikt:
Vi har eit ord som er vårt key: la oss ta eit døme av SNAKE, Engelsk for slange.
Eit polyalfabetisk cifer fungerer ved å leggje dette ordet under ein beskjed repiterende til beskjeden slutter. Deretter bruker vi nummeret på bokstaven som leggjer under beskjeden som ein shift key på bokstaven over. 

Ein kan i andre ord visualisere det slik:
$HALLO$
$SNAKE$

$HALLO$
$19,14, 1, 11, 5$

Vi skifter bokstaven H over til bokstaven som er 19 bokstaver høgere i Alfabetet enn H.
Likt som A med 14, L med 1, deretter L med 11, og deretter O med 5.

$HALLO \rightarrow OMWT$
Likevel vi ser at det er to L-er i HALLO så er det to ulike bokstavet for dei like bokstavene i den enkrypterte beskjeden.

## Løyse eit polyalphabetic cipher.

Det er ganske lett å finne ut kva eit polyalphabetic cipher sin key er.
Det vi trenger å gjere er nesten heilt likt som i Ceaser Cipher. 
Det vi gjer er først er på finne ut kor mange bokstaver det er i keyen.
Dette kan vi finne ut gjennom trail and error i ein frekvens analyse basert metode.
Likevel vi ser ein forandring frekvensene i ein bokstavene i ordet, vil det framleis vere nokre mønster som vi kan sjå etter. Etter vi har klart å konkludere antallet bokstaver.
Er det heilt likt som eit ceaser cipher, vi sjekker berre kvar N-te bokstav i keyen med den enkrypterte beskjeden og prøver å løyse ceaser cipher shiften. Dette kan vi gjere ved blant anna frekvens analyse eller til dømes bruteforce, og etterpå når vi veit alle shiftene kan vi omdanne dette til bokstaver og skaffe den originale shift keyen.




