# ActionSources

### Traditional ActionCreator

Return value and action type was tightly coupled.

```javascript
function tick(message) {
  const date = new Date()
  if (message !== undefined) return { type: 'TIMER_TICK', payload: { date }}
  return { type: 'TIMER_TICK', payload: { date, message }}
}
```

### Pure Function (ActionSrc)

ActionSrc for `createActions` is just a pure javascript function with I/O. Arguments is optional.

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

Related: [createActions ->](createActions.md)
