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
 
 # 2. Find the frequency of a number in an array
 (occurance of number)
 const numberArray = [1,2,5,8,5,6, 5];
 number is 5
 /// output : 3
 
 function findOccurance(array, num){
 let counter = 0;
 arry.forEach((a)=>{
 if(a == x){
 counter ++
 }
 });
 return counter;
 }
 
  console.log(ffindOccurance(numberArray, number));
  ======================================================
  
  let t = numberArray.filter((e)=>e== x);
  console.log(t.length)
  
  
  ### if multiple occurances then use hash/objects
  const arr = [0, 5, 4, 5, 4, 5];
var x = 5;

function occurance(arr, number){
   let t = arr.reduce((accumulator, curr)=>{
      if(curr in accumulator){
          accumulator[curr]++;
      } else{
         accumulator[curr] = 1 
      }
      return accumulator;
   },{});
   return t;
}
 

let y = occurance(arr, x);
console.log(y)
 
 
