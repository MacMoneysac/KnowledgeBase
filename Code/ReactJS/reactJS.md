# ReactJS

## Getting started

```js

npx create-react-app counter-app
npm start

npm i bootstrap@4.1.1 font-awesome@4.7.0 react-bootstrap axios
npm i -S @react-google-maps/api

import "bootstrap/dist/css/bootstrap.css";
import "font-awesome/css/font-awesome.css";

import Counter from "./components/counter";

```

## Snippets

imrc → Import React / Component  
cc → Class Component

## Stateless Functional Component

```js

const NavBar = () => {
    return (
    <span />
    );
};

```

## Funtional Component with State

```js

class NavBar extends Component {
    state = {};

    render() {
    return (
            <span />    
        );
    }
}

```
