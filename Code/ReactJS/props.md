# Props, passing data to components

z.B. _key, onDelete, value_

```js

state = {
    count: this.props.value,
  };

```

```js

state = {
    counters: [
      { id: 1, value: 0 },
      { id: 2, value: 0 },
      { id: 3, value: 0 },
      { id: 4, value: 0 },
    ],
  };
  render() {
    return (
      <div>
        {this.state.counters.map((counter) => (
          <Counter key={counter.id} value={counter.value} selected={true} />
        ))}
      </div>
    );
  }

```

```js

<Counter
  key={counter.id}
  onDelete={this.handleDelete}
  value={counter.value}
/>

```
