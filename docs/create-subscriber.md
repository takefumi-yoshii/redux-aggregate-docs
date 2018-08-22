# createSubscriber

### 🛰 Everything can receive

Here we are creating Redux reducer with `createSubscriber`.  
`Subscriber` contains `ReducerFactory`.  

```javascript
import { createSubscriber } from 'redux-aggregate'
const {
  reducerFactory // Generated ReducerFactory
} = createSubscriber()
```
**It be required `Subscriptions` for subscribe.** (SummarySB as follows)

```javascript
import { createAggregate, createActions, createSubscriber } from 'redux-aggregate'
import { TimerAC } from './actions/timer'
import { TodosMT } from './models/todos'
import { SummarySB } from './models/summary'
// ______________________________________________________
//
// @ Aggregates

export const Timer = createActions(TimerAC, 'timer/')
export const Todos = createAggregate(TodosMT, 'todos/')
export const Summary = createSubscriber()
Summary.subscribe(Timer, SummarySB.Timer)
Summary.subscribe(Todos, SummarySB.Todos)
```
Related: [subscriptions ->](subscriptions.md)
