# Insertion sort.
Tenk deg at du spiller eit kortspill og dealeren gir deg eit nytt kort, dei kortene du allereie har er sortert. Gå ned linjen av kortene dine til du finner posisjonen kortert er lavere er den neste, men høgere enn den bak ($bak \le kortet \le neste$). Plasser kortert der, så gjer du dette med kvart einaste nye kort du får. Slik fungerer insertion sort, men "kortet" du får av "dealeren" er det neste elementen å sorterte i ein liste.
Start med siste element index 1 og jobb deg oppover. Vi kan også starte i frå høgre av arrayen og jobbe oss nedover i staden for oppover.  Viss vi har ein heilt usortert array kan vi også sortere denne med insertion sort òg. Vi deler arrayen  i to, ein sortert side og ein usortert side. Vi går oppover listen og plasserer elemntet vi har ned til rett på den "sorterte" listen, slik at vi "inserte" elementet inn i listen. Den sorterte listen er alltid under indeksen til det nåværende å bli sortert elementet.

## Psuedo kode.
1. Call insert til å inserte elementet på index 1 inn i den sorterte subarrayen på index .
2. Call insert på index 2 på subarray mellom 0 $\rightarrow$ og 1.
3. Call insert på index 3 på subarray mellom 0 $\rightarrow$ og 2.
4. …… Repiter.
5. Call insert på element $n-1$ index inn i subarray 0 $\rightarrow$ og $n-2$.


Her er ein visualisering av insertion sort:
![](https://upload.wikimedia.org/wikipedia/commons/9/9c/Insertion-sort-example.gif)