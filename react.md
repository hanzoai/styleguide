# React Style Guide

=> **Note**: this guide assumes you are using [Babel](https://babeljs.io)

## Table of Contents

  1. [React Hooks](#hooks)

## Hooks

  <a name="reacthooks"></a><a name="1.1"></a>
  - [1.1](reacthooks) **React Hooks**: We hope to replace all class components with react hooks

  >Why? Hooks provide the ability to extract state and the React lifecycle into functions that can be utilized across components in your app, making it easy to share logic.

    ```javascript
    const [count, setCount] = React.useState(42)
    <Button onClick={() => setCount(count + 1)}>{count}</Button>
    ```

**[⬆ back to top](#table-of-contents)**
