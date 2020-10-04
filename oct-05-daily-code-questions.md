// String Reverse many different ways 

```javascript
const mapOfString = str => {
    const map ={};
    str.split("").forEach(i => map[i] = map[i] ? map[i] + 1: 1);
    return map;
}
mapOfString("helloworld")


const removeDuplicates = str.split("").filter((i, index, array) => {
       return array.indexOf(i) === index
});
```

```javascript
const str ="Helloworld";
const array = [1,2,3,4,1,2,3,4];
const removedups = [...new Set(str.split(""))].join("")
const removeDuplicates = str.split("").filter((i, index, array) => {
    return array.indexOf(i) === index
});
```


```javascript
// reverse a string 
str.split("").reverse().join("")
const reverseString = str => {
    return str? reverseString(str.substr(1)) + str[0] : str;
}
const reverseString = str => {
    return str.split("").reduce((r, c) => c + r, "");
}
```

```javascript
const reverse = str => {
   let out= "";
   "hello"
   // h 
   // e + "h"
   // l + "eh"
   for(const c of str){
       out = c + out;
   }
   return out;
}
```


```javascript
const removeDuplicates = (str, char) => {
    return str.split("").filter(i => {
        return i !== char
    }).join("");
} 
// How to find the maximum occurring character in given String? (solution) DONE

const mapOfString = str => {
    const map ={};
    str.split("").forEach(i => map[i] = map[i] ? map[i] + 1: 1);
    return map;
}
```

```javascript
const maximumOccurringCharacter = (str) => {
    const obj = mapOfString(str);
    maxChar = str.split("")[0];
    maxVal = 1
    for(let i in obj){
       if(obj[i] > maxVal) {
        maxChar = i
        maxVal = obj[i]
       }  
    }
    return maxChar;
}
```

/*
How can a given string be reversed using recursion? (solution)
How do you check if a string contains only digits? (solution)
How do you find duplicate characters in a given string? (solution)
How do you count a number of vowels and consonants in a given string? (solution)
How do you count the occurrence of a given character in a string? (solution)
How do you print the first non-repeated character from a string? (solution)
How do you reverse words in a given sentence without using any library method? (solution)
How do you check if two strings are a rotation of each other? (solution)
How do you check if a given string is a palindrome? (solution)
How do you find the length of the longest substring without repeating characters? (solution)
How do you find all the permutations of a string? (solution)
*/

```javascript
const StringContainsDigit = (str, char) => {
    let count = 0;
    for(let c of str) {
        if(c === char){
          count ++;
        }
    }
    return count;
}
```

```javascript
const StringContainsDigit = str => {
    for(let c of str) {
        if(isNaN(c)){
            return false;
        }
    }
    return true;
}
const mapOfString = str => {
    const map ={};
    str.split("").forEach(i => map[i] = map[i] ? map[i] + 1: 1);
    return map;
}
```

```javascript
const getCharFirstRepeated = str => {
    const obj = mapOfString(str);
    for(let i in obj){
        if(obj[i] === 1){
            return i;
        }
    }
}
```

// How do you reverse words in a given sentence without using any library method? (solution)
// How do you check if two strings are a rotation of each other? (solution)


```javascript
const isRotation = (str1, str2) => {
    const tmp = str1 + str1;
    return tmp.includes(str2);
}
```

 -  How do you find the length of the longest substring without repeating characters? (solution)
 - How do you find all the permutations of a string? (solution)


```javascript
const findPermutations = string => {
    // "ABC"
    if(string.length < 2){
        return string;
    }
    let permutationsArray = [];
    for(let i =0; i < string.length ; i++){
        let char = string[i];
        let remainingChar = string.slice(0,i) + string.slice(i+1, string.length);
        for(let permutation of findPermutations(remainingChar)) {
            permutationsArray.push(char + permutation);
        }
    }
    return permutationsArray;
}
```javascript


