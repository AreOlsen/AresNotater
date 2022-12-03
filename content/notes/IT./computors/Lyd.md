## The fuck e lyd.
Lyd er trykkbølger i luft og andre medium.
Vibrasjonene av luft registreres i øret og tolkes som lyd

## Bits? 
Det er også viktig å bestemme kor mangen bit som vi skal registrere for kvart registrert punkt, dette skjer normalt i 16 bit.

Vi har samplingfrekvens originalt på 44100 samplinger per sekund,  da vil vi dersom vi bruker 16 bit, ha $44100\times 16=705600$ bits lagret per sekund. Dette hadde blitt ugitt på begge ørene, dette er mono lyd.

Dersom vi bruker stereo og har ulike lydnivåer per øre/høytaller vil dette bruke dobbelt så mykje bits, så $44100\times16\times 2 = 1411200$ bits per sekund.

Det er mangen lyder som er så høg i frekvens at ørene berre gjer nah fam we don do dat here. Alt over disse frekvensene berre nah we ain doin dat sier pcen, den sier berre nop, d er eg for lat for.

Når vi sampler lyd pleier vi å bruke området mellom 38768 til 38767,.

Vi har rn svært mykje bits brukt per sekund, nah for real?

## Vi komprimerer shitet!
Vi lagrer forskjeller i amplitude og frekvens kvar måling i staden for å sjekke kor høgt dei er kvar gang, dette sparer mangen bits.




Ein anna metode er å bruke ein FFT til å splitte alt opp inn i nokre få sinus funksjoner og deretter bruke funksjonene i runtime og skape lyden matematisk.