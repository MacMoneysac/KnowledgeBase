# Axious

```js
 import axious from 'axious';

 ```

App.js

 ```js
// Snippet: cdm

// Use async when use await
async componentDidMount(){

    // pending > resolved (success) OR rejected (failure)
    const { data: items } = await axious.get('/api/items');
    this.setState({ items });

    // data destructuring

}
 ```
