
``````````````

let str = "aaaabbbccccaa"; 
// Output: "4a3b4c2a";


function countChar(st){
    let out = "";
    let count = 1;
    
    for(let i=0;i<st.length;i++){
        if(st[i] === st[i+1]){
            count++
        }else{
            out += count+st[i];
            count = 1;
        }
    }
   return out;
}

console.log(countChar(str))


``````````````````````
