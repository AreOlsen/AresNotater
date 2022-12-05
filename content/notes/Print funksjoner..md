# Printing




## Printing av tall.

### Med antall desimaler.
Viss ein har lyst til å printe noko med $x$ antall desimaler i Python så må ein bruke ein spesiell type funksjon når ein skal printe det ut.


````python
#Med x antall desimaler, skift x ut til ønsket.
#variabelÅPrinte er ein tidligere definert variabel, evt berre tallet.
print("{:.xf}".format(variabelÅPrinte))
````



## Variabler i printing.

Vi kan printe fleire variabel samtidig som vi printer ut tekst.
Til dømes: kan vi printe ut "Hei, det er mengdePersoner i bussen".
Men korleis får vi mengdePersoner variabelen til å printe ut variabel verdien, i staden for berre namnet?

Det kan vi gjere på ganske mange ulike metoder, her ser vi på to ulike.
Vi kan til dømes: splitte opp teksten og addere variabelen slik at den blir 

````Python
print("Hei, det er " + mengdePersoner + " i bussen")
````


Men vi kan også berre direkte settje det inn i teksten med å ta i bruk spesiell syntax:

````Python
print(f'Hei det er {mengdePersoner} i bussen')
````

