# react

## ES6 Javascript used in react

###Keywords

let keyword is just like var
const keyword is a const that should not change after its definition

###arrow functions

####Conventional JS function
```
var func = function() {
  ...
 }
```
or
```
function func (){
  ...
}
```
####Arrow functions 
```
Example 1
const func = () =>{
  ...
}
Example 2 - For single argument we can ommit the ()
const func = name =>{
  console.log(name);
}
func();
Example 3 
const multiply = number =>{
  return number * 2;
}
console.log(multiply(2));
Example 4 - give the same result at Example 3. Basically for a single return function we can write it this way.
const multiply = number => number * 2;
console.log(multiply(2));
```

## Simple React function

``` 
<div class="person">
  <h1>Hello TK
  </h1>
  <h2>
    Age: 28
  </h2>
</div>
<div id="p1"></div>
<div id="p2"></div>
<div id="p3"></div>

<div id="app"></div>

```
```
// static react component
function Person(){
  return(
    <div class="person">
      <h1>
        Hello Kenny
      </h1>
      <h2>
        Age: 27
      </h2>
    </div>
  );  
}
//use ReactDOM to render a JS function as a some sort of a "HTML Element" and points to where to render it.
ReactDOM.render(<Person/>,document.querySelector("#p1"));

//dynamic react component
  //props basically enables a property to be passed into the Person   function hence allow us to create react component with dynamic       values
function DynamicPerson(props){
  return(
    <div class="person">
      <h1>
        Hello {props.name}
      </h1>
      <h2>
        Age: {props.age}
      </h2>
    </div>
  );  
}

ReactDOM.render(<DynamicPerson name="Tim" age="40"/>,document.querySelector("#p2")); 
ReactDOM.render(<DynamicPerson name="ah gong" age="99"/>,document.querySelector("#p3")); 

//Better way of writing ReactDOM
var app =(
  <div>
    <DynamicPerson name="ah ma" age="98"/>
    <DynamicPerson name="sot" age="56"/>
  </div>
);

ReactDOM.render(app,document.querySelector("#app"));
```
