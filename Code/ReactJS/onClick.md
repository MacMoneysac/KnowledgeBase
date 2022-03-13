# onClick handler

Problem, you can only pass a refernce to a function in a onClick argument.

e.g. onClick = this.handleIncrement  - But no paranthesis

```js

handleIncrement = (product) => {
  console.log(product);
  this.setState({ count: this.state.count + 1 });
};

```

## Without Parameter

```js

<button
  onClick={handleIncrement}
  className="btn-secondary btn-sm"
>
  Increment
</button>

```

## With Parameter

> () => function()

```js

<button
  onClick={() => this.handleIncrement("argument")}
  className="btn-secondary btn-sm"
>
  Increment
</button>

```
