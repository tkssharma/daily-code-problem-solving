### Here is my list of some of the frequently asked string coding questions from programming job interviews:

- How do you reverse a given string in place? (solution)
- How do you print duplicate characters from a string? (solution)
- How do you check if two strings are anagrams of each other? (solution)
- How do you find all the permutations of a string? (solution)
- How can a given string be reversed using recursion? (solution)
- How do you check if a string contains only digits? (solution)
- How do you find duplicate characters in a given string? (solution)
- How do you count a number of vowels and consonants in a given string? (solution)
- How do you count the occurrence of a given character in a string? (solution)
- How do you print the first non-repeated character from a string? (solution)
- How do you convert a given String into int like the atoi()? (solution)
- How do you reverse words in a given sentence without using any library method? (solution)
- How do you check if two strings are a rotation of each other? (solution)
- How do you check if a given string is a palindrome? (solution)
- How do you find the length of the longest substring without repeating characters? (solution)
Given string str, - How do you find the longest palindromic substring in str? (solution)
- How to convert a byte array to String? (solution)
- How to remove the duplicate character from String? (solution)
- How to find the maximum occurring character in given String? (solution)
- How do you remove a given character from String? (solution)

Most Common Solutions 

```javascript
// lot of things can be solvd by just gettig map of a string characters
const map ={};
const string = "Hello World";
const array = string.split("");
array.forEach(i => map[i] ? map[i] = map[i] + 1 : map[i] = 1);
console.log(map)
```


```javascript
// lot of things can be solvd by just gettig map of a string characters
const string = "hello world";
const removeDups = [... new Set(string.split(""))].join("")
```

```javascript
// Remove char from String
const removeChar = (string, char) {
    return string.split("").filter(i => i !== char).join("");
}
```


