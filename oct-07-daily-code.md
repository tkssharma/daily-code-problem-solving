
```javascript
const array = [1,2,3,4,56];
const array2= [...array];
const array5 = JSON.parse(JSON.stringify(array));
const array4 = [0,0,3,4,5,6,7];
array4.every(x => x >= 0);

const array1 = [1,2,3,4,5];
const array2 = [1,5,7,8,9];

const complement = (array1, array2) => {
    return (array1 && Array.isArray(array1) && array2 && Array.isArray(array2))
    ? array1.filter((c) => array2.indexOf(c) === -1) : undefined
}

const array = [1,2,3,4,5,6]
const array = [1,2,]
3,4,5,6, 1,2
// left rotation 

numofRotations = 18 % 6 => 0
const leftRotation = (array, rotations) => {
    if(array.length <2){
        return array.slice(0);
    }
    const n = rotations % array.length ;
    if(n === 0) {
      return array.slice(0)
    }
    if(n < 0){
       return array.slice(n).concat(array.slice(0, array.length -1));
    } else {
        return array.slice(n).concat(array.slice(0, n));
    }
}
const rightRotation = (array, k) => {
    const l = array.length;
    return array.splice(l-k).concat(array.slice(0, l-k));
}

const events = [
    { 
      id : "789",
      name: "First Event",
      metadata: {
        type: "public"
      }
    },
    {
        id : "790",
        name: "First Event",
        metadata: {
          type: "public"
        }
    },
    {
        id : "789",
      name: "Event 2",
      metadata: {
        type: "private"
      }
    },
    {
        id : "789",
      name: "Third Event",
      metadata: {
        type: "closed"
      }
    }
  ];

  const newData = events.map( i=> {
      if(i.name ){
          i = {...i, name: "new name"}
      };
      return i;
  }).filter(i => {
      return i.metadata && i.metadata.type === "public";     
  }).sort((a,b) => parseInt(a) - parseInt(b));
  

  const array = [1,2,3,4,5,5,5,56,7,8,9, 56];
  [56,56,56,...]
  const maxCount = array => {
      const array1 = array.sort((a,b) => b-a);
      let max = Math.max(...array1);
      result = 0;

      for(let i=0 ; i <array1.length ; i++){
          if(max === array[i]){
              result ++;
          }
          if(array1[i] < max) break;
      }
      return {
          max,
          result
      }
  }

  const array  = [1,2,3,[4,5,6,[6,7,8,9]]];
                 [1,2,3,[]]
  const deepFlatten1 = arr => [].concat(...arr.map(toFlatten => {
    return (Array.isArray(toFlatten) ? deepFlatten1(toFlatten) : toFlatten)
    }))

  const deepFlatten2 = arr => {
	return arr.reduce((flat, yetToFlatten) => {
		return flat.concat(Array.isArray(yetToFlatten) ? deepFlatten2(yetToFlatten) : yetToFlatten);
	}, []);
}

let myArr1 = [[1], [2], [3, 4], 5]

/* Problem statement 1 - You want to convert an array of decimal numbers into a new array with their hexadecimal equivalents.
 */

var decimalArray = [23, 255, 122, 5, 16, 99];

var hexadecimalArray = decimalArray.map(function(element) {
   return element.toString(16);
});

console.log(hexadecimalArray);

/* Problem statement 2 - You want to filter element values in an array and assign the results to a new array. */

var charSet = ['**','x','a','b'];

var newArray = charSet.filter(function(element) {
    return (element !== "**");
});

 /* Problem Statement 3 - You want to ensure that array contents meet certain criteria. In this case, ensure that every element in the array consists of alphabetical characters */

 const checkMatching = (element, index, array) => {
     var textExpr = /^[a-zA-Z]+$/;
     return textExpr.test(element);
 }
 var elementSet =  ["**",123,"aaa","abc","-",46,"AAA"];
const result = elementSet.every(checkMatching);
const result = elementSet.some(checkMatching);

/* Problem Statement -
Build the function indexOf, for the case when the browser does not support the function natively.
 */

 if(! Array.prototype.indexOf){
     Array.prototype.indexOf = function indexOf(searchElement, startFromIndex){
         if(startFromIndex == null) {
             startFromIndex =0;
         } else if (startFromIndex < 0){
             startFromIndex = Math.max(0, (this.length + startFromIndex));
         }
         for(var i = startFromIndex; i < this.length; i++) {
             if(this[i] === searchElement) {
                 return i;
             }
         }
       return -1;  
     }
 }

 /* Find the intersection of two arrays. Can you do it in O(M+N) time (where M and N are the lengths of the two arrays)?
intersection([1, 5, 4, 2], [8, 91, 4, 1, 3])    // [4, 1]
intersection([1, 5, 4, 2], [7, 12])             // []
*/

// My first attempt at it
arrayIntersection1 = (arr1, arr2) => {
    return arr1.filter(item => {
        return arr2.indexOf(item) !== -1;
    })
}

const arrayIntersection = (arr1, arr2) => {
    let intersection  = [];
    for(let i of arra1) {
        for(let j of arr2) {
            if(i === j) {
                intersection.push(i);
                break;
            }
        }
    }
    return intersection;
}
```
