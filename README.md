# task-4
how to compare two json have the same properties without order    a. let obj1={name: "person 1", age:5};    b. let obj2 ={ age:5,name: "person1"};


let obj1 = {name: "person 1", age: 5};
let obj2 = {age: 5, name: "person 1"};

let sortedObj1 = JSON.stringify(obj1, Object.keys(obj1).sort());
let sortedObj2 = JSON.stringify(obj2, Object.keys(obj2).sort());

if (sortedObj1 === sortedObj2) {
  console.log("The JSON objects are the same.");
} else {
  console.log("The JSON objects are different.");
}
