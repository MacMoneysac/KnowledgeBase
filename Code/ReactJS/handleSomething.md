# Handlers

```js

constructor() {
    super();
    this.handleIncrement = this.handleIncrement.bind(this);
  }

handleIncrement() {
    console.log("Increment", this);
  }

// or the same but simpler

handleIncrement = () => {
    console.log("Increment", this);
}

```
