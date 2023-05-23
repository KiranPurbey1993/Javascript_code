# 1)
```
const A = {
    "a":{
        "b":{
            "c":[]
            },
        "d":{},
    },
    "e":"e",
    "f":"nill",
    "g":-2
}
// expected = [ 'a.b.c', 'a.d', 'e', 'f', 'g' ];
let output = [];

function grp(input, z){
   
  for([key, value] of Object.entries(input)){
      if(z.length > 0) key= z +'.'+key;
       
      if(typeof(value) == 'object' && Object.entries(value).length > 0){
         grp(value, key)  ;
         
      }else{
        output.push(key);
         
      }
       
  }
  return output;
}

console.log(grp(A, ''));
```
