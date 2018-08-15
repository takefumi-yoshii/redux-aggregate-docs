# redux-aggregate-immer

### 🏝 What you want to do Frankly

[redux-aggregate-immer](https://www.npmjs.com/package/redux-aggregate-immer) is the helper module for redux-aggregate.
Below code be able to write more comfortable, with `wrapImmer`.

```javascript

const initialState = {
  count: 0,
  nested: { some: { value: 'string' } }
}
// ______________________________________________________
//
// @ Mutations

function increment(state) {
  return { ...state, count: state.count + 1 }
}
function idecrement(state) {
  return { ...state, count: state.count - 1 }
}
function setNestedValue (s, value) {
  return {
    ...state,
    nested: {
      ...state.nested,
      some: {
        ...state.nested.some,
        value
      }
    }
  }
}
export const Mutations = {
  increment,
  decrement,
  setNestedValue
}
```

Mutable mutations will be convert to immutable mutations.
To be careful not to return state at those mutation.

```javascript
import { wrapImmer } from 'redux-aggregate-immer'

const initialState = {
  count: 0,
  nested: { some: { value: 'string' } }
}
// ______________________________________________________
//
// @ MutableMutations for wrapImmer

function increment(state) {
  state.count++
}
function idecrement(state) {
  state.count--
}
function setNestedValue (state, value) {
  state.nested.some.value = value
}
export const Mutations = wrapImmer({
  increment,
  decrement,
  setNestedValue
})
```
