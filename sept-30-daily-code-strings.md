
 - How do you find the missing number in a given integer array of 1 to 100? (solution)
 - How do you find the duplicate number on a given integer array? (solution)
 - How do you find the largest and smallest number in an unsorted integer array? (solution)
 - How do you find all pairs of an integer array whose sum is equal to a given number? (solution)
 - How do you find duplicate numbers in an array if it contains multiple duplicates? (solution)
 - How to remove duplicates from a given array in Java? (solution)
 - How do you search a target value in a rotated array? (solution)
 - Given an unsorted array of integers, find the length of the longest consecutive elements sequence? (solution)
 - How is an integer array sorted in place using the quicksort algorithm? (solution)
 - How do you remove duplicates from an array in place? (solution)
 - How do you reverse an array in place in Java? (solution)
 - How are duplicates removed from an array without using any library? (solution)
 - How to convert a byte array to String? (solution)
 - What is the difference between an array and a linked list? (answer)
 - How do you perform a binary search in a given array? (solution)
 - How to find a median of two sorts arrays? (solution)
 - How to rotate an array left and right by a given number K? (solution)
 - How do you find duplicates from an unsorted array? (solution)
 - Given an array of integers sorted in ascending order, find the starting and ending position of a given value? (solution)
 - Given an integer array, find the contiguous subarray (containing at least one number) which has the largest sum and return its sum? (solution)


 - How do you find the largest and smallest number in an unsorted integer array? (solution)
```javascript
const getMinMax = (array) => {
    let min = array[0]
    let max = array[0]
    for(let k of array) {
        if(k > max) {
            max = k
        }
        if(k < min) {
            min = k
        }
    }
    return {max, min};

} 
```

 - How do you find all pairs of an integer array whose sum is equal to a given number? (solution)
```javascript
function getPairsCount(arra, n, sum) { 
  let count = 0; // Initialize result 
  // Consider all possible pairs and check their sums 
  for (let i=0; i<n; i++) 
        for (let j=i+1; j<n; j++) 
            if (arr[i]+arr[j] == sum) 
                count++; 
    return count; 
}
function twoSum(arr, S) {
 const sum = [];
  for(let i = 0; i< arr.length; i++) {
    for(let j = i+1;  j < arr.length; j++) {
      if(S == arr[i] + arr[j]) sum.push([arr[i],arr[j]])
    }
  }
 return sum
}

```