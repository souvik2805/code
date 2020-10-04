### Export default (by Obj) : - 

```
function  getEpoach()  {
return  new  Date().getTime();
}
function  greet(firstName,  secondName)  {
return  `Hello ${firstName}  ${secondName} How are you`;
} 
export  default  {
getEpoach:  getEpoach,
greet:  greet
};
````
```
import  React  from  "react";
import  "./styles.css";
import  Utils  from  "./utils/CommonUtils";
export  default  function  App()  {
console.log(Utils.greet("Souvik",  "Biswas"));
let  c  =  <p>Hello</p>;
return  c;
}
```

###  Multiple exports : - 

```
export  function  getEpoach()  {
return  new  Date().getTime();
}
export  function  greet(firstName,  secondName)  {
return  `Hello ${firstName}  ${secondName} How are you`;
}
```
```
import  React  from  "react";
import  "./styles.css";
import  {  greet,  getEpoach  }  from  "./utils/CommonUtils";
export  default  function  App()  {
console.log(greet("Souvik",  "Biswas"));
let  c  =  <p>Hello</p>;
return  c;
}
```
