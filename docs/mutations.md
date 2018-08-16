# Mutations

### ✅ In most use cases are enough for this

Mutaions is immutable mutate functions for state.
Generate boilerplate starting from this MutationsMap.
It be equal to behavior of Reducer.
Let provide payload as the second argument if necessary.
**This is pure function for state.**

```javascript
const state = {
  count: 0,
  unit: 'pt'
}
// ______________________________________________________
//
// @ Mutations

function increment(state) {
  return { ...state, count: state.count + 1 }
}
function decrement(state) {
  return { ...state, count: state.count - 1 }
}
function setCount(state, value) {
  return { ...state, count: value }
}
export const Mutations = {
  increment,
  decrement,
  setCount
}
```

If you call `createAggregate` with this Mutations and `counter/` namespace, it will be behave as follows.

```javascript
const { types, creators } = createAggregate(Mutations, 'counter/')
const { type, payload } = creators.setCount(100)
console.log(types.setCount) // counter/setCount
console.log(type, payload) // counter/setCount, 100
```

Related: [createAggregate ->](create-aggregate.md)

### ❓ How to define many-to-many

If need to extract definition of Actions, use [createActions](create-actions.md).  
If need to extract definition of Reducers, use [subscribe](subscribe.md) and [subscriptions](subscriptions.md).
