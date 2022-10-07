# Duplicate object entries in array of object

var  arr = [
  {id: 1, name: 'Tom'},
  {id: 4, name: 'Tom'},
  {id: 2, name: 'Nick'},
 
];
var unique = [];

arr.map(k=> unique.filter(a=> 
a.name == k.name).length > 0? null:unique.push(k)
);





~console.log(unique);
