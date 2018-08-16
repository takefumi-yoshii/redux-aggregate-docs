# createAggregate

### 🚀 Accelerate development

Here we are creating Redux boilerplate with `createAggregate`. 
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

Related: [Mutations ->](mutations.md)

___

### 🔥 Auto inferred type by TypeScript

![image.png](/assets/type_inference_in_conditional_types_mutation.png)

By the map of Type inference in conditional types, generated action creator's auto inferred.
