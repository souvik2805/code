
### Every function in Js is Object


```sh
const person = {
    name: "Sovuik",
    walk(){
        console.log(this);
    }
};
```
```sh
var foo = person.walk;
foo();
```

 . Here preson.walk is an Object(Window)
 As in Javascript Function are Object
 So here pereson.walk is acutally is an Object

**** To overcome this Problem we use bind(). 
```sh
 var foo2 = person.walk.bind(person);
foo2();
```

  Now  foo2 -> this point on the Person.


