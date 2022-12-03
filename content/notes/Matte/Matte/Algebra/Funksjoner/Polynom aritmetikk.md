# Polynom Aritmetikk.

## Addering av polynomer.

Addering av polynomer er ganske lett. Vi starter med to ulike polynomer i to ulike paranteser, men vi kan fjerne parantesene.
Vi later så sei at termene er normale tall. Vi pleier å gruppere termene som har like eksponenter i $x$ verdi. 
Dei termene som har lik eksponent i $x$ verdi kan vi gjøre aritmetikk med, men vi kan ikkje gjøre aritmetikk med termer som har ulike eksponent verdi i $x$. Viss den eine parantesen har eit tall som ganges foran, må vi huska å gange det ut før vi gjør aritmetikken. Husk at negative termer holder seg negative når dei dras ut av parantesen. I andre ord så ganger vi forteiknet utanfor parantesen med forteikna innanfor parantesen. If you catch my drift!

Vi så rekner berre ut, og får svaret av adderingen.

Eksempel:

$(5x^2+8x-3)+(2x^2-7x+13x)$, blir til:
$5x^2+8x-3x+2x^2-7x+13x$, blir til:
$5x^2+2x^2+8x-7x+13x-3$, blir til:
$7x^2+14x-3$.

## Subtraksjon av polynomer.
Subtraksjon av polynomer er veldig likt addering av polynomer!
Den einaste småe forskjellen er at vi må huske å gange forteikna foran parantesen med forteikna inni parantesen. Helt likt som i addering av polynomer. Vi kan berre subtrahere dei termene som har lik eksponent i $x$ verdi. Viss eit tall er foran parantesen må det ganges ut med parantesen før vi fortsetter med subtraheringen.
Vi så rekner berre ut, og får svaret av subtraheringen.

Eksempel:

$(16x+14)-(3x^2+x-9)$, blir til:
$16x+14-3x^2-x+9$, blir til:
$-3x^2+16x-x+14+9$, blir til:
$-3x^2+15x+25$.


## Multiplisering av polynomer.
### Areal modell.
^1d880f
Vi kan tenke på polynomer multiplikasjon som arealet til eit rektangel, kube, etc. Der kvar faktor er ein dimensjon. Til dømes: $f(x)=(x+2)(x-2)$ har to sider, av ein kube. Kvar ledd innan faktoren er ein eigen side av ein kube. Vi ganger då sidene ut og får kvar kube sin areal, og deretter adderer dei saman. Arealet er likt som når vi bruker [[Polynom aritmetikk#^f59c58|fordelingsegenskapen til multiplikasjon]]! 

Eksempel (Areal/Utskrivet polynom nederst):
![](https://cdn.kastatic.org/googleusercontent/X1kMAy0h-uKDm_z90T8peu7R3ph5TTKUqxdYDzayni4J0PQvXNtUGpKTFuuZl03WpXwmWAM60dthAkWcgr1nq6TN)


### Distributive property (Fordelingsegenskapen til multiplikasjon).
^f59c58
Distributive property, eller fordelingsegenskapen til multiplikasjon som det heiter på norsk er kanskje den mest logiske og rettfrem måten for å rekne ut polynomer som består av faktorer. Det vi gjer er at vi ganger kvart ledd i ein faktor med heile den andre faktoren, vi gjer dette for kvart ledd i den eine faktoren. Det går ann å multiplisere fleire faktorer slik ved å gange eit ledd, med eit ledd $\dots$, og deretter heile faktoren, men dette er veldig tungvingt og feil kan lett oppstå. Viss det er fleire faktorer anbefaler eg å berre gange ut to faktorer og settje dei i ein parantes, dette har lik verdi som dei to faktorene aleine. Når ein kan dette utanatt er det mykje raskare enn [[Polynom aritmetikk#^1d880f|areal modelen]].

Døme:
$f(x)=(x+2)(x+3) \rightarrow$
$\text{første ledd i første faktor} \space x^2+3x$ 
$\space \text{andre ledd i første faktor} \space 2x+6.$
$\space = \underline{x^2+5x+6}$

Døme 2:
$f(x)=(x+2)(x+3)(x+4)$
$f(x)=(x+3)(x^2+7x+12)$
$f(x)= x^3+7x^2+12x+3x^2+21x+36$
$\underline{f(x)=x^3+10x^2+33x+36}$


## Aritmetikk med brøker.
Når vi har ulike polynom-brøker vi skal gjere aritmetikk med må vi har felles nevner som i normal brøk aritmetikk. Då simpelt ganger vi nevnerene med kvarandre og tellerene med dei motsatte nevneren. Som med normal brøk aritmetikk. Viss vi ikkje gjer dette blir det heilt feil!

Eksempel:
$\large \frac{x^2-4}{x+2} + \frac{x-2}{1} \rightarrow \frac{1(x^2-4)}{1(x+2)} + \frac{(x-2)(x+2)}{1(x+2)} \rightarrow \frac{x^2-4+(x-2)(x+2)}{x+2}$

Vi multipliserer slik at vi får felles forhold mellom tallene i brøkene, og deretter setter dei sammen. Må også gjerest når vi skal addere/subtrahere/multiplisere normale tall. Vi må gjere dei til brøker og multiplisere som nemnt over.

## Polynom divisjon.
Polynom divisjon er likt som normale divisjoner/brøker, berre med algebraiske termer i seg. Referer til [[Polynom divisjon]] for å finne ut korleis du kan gjere dette, og kvifor $x\ne-2$ i døme!


Eit døme (Faktorisering metode): 
$\require{cancel} \large \frac{x^2-4}{x+2} = \frac{(x+2)(x-2)}{x+2} \rightarrow \frac{\cancel{(x+2)}(x-2)}{\cancel{(x+2)}}\rightarrow (x-2),\space x \ne -2$
