# react

## ES6 Javascript used in react

let keyword is just like var
const keyword is a const that should not change after its definition

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
