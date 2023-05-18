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
 
  console.log(findOccurance(numberArray, number));
  
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

# 3) Group by property
const t = [
    {name: "Kiran", age:30},
    {name: "Ritesh", age:30},
    {name: "Kiran", age:28},
    {name: "Babu", age:26}
    
    ];
    
    function grpByProperty(arr, property){
       let u = arr.reduce((acc, cur)=>{
           let y = cur[property];
           if(!acc[y]){
               acc[y] = [];
           }
          
            acc[y].push(cur);
           
           return acc;
       },{}) ;
       return u;
    }
    
    console.log(grpByProperty(t, 'name'));
    
    =================================
    
    const t = [
    {name: "Kiran", age:30},
    {name: "Ritesh", age:30},
    {name: "Kiran", age:28},
    {name: "Babu", age:26}
    
    ];
    
    function grpByProperty(arr, property){
        let grpArr = {};
        arr.forEach(a=>{
            if(!grpArr[a[property]]){
              grpArr[a[property]]  = [a]
            }else{
                grpArr[a[property]].push(a); 
            }
        });
        return grpArr;
    }
    
   console.log(grpByProperty(t, 'age'));
   
   # 4) Program to check a string with balanced brackets.
   
   isValid=(s)=>{
    let map = {
        "]":"[",
        ")":"(",
        "}":"{"
    }
   let stack = [];
   
   for(let i=0; i<s.length;i++){
       if(s[i] == "[" || s[i] == "(" || s[i] == "{"  ){
           stack.push(s[i]);
       }else if(stack[stack.length -1] === map[s[i]]){
           stack.pop();
       }else return false;
   }
    
  return stack.length ? false:true;  
}

const t ="{[(])}";
console.log(isValid(t));
   
 
 
 # 5)Find the pairs of array element for which sum is equal to given target value (Two Sum Problem)
 
     function printpairs(arr, sum)
    {
        for (let i = 0; i < arr.length -1; ++i)
        {
           for(let j = (i+1);j< arr.length;j++){
               if(arr[i] + arr[j] == sum){
                console.log(arr[i], arr[j]);
                  return true;
               }
              
           }
        }
         return false;
    }
    
    let A = [ 0, -1, 2, -3, 1];
        let x = -2;
        let size = A.length;
        
        console.log(printpairs(A, x));
        
        
        =========================if multiple=============
        
        
   function printpairs(arr, sum)
    {
        let s ={};
        let sum1 =[];
        for (let i = 0; i < arr.length; ++i)
        {
            let temp = sum - arr[i];
 
            // checking for condition
         
            if (s[temp.toString()] !== undefined) {
                sum1.push([arr[i], temp]);
            }
            
            s[arr[i].toString()] = arr[i];
              console.log(s);
        }
        return sum1;
    }
    
    let A = [ 0, -1, 2, -3, 1 , -4];
        let x = -2;
        let size = A.length;
        
        console.log(printpairs(A, x));
        
        
   # 5) Find the missing number from unsorted array with O(n) complexity
   
   function findMissing(arr,n){
      let total = Math.floor((n+1)*(n+2)/2);

     for(let i=0;i< n;i++){
         total = total - arr[i];
     }
     console.log(total);
     return total;
   }
   
   let arr = [ 1, 3,  2 ];
        let n = arr.length;
 
        // Function call
       findMissing(arr,n);
 # 6)  Find the missing number from sorted array with O(n) complexity
 function findMissing(arr,n){
let miss = [];
for(var i=0;i< n;i++){
        if((arr[i + 1] - arr[i] !== 1) && arr[i+1] != undefined){
           miss.push(arr[i] + 1) 
        }
}
console.log(miss)
return miss;
}

let arr = [ 1, 2,3,5,7, 9,11];
        let n = arr.length;
 
        // Function call
       findMissing(arr,n);
