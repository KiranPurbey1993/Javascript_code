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

Enqueue means to add an element, dequeue to remove an element.

# 4 . Implement mul Function

console.log(mul(2)(3)(4)); // output : 24


function mul(a){
    return function(b){
        return function(c){
        return a * b* c;
        }
    }
}



