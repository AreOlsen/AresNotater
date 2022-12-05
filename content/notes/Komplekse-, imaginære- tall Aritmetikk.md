# Komplekse og imaginærte tall Aritmetikk

# Første.

Det aller første vi gjer er å [[Simplisifesere røtter av negative tall|simplisifisere røttene som innehalder negative tallene]], eller finne [[Imaginære tall|i]] verdien.


# Addisjon
Addisjon med komplekse tall er faktisk svært lett. Det er nesten heilt likt som med [[Polynom aritmetikk]], vi later som at [[Imaginære tall|i]] er ein variabel i staden for $\sqrt{-1}$. Vi deretter fortsetter som det var polynom aritmetikk, vi opner parantesene og adderer [[Polynom terminologi#Term ledd|leddene]] som innehalder samme grad/eksponent verdi ($1^2$ og $2^2$ har samme eksponent verdi). Vi får då eit nytt kompleks tall.

Døme:
$(1+2i)+(3-3i)$
$\rightarrow 1+2i+3-3i$
$\rightarrow 1+3+2i-3i$
$\rightarrow 4-1i$
$\rightarrow 4-i$


# Subtraksjon
Heilt likt som med [[Polynom aritmetikk#Subtraksjon av polynomer|polynom subtraksjon]]. Vi setter det som skal bli subtrahert inn i ein parantes med forteiknet $-$ (Eller koeffisienten $-1$). Vi deretter multipliserer alle ledda inn i polynom som subtraherer med forteiknet/koeffisienten, Vi deretter drar polynomene ut av parantesene og fortsetter med å [[Komplekse-, imaginære- tall Aritmetikk#Addisjon|addere]] dei termene med samme $i$ grad sammen.

Døme:
$(3+i)-(2+i)$
$\rightarrow (3+i)-2-i$
$\rightarrow 3+(-2)+i+(-i)$
$\rightarrow 3-2+i-i$
$\rightarrow 1$


# Divisjon
Divisjon med komplekse tall



# Multiplikasjon

### Multiplikasjon av berre imaginære tall:
Viss vi har ingen koeffisienter fungerer dette heilt likt som med eksponenter, $i \times i = i^2$. Men viss vi har koeffisienter må vi multiplisere disse sammen før vi samler $i$ tallene. Deretter ser vi berre på eksponent mønsteret, og finner denne verdien og multipliserer med koeffisienten.
Eksempel:

Viss vi har koeffisienter, multipliserer vi disse sammen, og deretter multipliserer dei imaginære tallene sammen. Og fortsetter som vi gjorde over, ved å se på mønsteret, for det imaginære tallet, og så multipliserer vi denne mønster verdien med koeffisienten.

Eksempel:
$2i\times 3i$
$= 6i^2$
$= 6\times(-1)$
$= -6$

### Multiplikasjon av kompleksetall.

Multiplikasjon av komplekse tall er egenteleg svært enkelt, og er heilt likt som med [[Polynom aritmetikk#Multiplisering av polynomer|multiplikasjon av polynomer]], vi later som $i$ er ein variabel, og forsetter med å multiplisere normalt som i ved polynomer.

Eksempel:
$(2+i)(2+i)=2^2+2\times2\times i + i^2$
$\rightarrow 4+4i+i^2$
$\rightarrow 4+4i+(-1)$ (Sjekk ut eksponenter av $i$ viss du ikkje forstår kvifor $(-1)$ ).
$\rightarrow 4-1+4i$
$\rightarrow 3+4i$

# Eksponenter av [[Imaginære tall|i]].

Ulikt normale tall har $i$ eit fast verdi mønster når vi settjer den til ein eksponent.
Den veksler mellom positiv og negativ 1, og positiv og negativ $i$, ettersom eksponenten øker. $i$ har ein syklus på $i$, $-1$, $-i$, og $1$ når den opphøgd i stigende ekspontener.

Mønsteret:
$i^0=1$
$i^1=i$
$i^2=-1$
$i^3=i^2\times i \rightarrow -1\times i \rightarrow -i$.
$i^4=i^3\times i \rightarrow (i)(i)(i)(i) \rightarrow (-1)(-1) \rightarrow 1$.
$i^5=i^4 \times i \rightarrow 1 \times i \rightarrow i$
$i^6=i^5 \times i \rightarrow i \times i \rightarrow -1$
$i^7=i^6 \times i \rightarrow -1 \times i \rightarrow -i$
$\dots$

### Finne verdi av $i$ opphød til store eksponenter.
Vi tar og bruker syklusen, og spesiellt $i^4$ av syklusen.
Vi tar og skriver om på eksoponent slik at vi får ein $i^4$ opphøgd til ein annen verdi, då $i^4$ er alltid lik 1, vil dette få vekk store deler av reknestykket.
Viss ikkje det går ann å dele eksponenten på 4 og få det som $(i^4)$ blir opphøgd i, må vi dra nokre tall frå eksponenten inn i ein eigen $i^{antall \space dratt \space ut}$. Dette gjer at vi kan skrive om det til å få ein $(i^4)^{noko} + i^{antall \space dratt \space ut}$.  Viss vi har ein koeffisient, gjer vi det samme med $i$ verdien som om det var berre $1$ i koeffisient, og etter på ganger verdien vi får med koeffisienten.

Eksempel:
$(i^{100})$
$\rightarrow (i^4)^{25}$
$\rightarrow 1^{25}$
$\rightarrow 1$

Meir komplisert eksempel:
$(5i^{250})$
$\rightarrow 5 \times i^{250}$
$\rightarrow 5 \times i^{240} \times i^{10}$
$\rightarrow 5 \times (i^4)^{60}\times i^{10}$
$\rightarrow 5 \times 1^{60} \times i^{10}$
$\rightarrow 5 \times 1 \times i^{10}$
$\rightarrow 5 \times (i^4)^{2} \times i^2$
$\rightarrow 5 \times 1 \times i^2$
$\rightarrow 5 \times -1$
$\rightarrow -5$.


