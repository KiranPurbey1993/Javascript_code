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



# 2)
``````
function flattenStudentDetails(studentDetails) {
  const tStudentDetails = {};

  function flattenObject(obj, parentKey = '') {
    for (const key in obj) {
      const newKey = parentKey ? `${parentKey}_${key}` : key;

      if (typeof obj[key] === 'object') {
        flattenObject(obj[key], newKey);
      } else {
        tStudentDetails[newKey] = obj[key];
      }
    }
  }

  flattenObject(studentDetails);

  return tStudentDetails;
}

const studentDetails = {
  name: 'amit',
  education: {
    school: { name: 'KV', percentage: 72 },
    college: { name: 'IIT', percentage: 65 },
  },
  comments: 'good',
};

const tStudentDetails = flattenStudentDetails(studentDetails);
console.log(tStudentDetails);

==================
{
  name: 'amit',
  education_school_name: 'KV',
  education_school_percentage: 72,
  education_college_name: 'IIT',
  education_college_percentage: 65,
  comments: 'good'
}
===================

```````````
