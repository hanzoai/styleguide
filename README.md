# HANZO Style Guide
Here lies carefully selected conventions based on years of experience as well as a few purely aesthetic preferences.  Conventions contribute to longterm maintenece, efficeniency, and reusiblity of code.

If you are modifying a project that originated at Hanzo, or begining a new project at Hanzo, code must adhere to these conventions.  Please go through process of checking your code first rather than being rejected for not meeting our guidelines.

This is a living document.  Please feel add your own suggestions.

# Contributing
To contribute to the style guide:

1. Fork this repo
2. Update document with your suggestions
3. Submit PR

# Index
- [Git Style Guide](git.md)
- [JavaScript Style Guide](js.md)
- [React Style Guide](react.md)

# Zen of Hanzo

The Zen of Hanzo guides the design and engineering of all of our products.

## Orthogonality
*   Functionality across components should not be shared
*   There should be preferably only one way to do something

## Smallness
*   Each thing should have a small number of concerns
*   Components should ideally do just one thing
*   APIs are easier to understand when they do less

## Consistency
*   ...but not at the expense of pragmatism
*   APIs should use consistent standards
*   Copy yourself

## Composability
*   Build large things out of small components
*   It’s easier to build large things out of many small components


## Completeness
*   “Batteries included.” Our standard library should cover as many use cases as possible
*   No single API tries to do everything, but collectively can accomplish anything

## Dimensionality
*   Provide access to multiple layers of abstraction
*   Conceal complexity but do not prevent access to it
*   Components compose across multiple dimensions
*   Use the right layer of abstraction

## Agility
*   Adapt and evolve as necessary.
*   Organizations need to be able to move at will
*   Nothing should lock you in
*   You should be able to grow rapidly
*   Collect the right things (small / big), look at details + big picture

## Reflect
*   Accessibility to data is important
*   Deep reflection is important for design especially

## Clarity
*   Ideas should be communicated in their simplest forms
*   Our APIs should be designed as intuitive as possible
*   Our documentation should enable users to absorb information as easily as possible, with as little fluff
*   Coherence and quality of data gathered / your own understanding

## Focus
*   commit to a single course of action guided by data
*   “If you chase two rabbits, you will lose them both.”
*   Our APIs should be focused on solving single problems
