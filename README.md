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
Add the following URL,
1) ```https://unpkg.com/react/umd/react.development.js```  
2) ```https://unpkg.com/react-dom/umd/react-dom.development.js```  
Under ```Add resource text box``` within the```Add External Scripts/Pens``` setting. 

## Ideology/Terminology behind React
React has some additional terminology and a different code implementation from convention thus this section will highlight a few of them.
#### a) There will be 3 basic folder generated after running "2a)"
- node-modules
- public
- src
#### b) index.html
- ```public -> index.html```
- This file will store the front end of the webpage
#### c) App.js
- ```src -> App.js```
- This file will store the back end of the webpage. E.g. Functionality of buttons, variables of front end.
#### d) index.js
- ```src -> index.js```
- This file will link up **App.js** with **index.html**
- The idea is similar to flask.
#### e) ReactDOM.render(Variable, ID) [Within index.js]
- ```ReactDOM.render(asdasfd, document.getElementById('testID'));```
#### f) ReactDOM.createRoot(ID) [Within index.js]
- Similar to 5e)  
```const root = ReactDOM.createRoot(document.getElementById('test'));```  
```root.render(<React.StrictMode>Whatever you want to do here.</React.StrictMode>)```
#### g) Components
- Components is a function which allows a chunk of code to be reused.
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
- ShoppingList is a **React component class** or **React component type**
- In this case, **render()** method returns a chunk of code to be displayed on screen
- The above html code is equivalent to the following code
```
return React.createElement
(
  'div', {className: 'shopping-list'},
  React.createElement('h1', /* ... h1 children ... */),
  React.createElement('ul', /* ... ul children ... */)
);
```
#### h) Props
- Props is a subset of a component. Component is the parent class and Props is a child class.
- this.props.value, passes the child ID from component to the child.

## Reference
- https://www.youtube.com/watch?v=0twjvW0c1r0
- https://reactjs.org/
