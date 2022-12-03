# Determining if a word is a palindrome with recursion.

A palindrome is a word that is written the same way forwards and backwards.
For example: "ROTOR" is a palindrome, but "MOTOR" is not.

How can we use [[Rekurisve algoritmer.|recursion]] to determine a palindrome? We first need to understand what the base case would be. Consider the word $a$, or character sequence $a$ (it does not have to be a word). Any string containing just one letter is a palindrome, and likewise an emptry string is a palindrome. Our basecase would be: if a string is exactly $0$ or $1$ is length then the string is a palindrome.

If the string contains two or more characters we need to have our recursive case. Consider the palindrome "ROTOR", the first and last letters are the same. If they are not the same, such as in "MOTOR", the word is not a palindrome. This can be used to differentiate between if a string is a palindrome or not. 
If the first and last characters are the same it might be a palindrome, then we have to check the second first and second last characters, ……… , until we have checked the whole string. We can just check the last and first characters then pop the letters and check the string again, until the string is length of either $1$ or $0$.
If we ever encounter a difference in the first and last letters then we know for certain it not a palindrome.

## Psuedocode.
1. So to check recursively if a string is a palindrome we check the first and last characters.
1.  If they are the same, strip them from the string, and check if the new last and first characters are the same.
	1. Repeat until string is length $0$ or $1$.
2. If the first characters are not the same, stop and declare that the word is not a palindrome.


We can implement this in javascript like this:
```js
var palindrome = function(string){
	//basecase 1
	if(string.length===0||string.length===1){
		return true;
	}
	//basecase 2
	if(lastcharacter(string)!==firstcharacter(string)){
		return false;
	}
	//basecase 3
	return plaindrome(middlecharacters(string));
};

```
