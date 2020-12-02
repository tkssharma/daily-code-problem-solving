## findMajority__
```
function findMajority__(input1, input2) {

       var maxCount = 0;
       var index = -1; // sentinels
       
       for (var i = 0; i < input1; i++) {
           var count = 0;
           for (var j = 0; j < input1; j++) {
               if (input2[i] == input2[j])
                   count++;
           }
 
           if (count > maxCount) {
               maxCount = count;
               index = i;
           }
       }
 
       if (maxCount > input1 / 2)  {
           return input2[index];
       } else {
           return -1;
       }
   }
  ``` 
##  String Compression
```
function getFrequency(string) {
   var freq = {};
   var orderedFreq = {};
   for (var i=0; i<string.length;i++) {
       var character = string.charAt(i);
       if (freq[character]) {
          freq[character]++;
       } else {
          freq[character] = 1;
       }
   }

Object.keys(freq).sort().forEach(function(key) {
orderedFreq[key] = freq[key];
});

var result = '';
Object.keys(orderedFreq).forEach(function(key, index) {
    result = result + key;
    result = result + orderedFreq[key];
});
   return result;
}
```

### String conversion 
```
function snakeToCamel(string) {
      return string.replace(/(_\w)/g, function(m){
          return m[1].toUpperCase();
      });
  }

// Java to C++
function camelToSnake(string) {
  return string.replace(/[\w]([A-Z])/g, function(m) {
      return m[0] + "_" + m[1];
  }).toLowerCase();
}

function isJavaVariable(str) {
return str.indexOf('_') == -1
}

```
   
