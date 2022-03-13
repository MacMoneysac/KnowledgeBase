# Map

```js

state = {
  "Fire", "Water", "Rock", "Air"
}

<ul>
  {this.state.tags.map((tag) => (
    <li key={tag}>{tag}</li>
  ))}
</ul>

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
  