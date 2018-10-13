# Reac Basics
In this project, I will define the basic properties of the React.js.
We put the following scripts in the index.hmtl
```sh
<script crossorigin src="https://unpkg.com/react@16/umd/react.development.js"></script>
<script crossorigin src="https://unpkg.com/react-dom@16/umd/react-dom.development.js"></script>
<script src="./app.js"></script>
```
In app.js we define element that we want react to create which will be an object. This is the element which we want to render to the DOM.
```sh
const title = React.createElement(
    // element to create
    'h1',
    {id: 'main-title', title:'This is a title'},
    'My First React Element'
);
console.log(title);
```
we create h1 with id and title attributes and text as its children.

## ReactDOM.render()
Render react element to the DOM. This function does the creating and updating. It connect react to the DOM.

```sh
ReactDOM.render(
    title,
    document.getElementById('root')
);
```
It will render the title object to the DOM with id root.
In the index html body
```sh
<div id="root"></div>
```
Now we render the header element which include the head information

```sh
const title = React.createElement(   
    'h1',
    {id: 'main-title', title:'This is a title'},
    'My First React Element'
);

const desc = React.createElement(
  'p',
  null,  
  'I just learned how to create a React node and render it into the DOM.'
);

const header = React.createElement(
    'header',
    null,
    title,
    desc
);

ReactDOM.render(
    header,
    document.getElementById('root')

);
```
> React render what should be render to the DOM.