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

ActionSources for `createActions` is just a pure javascript function's map. Arguments is optional.

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

Related: [createActions ->](create-actions.md)
