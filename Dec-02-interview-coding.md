## Moving selected items to back of Array 

```
function test(arr, item){
    let count = 0;  
    for(let i =0; i < arr.length ; i ++){
    
          if(arr[i] !== item){
             arr[count++] = arr[i]
          }
          
       }
     while(count < arr.length){
        arr[count++] = item;
    }
      return arr;
    }
  ```  
  ```
    function test(arr, index){
    const x = arr.filter(x => x !== 0);
    const y = arr.filter(x => x === 0);
     return [...x,...y];
    }
  ```
    
 ## Moving all 0s to front of Array 
   ``` 
    const arr = [1,0,1,0,1,0,1,1,1,0,0,0,1];
    
    function test(arr){
        let count = arr.length-1;
        for(let i = arr.length-1 ;  i >= 0; i--){
           if(arr[i] !== 0){
               arr[count--] = arr[i]
           }
        }
        while(count  >= 0){
            arr[count--] = 0;
        }
        return arr;
    }
    console.log(test(arr));
    ```
