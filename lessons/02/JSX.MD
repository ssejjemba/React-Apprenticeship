# Using JSX

## 📝 Your Notes

This is a brief about JSX and how it is used in react

## Background

JSX is more intuitive than the raw React API and is easier to understand when
reading the code. It's fairly simple HTML-like syntactic sugar on top of the raw
React APIs:

```jsx
const ui = <h1 id="greeting">Hey there</h1>

// ↓ ↓ ↓ ↓ compiles to ↓ ↓ ↓ ↓

const ui = React.createElement('h1', {id: 'greeting', children: 'Hey there'})
```

Because JSX is not actually JavaScript, you have to convert it using something
called a code compiler. [Babel](https://babeljs.io) is one such tool.

🦉 Pro tip: If you'd like to see how JSX gets compiled to JavaScript,
[check out the online babel REPL here](https://babeljs.io/repl#?builtIns=App&code_lz=MYewdgzgLgBArgSxgXhgHgCYIG4D40QAOAhmLgBICmANtSGgPRGm7rNkDqIATtRo-3wMseAFBA&presets=react&prettier=true).

If you can train your brain to look at JSX and see the compiled version of that
code, you'll be MUCH more effective at reading and using it! I strongly
recommend you give this some intentional practice.

## Exercise

Find the exercise under the exercises folder in the folder called 02 ('../../exercises/02.html').
The exercise is an html file with a few instructions on how to solve it.
We are not using create react app for this lesson as we are simply using react as a library and not as a framework.

### Instructions
- Copy the html file to your local folder 
- Finish the tasks from the instructions
- Read and attempt the extras for bonus marks during assessment
- Extras should be done and handed in as seperate files

## Extra Credit

### 1. 💯 interpolate className and children

"Interpolation" is defined as "the insertion of something of a different nature
into something else."

Let's take template literals for example:

```javascript
const greeting = 'Sup'
const subject = 'World'
const message = `${greeting} ${subject}`
```

See if you can figure out how to extract the `className` (`"container"`) and
`children` (`"Hello World"`) to variables and interpolate them in the JSX.

```jsx
const className = 'container'
const children = 'Hello World'
const element = <div className="hmmm">how do I make this work?</div>
```

📜 The react docs for JSX are pretty good:
https://reactjs.org/docs/introducing-jsx.html

Here are a few sections of particular interest for this extra credit:

- https://reactjs.org/docs/introducing-jsx.html#embedding-expressions-in-jsx
- https://reactjs.org/docs/introducing-jsx.html#specifying-attributes-with-jsx

### 2. 💯 spread props

What if I have an object of props that I want applied to the `div` like this:

```jsx
const children = 'Hello World'
const className = 'container'
const props = {children, className}
const element = <div /> // how do I apply props to this div?
```

If we were doing raw React APIs it would be:

```jsx
const element = React.createElement('div', props)
```

Or, it could be written like this:

```jsx
const element = React.createElement('div', {...props})
```

See if you can figure out how to make that work with JSX.

📜 https://reactjs.org/docs/jsx-in-depth.html#spread-attributes
