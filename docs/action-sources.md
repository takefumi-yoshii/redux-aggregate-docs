# ActionSources

### ✨ Pureness was kept

Traditional ActionCreator's return type and paylaod was tightly coupled.

```javascript
function tick(message) {
  const date = new Date()
  if (message !== undefined) return { type: 'TIMER_TICK', payload: { date }}
  return { type: 'TIMER_TICK', payload: { date, message }}
}
```

ActionSources for `createActions` is just a pure javascript function's map.
Input argument and return value is optional.
**This is pure function for all.**

```javascript
// ______________________________________________________
//
// @ ActionSources

function tick(message) {
  const date = new Date()
  if (message !== undefined) return { date }
  return { date, message }
}
export const ActionSources = { tick }
```

If you call `createActions` with this ActionSources and `timer/` namespace, it will be behave as follows.

```javascript
const { types, creators } = createActions(ActionSources, 'timer/')
const { type, payload } = creators.tick('current time notification')
console.log(types.tick) // timer/tick
console.log(type, payload.message) // timer/tick, 'current time notification'
```

Related: [createActions ->](create-actions.md)
