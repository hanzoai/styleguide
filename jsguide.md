# JavaScript Style Guide

*Carefully selected conventions based on years of experience as well as purely aesthetic preferences*

> **Note**: this guide assumes you are using [Babel](https://babeljs.io)

## Table of Contents

  1. [Syntax](#syntax)
  1. [References](#references)
  1. [Objects](#objects)

## Syntax

  <a name="syntax--semicolon"></a><a name="1.1"></a>
  - [1.1](syntax--semicolon) **semicolon**: JavaScript semicolons are optional. As company preference, we omit semicolons

    ```javascript
    const foo = 1
    console.log(foo) // => 1
    ```
  <a name="syntax--complex"></a><a name="1.2"></a>
  - [1.2](#syntax--trailing-comma)  **Complex**: JavaScript has allowed trailing commas in array literals since the beginning, and later added them to object literals (ECMAScript 5) and most recently (ECMAScript 2017) to function parameters.

  >Why? Trailing commas can be useful when adding new elements. If you want to add a new property, you can simply add a new line without modifying the previously last line if that line already uses a trailing comma. This makes version-control diffs cleaner and editing code might be less troublesome.

    ```javascript
    const foo = [1, 2, 3,]

    const bar = {
      foo: "bar",
      baz: "qwerty",
      age: 42,
    }
    ```

**[⬆ back to top](#table-of-contents)**

## References

  <a name="references--prefer-const"></a><a name="2.1"></a>
  - [2.1](#references--prefer-const) Use `const` for all of your references avoid using `var`.

    > Why? This ensures that you can’t reassign your references, which can lead to bugs and difficult to comprehend code.

    ```javascript
    // bad
    var a = 1
    var b = 2

    // good
    const a = 1
    const b = 2
    ```

  <a name="references--disallow-var"></a><a name="2.2"></a>
  - [2.2](#references--disallow-var) If you must reassign references, use `let` instead of `var`

    > Why? `let` is block-scoped rather than function-scoped like `var`.

    ```javascript
    // bad
    var count = 1
    if (true) {
      count += 1
    }

    // good, use the let.
    let count = 1
    if (true) {
      count += 1
    }
    ```

  <a name="references--block-scope"></a><a name="2.3"></a>
  - [2.3](#references--block-scope) Note that both `let` and `const` are block-scoped.

    ```javascript
    // const and let only exist in the blocks they are defined in.
    {
      let a = 1
      const b = 1
    }
    console.log(a) // ReferenceError
    console.log(b) // ReferenceError
    ```

**[⬆ back to top](#table-of-contents)**

## Objects

  <a name="es6-object-shorthand"></a><a name="3.1"></a>
  - [3.3](#es6-object-shorthand) Use object method shorthand.

    ```javascript
    // bad
    const atom = {
      value: 1,

      addValue: function (value) {
        return atom.value + value
      },
    }

    // good
    const atom = {
      value: 1,

      addValue(value) {
        return atom.value + value
      },
    }
    ```

  <a name="es6-object-concise"></a><a name="3.2"></a>
  - [3.4](#es6-object-concise) Use property value shorthand.

    > Why? It is shorter and descriptive.

    ```javascript
    const miyamotoMusashi = 'Miyamoto Musashi'

    // bad
    const obj = {
      miyamotoMusashi: miyamotoMusashi,
    }

    // good
    const obj = {
      miyamotoMusashi,
    }
    ```

  <a name="objects--grouped-shorthand"></a><a name="3.3"></a>
  - [3.5](#objects--grouped-shorthand) Group your shorthand properties at the beginning of your object declaration.

    > Why? It’s easier to tell which properties are using the shorthand.

    ```javascript
    const miyamotoMusashi = 'Miyamoto Musashi'
    const honjoMasamune = 'Honjo Masamune'

    // bad
    const obj = {
      katana: 1,
      samurai: 2,
      miyamotoMusashi,
      dojo: 3,
      bushi: 4,
      anakinSkywalker,
    }

    // good
    const obj = {
      miyamotoMusashi,
      anakinSkywalker,
      katana: 1,
      samurai: 2,
      dojo: 3,
      bushi: 4,
    }
    ```
**Other Style Guides**

  - [Google JavaScript Style Guide](https://google.github.io/styleguide/jsguide.html)
  - [Principles of Writing Consistent, Idiomatic JavaScript](https://github.com/rwaldron/idiomatic.js)
  - [StandardJS](https://standardjs.com)

