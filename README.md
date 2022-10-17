# 1. Duplicate object entries in array of object

var  arr = [
  {id: 1, name: 'Tom'},
  {id: 4, name: 'Tom'},
  {id: 2, name: 'Nick'},
 
];

var unique = [];

arr.map(k=> unique.filter(a=> 
a.name == k.name).length > 0? null:unique.push(k)
);



// console.log(unique);


# 2. Reverse a string
var string = "Welcome to this Javascript Guide!";

var s = reverseWord(string, "");

var r = reverseWord(string, " ");



function reverseWord(word, separtor){
    return word.split(separtor).reverse().join(separtor)    
}
console.log(s);
console.log(r);




// output = !ediuG tpircsavaJ siht ot emocleW


# 3. Implement enqueue and dequeue using only two stacks
###### Enqueue means to add an element, dequeue to remove an element in same order how it pushed.

# 4 . Implement mul Function

console.log(mul(2)(3)(4)); // output : 24


function mul(a){
    return function(b){
        return function(c){
        return a * b* c;
        }
    }
}

# 5. FizzBuzz Challange

for (var i=1;i<=50;i++){

   let f = i % 3 == 0;
   
   let b = i % 5 == 0;
   
   console.log(f ? (b?'FizzBuzz':'Fizz') : (b?'Buzz':i));
}



// 1
// 2
// Fizz
// 4
// Buzz
// Fizz
// 7
// 8
// Fizz
// Buzz
// 11
// Fizz
// 13
// 14
// FizzBuzz
// 16
// 17
// Fizz
// 19
// Buzz
// Fizz
// 22
// 23
// Fizz
// Buzz
// 26
// Fizz
// 28
// 29
// FizzBuzz
// 31
// 32
// Fizz
// 34
// Buzz
// Fizz37
// 38
// Fizz
// Buzz
// 41
// Fizz
// 43
// 44
// FizzBuzz
// 46
// 47
// Fizz
// 49
// Buzz

# 6. Given two strings, return true if they are anagrams of one another
###### eg - Mary and Army

var st = 'Mary';
var at = 'Army';

function anagrams(st, at){

   let k  = st.toLowerCase().split('').sort().join('');
   
   let p = at.toLowerCase().split('').sort().join('');
   
   if(k == p) {return true;}
}

//console.log(anagrams(st, at));

# 7.Search

###### Linear Search

var a = [5,7,9,10,50,80,85];
var search = 80;


1) var t = a.findIndex(el => el== 81);

console.log(t);



2) let index = a.map(obj => obj).indexOf(search);

console.log(index);

3) var index = null;
for (var i=0; i<a.length; i++) {
    if ( a[i] == 80 ) {
        index = i;
        break;
    }
}

console.log(index);

var t =null;
a.forEach(function(item, index) {
    if(item == search){
     t = index;   
    }
})

console.log(t);

###### Binary Search is a searching algorithm used in a sorted array by repeatedly dividing the search interval in half
###### Binary search, also known as half-interval search
var a = [5,7,9,10,50,80,85];
var search = 80;
1)
var t = a.sort((a, b) => a - b);

// console.log(t);

function binary(t, val){
    let start = 0;
    let end = t.length - 1;
    
    while (start <= end){
        let mid = Math.floor((start + end) / 2);
        
        if(val == t[mid]){
            return mid;
        }
        
        if(val < t[mid]){
            end = mid -1;
        }else{
            start = mid+1;
        }
    }
    return -1;
}


console.log(binary(t, 7));

2) 

function binary(t, search, start = 0, end = t.length - 1){
    let mid = Math.floor((start + end) / 2);
    
    if(search == t[mid]){
        return mid;
    }
    
    return  search < t[mid] ? binary(t, search, start, mid - 1) :
    binary(t, search, mid + 1, end)
}


console.log(binary(t, 10));

# 8. Sort
1) 
var a = [5,7,9,10,50,80,85];

var search = 80;

var t = a.sort((a, b) => a - b);

console.log(t)

2)
let arr = [4, 32, 2, 5, 2,8];

for(var i=0;i<arr.length; i++){
    for (var j=i+1;j<arr.length;j++){
        if(arr[i]> arr[j]){
           let temp = arr[i];
            arr[i]=arr[j];
            arr[j] = temp;
        }
    }
}

console.log(arr);

#### Bubble Sort
###### Bubble Sort only considers one element at a time. Thus, it is highly time consuming and inefficient. Due to its inefficiency, bubble sort is almost never used in production code.
0(n^2).....omega of n square
Iteration 1: [6,4,2,5,7] → [4,6,2,5,7] → [4,2,6,5,7] → [4,2,5,6,7] → [4,2,5,6,7]

Iteration 2:[4,2,5,6,7] → [2,4,5,6,7] → [2,4,5,6,7] → [2,4,5,6,7] → [2,4,5,6,7]

Iteration 3: [2,4,5,6,7] → [2,4,5,6,7] → [2,4,5,6,7] → [2,4,5,6,7] → [2,4,5,6,7]

function bubble(a){
   
   let n = a.length;
   
   for(var i = 0; i<n;i++){
       for (var j=0; j<n;j++){
           if(a[j] > a[j + 1]){
               let tem = a[j];
               a[j] = a[j+1];
               a[j+1] = tem;
               
           }
       }
   }
   return a
}

console.log(bubble(a));

# 9. palindrome
var k = 'nitin';


var t = k.toLowerCase();

var t1 =t.split('').reverse().join('');

console.log(t);
console.log(t1)

return (t == t1)?console.log('true'):console.log('false');

# 10. Output
console.log(1 < 2 < 3);  , because 1<2 ===true ...true< 3 ......true
###### ======true
console.log(3 > 2 > 1);  ====false, because from left to right....3>2 = true...true>1 (1>1====false).....so     
###### ====== false


# 11. How do you add an element at the begining of an array? How do you add one at the end?
var k =['p', 'u'];
1)
 k.unshift('start');
k.push('end');
console.log(k);

2)
var t = ['start', ...k , 'end']      .............spread operator
console.log(t);

# 12. Mul Function
###### The MUL function is a miniature of the multiplication function. In this function, we call the function that required an argument as a first number, and that function calls another function that required another argument and this step goes on. 

function mul(x) {
  return function (y) {
      return x * y ;
    
  };
}

console.log(mul(2)(3));
