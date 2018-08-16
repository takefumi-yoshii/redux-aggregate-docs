# createActions

### 🌎 Anything will happen

This api return `ActionTypes / ActionCreators`.
First argument is map of `ActionSources`.
Second argument is a unique namespace.With this, ActionType won't conflict.

```javascript
import { createActions } from 'redux-aggregate'
import { ActionSources } from 'path/to/actions/timer'
const {
  types,    // Generated ActionTypes
  creators  // Generated ActionCreators
} = createActions(ActionSources, 'timer/')
```

**By this alone, completed to define ActionTypes/ActionCreators with inferred type.**

Related: [ActionSources ->](action-sources.md)

___

### 🔥 Auto inferred type by TypeScript

![image.png](/assets/type_inference_in_conditional_types_action_src.png)

By the map of Type inference in conditional types, generated action creator's auto inferred.
