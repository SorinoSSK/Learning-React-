# Learning React
This repositories contains learning guide for me to pick up the skill in coding react as it differs from conventional web based coding. References of the content could be found at the very end of this repository.
## Installation
React is a front-end library that uses javascript on a NodeJS framework rather than a language itself. Therefore, user should install NodeJS before installing React.
#### a) Install Node.js
Install NodeJS first from ```https://nodejs.org/en/download/```.
#### b) Open up Node.js command prompt
After install NodeJS, open up ```Node.js command prompt``` to begin install React library.
#### c) Install react
In the ```Node.js command prompt```, type the following command, ```npm install -g create-react-app``` to install React.

## Creation of React project
The creation of a React project have to be done manually on the ```Node.js command prompt``` before we begin coding.
#### a) Open up Node.js command prompt
Open up ```Node.js command prompt``` to create a React project.
#### b) Change directory to intended directory
Use the command ```cd ...``` to change to the directory you intend to store the newly created React project. This directory is not the React project directory itself.
#### c) Create a project 
Within the directory, type the following command, ```create-react-app (project-name)``` to create the React project.
**Notes**
- Do not use caps for project name, an error will be shown instead.
- (project-name) is a unique name to be given to the React project.

## Executing React project
React project will be compiled and executed from the command prompt.
#### a) Open up Node.js command prompt
Open up ```Node.js command prompt``` to run a React project.
#### b) Change directory to intended directory
Use the command ```cd ...``` to change to the directory of your React project (In the React project directory and not the directory that stores your React project).
#### c) Execute the React file
To execute the React project, type the following command, ```npm start```. The React project will be compiled and executed. A webpage will appear on a new tab or browser have it has completed compiling.

## Editing of NodeJS program
The coding of the program can be done using ```Visual Studio code```.

## Online Editor
An online editor such as ```https://codepen.io``` can be used to implement and test your code. However, you have to modify certain settings before it can be used to compile React program. The follow steps will guide you in the modification of ```https://codepen.io``` settings.
#### a) Open pen settings
```Open JS Settings```
#### b) Set preprocessor to Babel
Select ```Bebel``` under ```JavaScript Preprocessor``` setting.
#### c) Add externel scripts to run react libraries
Add the following URL, under ```Add resource text box``` within the```Add External Scripts/Pens``` setting.
1) ```https://unpkg.com/react/umd/react.development.js```  
2) ```https://unpkg.com/react-dom/umd/react-dom.development.js```

## Installing libraries
...
#### a) Open up Node.js command prompt
Open up ```Node.js command prompt``` to install libraries.
#### b) Install your intended library
In this example, the command will install react router that is DOM specific.  
Use the command ```npm -i react-router-dom``` to change to install react router.

## Ideology/Terminology behind React
React has some additional terminology and a different code implementation from convention thus this section will highlight a few of them.
#### 1) Structure of React
Unlike conventional web application or application programming, React consist of 3 basic folders which are generated after executing ```Creation of React project```. The 3 basic folders are
1) node-modules
2) public
3) src
#### 2) Primary file of React or the frontend of the webpage
Similar to many web based application, the main page that will be displayed is ```index.html```.  
The file can be found in ```public -> index.html```.
#### 3) Primary backend file of React
```App.js``` is the primary backend file that will be rendered (fed into variables) in ```index.html```
The file can be found in ```src -> App.js``` and it usually consist of functionality components such as buttons, and variables of front end.
#### 4) Linking both frontend and backend of React project
```index.js``` is the file that provides the linkage between ```index.html``` and ```App.js```
The file can be found in ```src -> index.js```. The idea of this structure is similar to flask framework.
#### 5) Rendering
Rendering is a term used to feed values from the backend to the variables declared at the front end. There are 2 ways to implement rendering and the code will be implemented within ```index.js```.  
a) ReactDOM.render(Variable, ID)
This line of code can be used in the following way, ```ReactDOM.render((Var), document.getElementById('testID'));```  
Where ```(Var)``` is any variable or HTML code you intend to feed to ```testID``` in the frontend.  
b) ReactDOM.createRoot(ID)
This line of code have a different implementation than ```a)```, but they works the same way. It can be implemented in the following way,  
```
const root = ReactDOM.createRoot(document.getElementById('test'));  
root.render(<React.StrictMode>Whatever you want to do here.</React.StrictMode>)
```  
Where ```test``` is the variable implemented at the frontend and ```Whatever you want to do here.``` is the same as ```(Var)```
#### 6) Components and Props
Rather than calling it functions, classes, parent, and child, React have a different terminology for reusing code.  
<ins>**Components**</ins>  
Components is similar to a function which allows a chunk of code to be reused. An example can be seen below.
```
class ShoppingList extends React.Component  
{  
    render()  
    {
        return
        {
            <div className = "shopping-list">
              <h1>Shopping List for {this.props.name}</h1>
              <ul>
                <li>Instagram</li>
                <li>WhatsApp</li>
                <li>Oculus</li>
              <ul>
            </div>
        }
    }
}
```
In this instance, ```ShoppingList`` is a **React component class** or **React component type**, and that **render()** method returns a chunk of code to be displayed on screen.
**The above html code is also equivalent to the following code.**
```
return React.createElement
(
  'div', {className: 'shopping-list'},
  React.createElement('h1', /* ... h1 children ... */),
  React.createElement('ul', /* ... ul children ... */)
);
```
<ins>**Props**</ins>  
Props is a subset of a component where a component is the parent class and props is a child class.
To obtain the index of the prop, you can use ```this.props.value``` to pass the child ID of the prop from the component. The following code is an example on how ```this.props.value``` can be used.
```
class Square extends React.Component {
  render() {
    return (
      <button className="square">
        {this.props.value}
      </button>
    );
  }
}

