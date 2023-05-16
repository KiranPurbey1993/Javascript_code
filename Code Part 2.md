 # 1. Find the index of  peak element in the array
const numberArray = [1,2,5,8,45,6];
 // output is 45
 
 function findPeak(a, n){
   if(n == 1) return 0;
   if(a[0] >= a[1] ) return 0;
   if(a[n-1] >= a[n-2]) return n-1;
   
   for(let i = 1; i< n-1; i++){
    if((a[i] >= a[i-1]) && (a[i] >= a[i+1])) return i;
   }
 }
 
 console.log(findPeak(numberArray, numberArray.length));
 
