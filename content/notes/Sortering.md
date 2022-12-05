# Sortering

Å sortere ein liste av elementer kan hjelpe datamaskinen eller evt. mennesker til å finne elementer på den listen. Til dømes ved binary search!

Javascript og andre programmeringspråk har oftast raske innebygde sorteringsmetoder, men det er godt å forstå korleis sortertingsalgoritmer fungerer slik at ein forstår korleis ein kan angrepe samme algoritme problemstilling på fleire ulike måter. 

Alle sortertingsalgoirtmer er basert på ein type funksjon som swapper to elementer i ein liste. I javascript kan ein slik funksjon blir implementert slik:
```javascript
var swap(array,firstIndex,secondIndex){
	var temp = array[firstIndex];
	array[firstIndex]=array[secondIndex];
	array[secondIndex]=temp;
	return array;
};
```

To dømer på sortertingsalgoritmer er [[Insertion sort.]] og [[Selection sort.]]