class Board extends React.Component {
  renderSquare(i) {
    return <Square value={i} />;
  }

  render() {
    const status = 'Next player: X';

    return (
      <div>
        <div className="status">{status}</div>
        <div className="board-row">
          {this.renderSquare(0)}
          {this.renderSquare(1)}
          {this.renderSquare(2)}
        </div>
        <div className="board-row">
          {this.renderSquare(3)}
          {this.renderSquare(4)}
          {this.renderSquare(5)}
        </div>
        <div className="board-row">
          {this.renderSquare(6)}
          {this.renderSquare(7)}
          {this.renderSquare(8)}
        </div>
      </div>
    );
  }
}
```
#### 7) Console log
```console.log("MESSAGE")``` is a javascript code that performs similarly to ```printf()``` or ```System.out.print()```. It is useful for debugging webpages through ```F12 -> console```.

#### 8) Location of current webpage
```window.location``` can be use to extract the path of the current webpage. An example of what can be seen when you perform ```console.log(window.location)```  
![image](https://github.com/SorinoSSK/Learning-React/blob/main/Image/Example1.png)  
Thus, using ```window.location.pathname``` will return **/pricing**.

#### 9) Variable type
There are 2 type of variable declaration, excluding ```define``` and such which are embedded system specific. One being **strongly type** and the other **weakly type**. Strongly type is define to be variables such as <ins>int, long, str</ins>, and so on while weakly type does not require user to define the type of the variable. ```let``` and ```var``` are such non-variable type.  
- <ins>**var**</ins>  
```var``` has a function scope but no a block scope.  
If ```var``` is used outside of a function, it will be considered to be in a global scope.  
If ```var``` is used inside of a function, it belongs only to that function.  
If ```var``` is used inside of a block, the variable will still be available outside of the block.  
- <ins>**let**</ins>  
```let``` is block specific and this if it is called from within the block, it will only reside within that block.  

**Notes**  
```for loops``` and ```while loops``` are considered to be a block. 

#### 10) Defining variable to be used for rendering
This is just a note for how React works when using variables to be renders. When you define the variable name with caps at the start, ```e.g. Test```, then when rendering ```Test```, it will render a non-html component. 
The following two examples are the same where the second example provides more flexibility in your variable naming convention.
```
function App() 
{
  let Component
  switch(window.location.pathname)
  {
    case "/":
      Component = App
      break
    case "/pricing":
      Component = Pricing
      break
    case "/about":
      Component = About
      break
  }
  return (
    <>
      <Navbar/>
      <Component/>
    </>
  )
}
```
```
function App() 
{
  let component
  switch(window.location.pathname)
  {
    case "/":
      component = <App />
      break
    case "/pricing":
      component = <Pricing />
      break
    case "/about":
      component = <About />
      break
  }
  return (
    <>
      <Navbar/>
      <component/>
    </>
  )
}
```
#### 11) Usage of curly brackets in React 
- JavaScript XML (JSX)  
By using ```{variable}```, you are breaking out of HTML code to start JavaScript coding within ```{}```. The idea would be thing that ```{}``` allows JavaScript code to exist within HTML code.
- Destructuring syntax  
The usage of this is to allow the import of specific library from a long list of libraries. For instance, ```import {BrowserRouter} from "react-router-dom"``` imports the library ```BrowserRouter``` from ```react-router-dom```. To import more than 1 specific library, we can code it as such, ```import {Route, Routes} from "react-router-dom"``` The idea is similar to how **python** import its library.

#### 12) Directing

## Reference
- https://www.youtube.com/watch?v=0twjvW0c1r0 [Date of access: 06/02/2023]
- https://reactjs.org/ [Date of access: 06/02/2023]
- https://www.youtube.com/watch?v=SLfhMt5OUPI [Date of access: 08/02/2023]
