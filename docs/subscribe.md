# subscribe

### 📡 Caught outside Actions

Aggregate contain method of `subscribe` action.
In the example below, subscribe TimerActions.
**It be required `Subscriptions` for subscribe.** (TodosSB.Timer as follows)

```javascript
import { createAggregate, createActions } from 'redux-aggregate'
import { TimerAC } from './actions/timer'
import { TodosMT, TodosSB } from './models/todos'
// ______________________________________________________
//
// @ Aggregates

export const Timer = createActions(TimerAC, 'timer/')
export const Todos = createAggregate(TodosMT, 'todos/')
Todos.subscribe(Timer, TodosSB.Timer)
```
Related: [subscriptions ->](subscriptions.md)

### Upstream subscribing of Downstream

Being able to subscribe is not just `Actions`.
An aggregate be able to subscribe another aggregate actions.
As with `Actions`, the Downstream aggregate follows Upstream aggregate function name and payload.

```javascript
// ______________________________________________________
//
// @ Aggregates

export const Timer = createActions(TimerAC, 'timer/')
export const Counter = createAggregate(CounterMT, 'counter/')
export const Todos = createAggregate(TodosMT, 'todos/')
export const Summary = createSubscriber()
Todos.subscribe(Timer, TodosSB.Timer)
Counter.subscribe(Timer, CounterSB.Timer)
Summary.subscribe(Timer, SummarySB.Timer)
Summary.subscribe(Counter, SummarySB.Counter)
Summary.subscribe(Todos, SummarySB.Todos)
```
