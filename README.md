# React Facebook Authentication

Allows developers to receive a facebook authentication token that can be used by a backend service.

## Installation
To install the latest version:

```
npm install --save react-facebook-auth
```
or
```
yarn add react-facebook-auth
```

### How to use
```js
import React from 'react';
import ReactDOM from 'react-dom';
import FacebookAuth from 'react-facebook-auth';

const MyFacebookButton = ({ onClick }) => (
  <button onClick={onClick}>
    Login with facebook
  </button>
);

const authenticate = (response) => {
  console.log(response);
  // Api call to server so we can validate the token
};

const App = () => (
  <div>
    <h1>Facebook Auth</h1>
    <FacebookAuth
      appId="<app-id>"
      callback={authenticate}
      component={MyFacebookButton}
    />
  </div>
);

ReactDOM.render(
  <App />,
  document.getElementById('root'),
);
```

A full example can be found in [examples](https://github.com/ionutmilica/react-facebook-auth/tree/master/example) directory.

### License
MIT