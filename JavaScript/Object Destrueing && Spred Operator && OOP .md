
### 1. Object Destrueing


```sh
const address = {
    street:'',
    city:'',
    country:''
};

const street = address.street;
const city = address.city;
const country = address.country;

// Object Destructureing 
const {street, city, country} = address;

// alias take street -> variable st

const {street:st} = address;
```

### 2.  Spred Operator
```sh

const first = [1,2,3];
const second = [4,5,6];
const combined = first.concat(second);
const combined2 = [...first,'a',...second,'b'];

const clone = [...first];
const ref = first;
console.log(first);
console.log(clone);
console.log(ref);

const fs = {name:"souvik"};
const sc = {job:"alumnux"};

const com = {...fs, ...sc, location:"Kolkata"};
console.log(com);
```

### 3.  Class, OOP
3. Class, OOP :- When we have Object at Least one Method , we need blueprint of the Obhect of that Type
 That's why we uses Classes

```sh
 const person = {
     name:"Souvik",
     walk(){
         console.log("Walk");
     }
    }
    
    
class Person{
    constructor(name){
     this.name = name;
    }
    walk(){
        console.log("Walk");
    }  
 }

 const person = new Person('Souvik');
```

  


