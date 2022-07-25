## Rules of Reducers:
1. They should only calculate the new state value based on the `state` and `action` arguments.
2. They are not allowed to modify the existing state. Instead, they must copy the existing state and make changes to the copied values.
3. They must not do any asynchronous logic or have other “side effects”.

> "By asynchronous logic or “side effects”, we mean anything that the function does aside from returning a value, e.g. logging to the console, saving a file, setting a timer, making an HTTP request, generating random numbers.
> 
>These rules make Redux code predictable and easy to debug: tests run reliably and other developers know what to expect from your code."
## Example 1 - reducer (with filter)
``` javascript
const initialState = [ 'Take Five', 'Claire de Lune', 'Respect' ];

const addNewSong = {
  type: 'songs/addSong',
  payload: 'Halo'
};

const removeSong = {
  type: 'songs/removeSong',
  payload: 'Take Five'
};

const removeAll = {
  type: 'songs/removeAll'
}

const reducer = (state = initialState, action) => {
  switch (action.type) {
    case 'songs/addSong': {
      return [...state, action.payload];
    }
    case 'songs/removeSong': {
     return state.filter(song => song !== action.payload);
    }
  default: {
    return state;
  }
  }
}
```