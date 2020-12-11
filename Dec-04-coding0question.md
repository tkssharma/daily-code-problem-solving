let arr = [1,2,3,3,5,1]

function getsubSethavingSum(arr, k){
    const pairs = [];
    for(let i=0 ; i< arr.length ; i++){
        let sum = arr[i] //2
        console.log('i' + arr[i]);
        for(let j = i+1; j < arr.length; j++){
            sum = sum + arr[j] // 5
            console.log('j' + arr[j]);
            if(sum === k){
                pairs.push({startIndex: i, endIndex: j});
            }
        }
    }
    return pairs;
}

console.log(getsubSethavingSum(arr, 6));
