# One time pad.
Den ultimate [[Kryptografi.|krypterings teknikken]]. I motsetning til [[Ceaser cipher]] og [[Polyalphabetic cipher]] har denne krypterings teknikken eit fingeravtrykk av null som gjer at den er umogleg å bruke nokon matematiske triks på for å kunne finne ut kva koden er.
Denne krypteringsteknikken heiter one-time pad.

I denne krypteringsteknikken skaper vi ein key som består av mange ulike tall som er valt av total tilfeldighet, og denne keyen er nøyaktig like lang som beskjeden slik at det er ingen repitisjon nokon sted som lager eit fingeravtrykk. Dette er nesten likt som [[Polyalphabetic cipher]] dersom vi tenker berre på tallene, men her er keyen like lang som beskjeden.

Fordi vi har ein total tilfeldighet vil mengden ganger ein bokstav oppstår i den enkrypterte beskjeden vere heilt tilfeldig.

Her er eit døme på ein one time pad:
$HALLO. Key:1,18,20,4,7 \rightarrow ISFPV$. 


## Umogleg å løyse eit one time pad ?
Viss vi prøver å finne den lange keyen så blir det ganske tungt ganske raskt fordi vi **må** gjere dette gjennom brute-force. Likt må vi sjekke alle moglege shift verdier som kan vere, for kvar einaste bokstav.

La oss ta eit døme:
$HALLO. Key:1,18,20,4,7 \rightarrow ISFPV$. 

Viss vi sier at vi berre kan ha bokstaver, og alfabetet vårt har ein lengde på 26, slik som i engelsk kan vi kalkulere alle moglege situasjoner for keyen:
$(26)^n$. Dette vokser ganske raskt....
For ordet $HALLO$ er det $26^5=11881376$ moglege situasjoner som er ganske mangen.
Dersom beskjeden hadde vore kanskje $\textit{HEI KVA HEITER DU}$ så hadde det vore $26^{14}=6.45099747\times 10^{19}$ situsjoner og det er ganske jævlig mangen situasjoner, cirka $6$ følgt av 19 nuller.

I [[Polyalphabetic cipher]] trenger ikkje keyen å ha ein lengde av beskjeden.