```javascript
const stringPermutations = str => {
    // AB => AB, BA
    if (str.length <= 2) return str.length === 2 ? [str, str[1] + str[0]] : [str];
    return str
      .split('')
      .reduce(
        (acc, letter, i) =>
          acc.concat(stringPermutations(str.slice(0, i) + str.slice(i + 1)).map(val => letter + val)),
        []
      );
  };
```
 

 - How do you find the missing number in a given integer array of 1 to 100? (solution)
 - How do you find the duplicate number on a given integer array? (solution)
 - How do you find the largest and smallest number in an unsorted integer array? (solution)
 - How do you find all pairs of an integer array whose sum is equal to a given number? (solution)

```javascript
// find the missing number in a given integer array of 1 to 100
[1,2,3,5,6], 5 => 21 => //4 
// => 1.2.3.4.5 => n*(n+1)/2
// [1,2,3,4,5,6] => 6*7/2 => 21

const getMissing = (array, n) => {
    const total = (n+1)*(n+2)/2;
   for(let i =0 ; i< n ; i++) {
       total -=a[i]; 
   }
   return total;
}


const mapOfString = array => {
    const map ={};
    array.forEach(i => map[i] = map[i] ? map[i] + 1: 1);
    return map;
}

const getMinMax =(array) => {
    let min = array[0];
    let max = array[0];
    for(let i=0 ; i< array.length; i++ ){
        if(max > array[i]){
            max = array[i]
        }
        if(min < array[i]){
            min = array[i]
        }
    }
    return {
        max, min
    }
}
```
```javascript

// [1,2,3,4,5,6] => 6
// [[2,4], [1,5]]

const getPairsCount = (array, sum) => {
    let count = 0; // Initialize result 
    let pairs = [];
  // Consider all possible pairs and check their sums 
  for (let i=0; i<n; i++) {
        for (let j=i+1; j<n; j++) {
            if (arr[i]+arr[j] === sum) {
                count++; 
                pairs.push([array[i], array[j]])
            }
        }
  }    
    return {
        count,
        pairs
    } 
}
```

 - How do you find the largest and smallest number in an unsorted integer array? (solution)
 - How do you find all pairs of an integer array whose sum is equal to a given number? (solution)
 - How do you find duplicate numbers in an array if it contains multiple duplicates? (solution)
 - How to remove duplicates from a given array in Java? (solution)
 - How do you search a target value in a rotated array? (solution)
 - Given an unsorted array of integers, find the length of the longest consecutive elements sequence? (solution)
 - How is an integer array sorted in place using the quicksort algorithm? (solution)
 - How do you remove duplicates from an array in place? (solution)
 - How  do you reverse an array in place in Java? (solution)
 - How are duplicates removed from an array without using any library? (solution)
 - How to convert a byte array to String? (solution)
 - What is the difference between an array and a linked list? (answer)
 - How do you perform a binary search in a given array? (solution)

```javascript
const getMinMax =(array) => {
    let min = array[0];
    let max = array[0];
    for(let i=0 ; i< array.length; i++ ){
        if(max > array[i]){
            max = array[i]
        }
        if(min < array[i]){
            min = array[i]
        }
    }
    return {
        max, min
    }
}
```

```javascript
const removeDuplicates = array.filter((i, index, array) => {
    return array.indexOf(i) === index
});

const sortNumbers = array.sort((a,b) => a-b);

const array = [1,2,3,1,2,3,4,51,2,34];
const removeduplicated = (array) => {
    const map = {};
    const out =[];
    for(let i of array) {
        if(!map[array[i]]){
            map[array[i]] = true;
            out.push(array[i])
        }
    }
    return out;
}
```

 - Find pair with given sum in the array
 - Find sub-array with 0 sum
 - Find maximum length sub-array having given sum
 - Find maximum length sub-array having equal number of 0’s and 1’s
 - Sort an array containing 0’s, 1’s and 2’s(Dutch national flag problem)
 - Inplace merge two sorted arrays
 - Merge two arrays by satisfying given constraints
 - Find index of 0 to replaced to get maximum length sequence of continuous ones
 - Find maximum product of two integers in an array

