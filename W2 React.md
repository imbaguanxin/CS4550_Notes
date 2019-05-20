# React

## Set up environment

Install `node.js` on local machine

Use `npm` to install the create react app CLI and create a boilerplate application

```bash
npm install -g create-react-app
```

Then make a directory and `cd` to that directory
```bash
mkdir my-app-example
cd my-app-example
create-react-app my-app-example
npm start
```

***Alternative way*** : make use of ide like `WebStorm` to start a react project

## Component

`react` enables us to have namespace or package. Under different namespace, we can have components which is similar to class in Java and can be reused outside. We can also importe components from other files. As a result, we can tear apart large application to small pieces
``` Javascript
import React from 'react';
class HelloWorld extends React.Component {
  render() {
    return(<h1>Hellow, world!</h1>)
  }
}
// export to default package as "HelloWorld"
export default HelloWorld
```
Outside this file, we can import `HelloWorld` using:
```Javascript
// just import from path
import HelloWorld from './hello'

// reuse this Component:
ReactDOM.render(
  <HelloWorld/>, // here we use HelloWorld component
  document.getElementById('root')
  )
```

## Bootstrap in `React` project

### Install and import `Bootstrap`

install from the command line:
```bash
npm install bootstrap --save
```
The package is going to stored under `/node_modules`. `--save` writes the dependency into `package.json` file.

import `Bootstrap`:
```Javascript
import 'bootstrap/dist/css/bootstrap.min.css'
```

### `className` and `styles`
In react, to differ className
