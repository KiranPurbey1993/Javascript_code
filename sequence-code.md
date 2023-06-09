#### 1) Fibonacci Sequence
```
function fibonacci(n){
  let fib =   [0,1];
  for(let i=2;i<n;i++){
      fib[i] = fib[i-1] + fib[i-2]
  }
  return fib;
}

console.log(fibonacci(2));
console.log(fibonacci(5));
console.log(fibonacci(7));

```
###### Time Complexity - O(n)
====================================================================

#### 2) nth Fibonacci 
```
function nthFibonacci(n){
 if(n<2) return n;
    return nthFibonacci(n-1) + nthFibonacci(n-2);
}

console.log(nthFibonacci(7))
```
###### Time Complexity - O(2^n)
==========================================

#### 3) Factorial
```
function factorial(n){
  let fac =   1;
  for(let i=1;i<=n;i++){
      fac = fac * i;
  }
  return fac;
}

console.log(factorial(2));
console.log(factorial(3));
console.log(factorial(5));
```
###### Time Complexity - O(n)


```
function factorial(n){
 if(n<2)return 1;
 return n * factorial(n-1);
}

console.log(factorial(4));
```

==================================================================

##### 4) Prime Number
```
function prime(n){
 if(n < 2) return false;
 
 for (let i=2; i<n;i++){
     if(n%i == 0){
         return false;
     }
 }
 return true;
}

console.log(prime(2));
console.log(prime(3));
console.log(prime(5));

```
###### Time Complexity - O(n)
=========================================================

##### 5) Number is Power of 2
```
function isPowerOfTwo(n){
 if(n<1) return false;
 while(n>1){
     if(n%2 !== 0) return false;
     n = n/2;
 }
 return true;
}

console.log(isPowerOfTwo(2));
console.log(isPowerOfTwo(3));
console.log(isPowerOfTwo(8));
```
###### Time Complexity - O(log n)
