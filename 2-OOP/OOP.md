#### ES5面向对象
```js
function Person(name,age) {
  this.name = name
  this.age = age
  this.sayHi = function() {
    console.log('HI'+this.name);
  }
  Person.prototype.show = function() {
    //
  }
}

var p1 = new Person('blue',12);
p1.show()
p1.sayHi()
```

#### ES6
```js
class Person {
  constructor(name,age){
      this.name = name
      this.age = age 
  }
  show(){}
}

let p1 = new Person('abc',33)
p1.show()
```

- ES6继承
```js
class Worker extends Person{
  constructor(props) {
   super(props);
        this.job = job
  }
  
}
```