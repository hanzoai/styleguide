# HanzoAI React Style Guide() {

*Carefully selected conventions based on years of experience as well as purely aesthetic preferences*

> **Note**: this guide assumes you are using [Babel](https://babeljs.io)

## Table of Contents

  1. [React Hooks](#reacthooks)

## Syntax

  <a name="reacthooks--semicolon"></a><a name="1.1"></a>
  - [1.1](reacthooks) **semicolon**: We hope to replace all class components with react hooks

  >Why? Hooks provide the ability to extract state and the React lifecycle into functions that can be utilized across components in your app, making it easy to share logic.

    ```javascript
    const [count, setCount] = React.useState(42)
    <Button onClick={() => setCount(count + 1)}>{count}</Button>
    ```

**[⬆ back to top](#table-of-contents)**

