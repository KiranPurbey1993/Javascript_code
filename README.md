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

# 7. Binary Search
###### Binary Search is a searching algorithm used in a sorted array by repeatedly dividing the search interval in half
###### Binary search, also known as half-interval search




