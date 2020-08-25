# vanilla javascript tutorial

### 1. getElementBy__
```sh
   let e1 =document.getElementById("demo");
  console.log(e1);
 ```
 ```sh
 var c = document.getElementsByName("name");
console.log(c);
 ```
 ```sh
  var c = document.getElementsByClassName("demo");
   console.log(c);
 ```
  ### 2.querySelectorAll :
   - use css selector for querySelectorAll
   - But it is bit slow
 ```sh
 var c = document.querySelectorAll("input[type=text]");
console.log(c);
 ```
 ### 3. innerHTML
 ```sh
  var c = document.getElementById("name");
  c.innerHTML += "THIS";
  c.innerHTML = "demo";
  c.innerText = "Text";
  c.style.color = "green";
 ```
 
 
 ### 4. CSS
 - add class or remove class or replace
 ```sh
  var c = document.getElementById("name");
  c.classList.add("demo_class");
  c.classList.add("demo_class2");
  c.classList.remove("demo_class2");
  c.classList.replace("demo_class","demo_class3");
 ```
 
### 4. setAttribute
 - predefined attribute like value, src, id etc simple; 
 - But for customatribute we have add it then use
 - **** For HTML specification the name of arribute must be in lowercase, if we want set in uppercase the dom automatically conver in lowercase.
```sh
var c = document.getElementById("name");
c.value = "TTTTTTTTTT";
c.setAttribute("data-test", "123");
console.log(c);
 ```

----- |






