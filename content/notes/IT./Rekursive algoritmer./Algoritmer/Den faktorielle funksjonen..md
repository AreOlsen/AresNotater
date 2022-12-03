# Den faktorielle funksjonen (n!).

$\LARGE 5!=5\times4\times3\times2\times1$.

Den faktorielle funksjonen viser oss antall ulike moglege arrangementer med $n$ antall elementer.
Vi kan skrive $n!$ som $n\times (n-1)\times(n-2)\times(n-3)……\times 2 \times 1$.

Ein anna bruk for den faktorielle funksjonen er å finne antall ulike måter du kan ta ting frå ein kolleksjon. Antall måter du kan ta $k$ elementer i frå $n$ elementer er som følgende: $\LARGE \frac{n!}{k!\times(n-k)!}$

>[!INFO] Sidenote:
>$0!=1$ og $n!$ er berre definert for positive tall.


Vi har to ulike metoder for åfinne den faktoriele funksjonen:
1. Den iterative metoden
2. Den rekursive metoden.


## Iterative metoden.
Vi går igjennom alle tall ifrå $n$ til $0$ og multipliserer det nåværende tallet, med den totale antallet hittil.

Vi kan skrive ein slik funksjon slik:
```c++
int factorial(int n){
	int value = 1;
	for(int i = n; i >= 2; i++){
		value=value*n;
	}
	return value;
}
```


## Rekursive metoden.

For alle positive verdier av $n$ kan vi skrive $n!$ som $n!=n\times(n-1)!$, ein kan altså finne $n!$ gjennom å finne den faktorielle av lavere verdier, og multiplisere med den høgere verdien.
Her er nokre dømer:
$5!=5\times4!$
$4!=4\times3!$
$3!=3\times2!$
$2!=2\times1!$
$1!=1$

Vi kan dermed skrive ein rekursiv faktoriell funksjon slik:

```js
var factorial = function(n){

	if(n===0||n===1){
		return 1;
	}
	return n*factorial(n-1);
}

```

>[!INFO] Sidenote
>$0!=1$ vi må huske dette når vi skriver den rekursive metoden.
>Derfor har vi òg if(n===0)
