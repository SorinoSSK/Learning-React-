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
Rendering is a term used to feed values from the backend to the variables declared at the front end and there are 2 ways to implement rendering.  
a) ReactDOM.render(Variable, ID) [Within index.js]
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
