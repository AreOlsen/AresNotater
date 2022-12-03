# Breadth first search.
Breadth first search er ein simpel algoritme som finner distansen frå ein  [[Beskrive grafer.|vertex]] til andre alle vertices på grafen, og den finner den shorteste path-en som gjer at vi kaller det ein shortest path algoritme. Vi bruker dei ulike metodene til å store [[Representere grafer.|grafer]] på til å searche gjennom disse. Av og til er ein betre enn ein anna. Den fungerer ved å starte ved ein source vertex og for så sjekker den alle nære vertexer om det er vår ønsket vertex, og gjer slik lag på lag videre, til den har fylt ut heile området. Måten den finner vårt slutt vertex gjer at den finner den korteste vegen, fordi når den først når vertexen har den allereie funnet den korteste vegen gjennom dens naturlege søkemåte. Vi pleier å representere distanse verdi frå slutten for å vite kor langt unna vi er, og så går vi berre nedover frå starten ned gjennom den laveste og sine nærmeste vertexes, og til slutt ender ein med målet. Slik:
![](https://cdn.kastatic.org/ka-perseus-images/1448249c9f4972b72248d899406a7f0c92fc5f3b.jpg).
Denne her grafen er ein undirected graf. Kvar vetex går til ein kube som ikkje er ein del av ein vegg, og kvar edge er mellom to tilkoblet kuber. 

Algoritmen breadth first search er som den er i namnet den går etter bredden først, i andre ord den sjekker gjennom alle adjacent vertecises før den går til kvar av disse verticesene sine tilkoblet vertices, og slik går den videre. Denne algoritmen fungerer for alle typer grafer, så lenge vi starter ved vår source vertex kan vi, viss mogleg, alltid komme til vår goal.

## Algoritmen.
Breadth first search algoritmen gir to ulike verdier for kvar vertex $v$:
1. Ein distanse
	1. Som viser minimum nummer av edges i ein path frå source vertex-en til vertex $v$.
2. Predecessor vertex av vertex $v$.
	1. Viser kva vertexer som leder inn i vertex $v$, startvertex har ein spesiell verdi som $null$. (Ikkje $0$ men $null$).

Dersom det er ingen path frå source vertexen til vertex $v$ så er $v$ sin distanse uendelig, og dens predecessor vertex har ein lik spesiell verdi som startvertexen.

Til dømes: her er ein undirected graf med åtte vertices, nummerert 0 til 7, med vertex nummerer som er over eller under (Indices). Inni kvar vertex er de to nummere, dens distanse frå source vertexen som i dette tilfellet er $3$, følgt av dens predecessor på den shorteste pathen frå vertex $3$. Ein $-$ indikerer $null$.
![](https://cdn.kastatic.org/ka-perseus-images/3545933c2fca71e45a03f1bb1bf2933b75c60e02.png)

I bfs setter vi origintalt distansen og predecessoren av kvar vertex til den spesielle verdien (null). Vi starter searchen på source vertexen og gir den ein distanse av $0$ til seg sjølv. Deretter går vi til alle dens naboer av sourcen og gir kvar nabo ein distanse av 1, og dens predecessor til å vere source vertexen. Deretter går vi til kvar av disse naboene, og sjekker alle dens naboer som ikkje allereie har blitt sjekket, og vi gir disse verticesene ein distanse av 2, og dens predecessor til å vere den naboen vi nettopp sjekket. Vi fortsetter slik til alle vertices som er moglege å nå i frå source vertexen har blitt sjekket, alltid sjekker vi alle vertices på distanse $k$ frå sourcen før vi sjekker nokon vertex på distanse $k+1$. Dei verticesene som ikkje er moglege å nå vil aldri bli sjekket.

Basically vi sjekker alle naboer, vi sjekker alle naboene sine naboer som ikkje har blitt sjekket endå, lagre verdi av distanse, repiter.

Vi veit at alle vertices som har ein verdi av $null$ er ikkje nåbare av source vertexen når vi er ferdig med å sjekke alle. Og at dei som ikkje har blitt nådd endå har òg verdi av $null$ fordi dei har ikkje blitt angitt verdier endå.

Det meir viktige spørsmålet er korleis vi kan holde følge med på verticesene som har blitt sjekket, men har ikkje vert starten av ein sjekk. For dette bruker vi ofte ein $queue$, som er ein data struktur som tillater oss å inserte og remove elementer, der den elementen vi fjerner er alltid den som vært lengst i queuen. Denne oppførselen kaller vi for *"first in, first out"*. Ein queue har tre operasjoner:
* enqueue(obj): inserter eit objekt inn i queue-en, og returnerer objektet.
* dequeue(): fjerner objektet som har vært lengst i queue-en.
* isEmpty(): returnerer true dersom queue-en inneholder ingen objekter i momentet det blir sjekket, og returnerer false dersom queue-en inneholder minst eit objekt.

Når vi først besøker ein vertex så enqueue me den. Ved starten enqueue med source vertexen fordi det alltid den første vertexen vi besøker. For å bestemme kvar for ein vertex vi besøker neste, så velger vi den vertexen som har vært i queuen lengst og fjerner den frå queuen, i andre ord så bruker vi vertexen som er returnert frå dequeue().

Merk at for kvart moment så innheolder queue-en entens aller vertices med samme distanse, eller den inneholder vertices med distanse $k$ følgt av vertices med distanse $k+1$. Dette sikrer at vi får besøkt alle vertices på distanse $k$ før vi besøker nokon vertices med distanse $k+1$.


```javascript
var doBFS = function(graph, source) {
    var bfsInfo = [];

    for (var i = 0; i < graph.length; i++) {
	    bfsInfo[i] = {
	        distance: null,
	        predecessor: null };
    }

    bfsInfo[source].distance = 0;

    var queue = new Queue();
    queue.enqueue(source);

    // Traverse the graph
    
    while(!queue.isEmpty()){
        var longestVertex = queue.dequeue();
        for(var i = 0; i < graph[longestVertex].length; i++){
            var search = graph[longestVertex][i];
            if(bfsInfo[search].distance===null){
                bfsInfo[search].distance=bfsInfo[longestVertex].distance+1;//W=1
                bfsInfo[search].predecessor=longestVertex;
                queue.enqueue(search);
            }
        }
    }
    
    
    
    // As long as the queue is not empty:
    //  Repeatedly dequeue a vertex u from the queue.
    //  
    //  For each neighbor v of u that has not been visited:
    //     Set distance to 1 greater than u's distance
    //     Set predecessor to u
    //     Enqueue v
    //
    //  Hint:
    //  use graph to get the neighbors,
    //  use bfsInfo for distances and predecessors 
    
    return bfsInfo;
};
```



## Analyse av breadth first search.
Vi kan vi at breadth first search openbart ein runningtime av $O(V+E)$, fordi vi går berre gjennom alle verticesene ein gang, og vi sjekker alle edgesene berre ein gang totalt. 

Men vi kan ta ein liten nærmere titt på matematikken bak dette, fordi vi elsker å analysere!
La oss anta for eit moment at $|E|\ge|V|$, da dette er casen for dei aller fleste grafer, spesielt dei med BFS. Da er $|V|+|E|\le|E|+|E| \rightarrow |V|+|E|\le 2\times |E|$, Da kan vi ignorere den nokre verdier fordi vi driver med [[Asymptotic notation.]]. Spesifikk [[Big O]].
Så ser vi at $O(V+E)$ egentelig betyr $O(E)$, fordi $E$ bestemmer nesten alt.

Derimot viss $|E|\lt |V|$ då er $|V|+|E|\le 2\times |V|$ og da vil $O(V+E)$ bety  nærmast det samme som $O(V)$. Vi kan settje disse to situasjonene sammen til ein ny asymptotisk notasjon av $O(max(V,E))$. Generelt viss $O(x+y)$ oppstår kan vi ofte korte det ned til $O(max(x,y))$, fordi den eine teller mykje meir enn den andre.

>[!INFO] Post scriptum.
>Noter ein graf er connected dersom det er ein path frå kvar vertex til alle andre vertices. Minimum numer av edges som den grafer kan ha er dermed $|V|-1$. Ein graf der $|E|=|V|-1$ blir kalt for eit **free tree**.

Grunnen til at BFS kjører i $O(V+E)$ tid er fordi det tar $O(V)$ tid å intialisere alle distanse og predecessore-ene for kvar vertex ($\theta(V)$). Kvar vertex blir besøkt maks ein gang ($O(V)$), fordi den einaste gange den blir nådd er når distansen er $null$, så kvar vertex er $enqueued$ på det maksimume ein gang. Siden vi eksaminerer kvar edge som er connected på ein vertex vil det på det maksimale ta $|E|$ vertices å søke gjennom alle dei. Derfor er det $O(V+E)$. 