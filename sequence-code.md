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
#### 2) Factorial
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
