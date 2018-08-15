# createAggregate

### 🚀 Accelerate development

Here we are creating them with `createAggregate`.
`Aggregate` contains `ActionTypes / ActionCreators / ReducerFactory`.
The first argument is `Mutations`, a map of mutate functions.
The second argument is a unique namespace.With this, ActionType won't conflict.

```javascript
import { createAggregate } from 'redux-aggregate'
import { Mutations } from 'path/to/model'
const {
  types,         // Generated ActionTypes
  creators,      // Generated ActionCreators
  reducerFactory // Generated ReducerFactory
} = createAggregate(Mutations, 'counter/')
```

**By this alone, completed to define ActionTypes/ActionCreators/ReducerFactory with inferred type.**

Mutaions is immutable mutate functions for state.
Generate boilerplate starting from this MutationsMap.
It be equal to behavior of Reducer.
Let provide payload as the second argument if necessary.

Related: [Mutations ->](mutations.md)
