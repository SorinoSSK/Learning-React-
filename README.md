# Learning-React

## 1) Installation
#### a) Install Node.js
- ```https://nodejs.org/en/download/```
#### b) Open up Node.js command prompt
#### c) Install react
- Run ```npm install -g create-react-app```

## 2) Create react project
#### a) Open up Node.js command prompt
#### b) Change directory to intended directory
- ```cd ...```  
- This directory will be used to store created react project.
#### c) Create a project **(Do not use caps for project name)**
```create-react-app project-name```

## 3) Running react project
#### a) Open up Node.js command prompt
#### b) Change directory to intended directory **(Directory of project folder)**
#### c) To run the react file
- Hosting react project (browser)
- ```npm start```

## 4) Visual Studio code can be used for editing visual studio
## 5) Ideology behind React
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
## 6) Online Editor
- ```https://codepen.io```
#### a) Open pen settings
- ```Open JS Settings```
#### b) Set preprocessor to Babel
- Under ```JavaScript Preprocessor```
- Select Babel
#### c) Add externel scripts to run react libraries
- Under ```Add External Scripts/Pens```
- Under ```Add resource text box```
- Add these two URL  
```https://unpkg.com/react/umd/react.development.js```  
```https://unpkg.com/react-dom/umd/react-dom.development.js```
## Reference
- https://www.youtube.com/watch?v=0twjvW0c1r0
- https://reactjs.org/
