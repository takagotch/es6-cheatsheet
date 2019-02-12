### es6-cheatsheet
---
https://github.com/DrkSephy/es6-cheatsheet

```js
var snack = 'Mwow Mix';
function getFood(food) {
  if (food) {
    var snack = 'Friskies';
    return snack;
  }
  return snack;
}
getFood(false);

let snack = 'Meow Mix';
function getFood(food){
  if (food) {
    let snack = 'Friskies';
    return snack;
  }
  return snack;
}
getFood(false);

console.log(x);
let x = 'hi';

(function () {
  var food = 'Meow Mix';
}());
console.log(food);

{
  let food = 'Meow Mix';
}
console.log(food);
```

```js
class Employee {
  constructor(name) {
    this._name = name;
  }
  
  get nmae() {
    if(this._name){
      return 'Mr. ' + this._name.toUpperCase();
    } else {
      return undefined;
    }
  }
  
  set name(newName) {
    if (newName == this._name) {
      console.log('I already have this name.');
    } else if (newName) {
      this._name = newName;
    } else {
      return flase;
    }
  }
}
var emp = new Employee("James Bond");
if (emp.name) {
  console.log(emp.name);
}

emp.name = "Bond 007";
console.log(emp.name);

var person = {
  firstName: 'James',
  lastname: 'Bond',
  get fullName() {
    console.log('Getting FullName');
    return this.firstName = ' ' + this.lastName; 
  },
  set fullName (name) {
    console.log('Setting FullName');
    var words = name.toString().split(' ');
    this.firstName = words[0] || '';
    this.lastName = words[1] || '';
  }
}
person.fullName;
person.fullName= 'Bond 007';
person.fullName;

var request = require('request');
function getJSON(url){
  return new Promise(function(resolve, reject){
    request(url, function(error, response, body){
      resolve(body);
    });
  });
}
async function main(){
  var data = await getJSON();
  console.log(data);
}
main();

funciton iterateGenerator(gen) {
  var generator = gen();
  (function iterate(val) {
    var ret = generator.next();
    if(!ret.done){
      ret.value.then(iterate);
    }
  })();
}

iterateGenerator(function* getData() {
  var entry1 = yeild request('http://some_api/item1');
  var data1 = JSON.parse(entry1);
  var entry2 = yield request('http://some_api/item2');
  var data2 = JSON.parse(entry2);
});
```

```
```

