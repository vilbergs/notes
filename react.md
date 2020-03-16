## Working with array state

When dealing with an array of state, it's best to make sure to always keep the array immutable. 
Meaning, every time we need to update the state array we need to supply the state dispatcher with an entirely new
copy of the array, with the changes we made.

Provided we're keeping track of the index we're at when mapping over the state array, this could be solved like this:
```javascript
  // say we're mapping over something...
  .map((x, xIndex) => {
     setState((previousState) => {
      previousState.map((item, itemIndex) => {
        if (xIndex === itemIndex) {
          return {
            ...item,
            value: newValue
          }
        }
        
        return item
      })
     })
  })
```
