
##  mobx
   
  npm install -E mobx
"mobx": "5.15.7",

npm install  mobx
"mobx": "^5.15.7",

-E : Exact Version

-----------------------------

npm i --save-dev @babel/plugin-proposal-class-properties @babel/plugin-proposal-decorators

"devDependencies": {
	"@babel/plugin-proposal-class-properties": "^7.10.4",
	"@babel/plugin-proposal-decorators": "^7.10.5"
}

-

**Set up 1**
```
>> npx create-react-app mymobx-1
	
>> npm install -E mobx /
>> npm install mobx
>> npm install mobx-ract


>> npm i --save-dev @babel/plugin-proposal-class-properties @babel/plugin-proposal-decorators

>> npm run eject
```

**Set up 2**
Goto package.json file and find babel(at bottom of the file)

	"babel": {
		"presets": [
		"react-app"
		]
	}

change it to

	"babel": {
		"plugins": [
		["@babel/plugin-proposal-decorators", { "legacy": true }],
		["@babel/plugin-proposal-class-properties", { "loose": true }]
		],
		"presets": [
		"react-app"
		]
	}

-   [How to use decorators](https://mobx.js.org/best/decorators.html)
-    [2.How to use decorators](https://babeljs.io/docs/en/babel-plugin-proposal-decorators)

**Set up  1&2  implement**

![Image](https://raw.githubusercontent.com/souvik2805/code/master/assest/Capture.PNG)

So far progess 


```
import { observable, autorun, action } from  "mobx";

class  ShoppingCart {
	@observable
	items  = [];

	@action
	add(item) {
	this.items.push(item);
	}
}

const  mycart  =  new  ShoppingCart();
autorun(() => {
console.log(mycart.items.length);
console.log(mycart.items.map((cart) =>  cart.name));
});

  

mycart.add({ name: "computer", price: 200 });
mycart.add({ name: "computer2", price: 200 });
```


##### showing  wrong  syntax for mobx  ide  in 
1. add  `tsconfig.json` file.
2. in file add this code
```
{
	"compilerOptions": {
	"experimentalDecorators": true,
	"allowJs": true
	}
}
```

