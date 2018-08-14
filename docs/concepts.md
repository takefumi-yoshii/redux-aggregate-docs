![image.png](/assets/logo.svg)

## State management is core of the application.

The purpose of this library is to make the application core independent by pure language specification.

Persistent code does not need to be closely related to Redux concept.
I think it is important to extend the life of the code / accompanying test.

Strong type definition by TypeScript,and ecosystems of supported by community.
I believe this will be its hub.

___

### 🔥 Surprisingly small type definition

By type inference in conditional types, we got type safe code any where.This helper solve the problem of the past type definition.
* [InferredTypes](inferred-types.md)

### ✅ In most use cases are enough for this

Don't you think that Actions need not be open for all use cases? This is the only thing We would like to do first.
* [Mutations](mutations.md)

### ✨ Pureness was kept

Do you think that even if ActionType and payload are coupled, it is pure? This helper require truthly pure function.
* [ActionSources](action-sources.md)

### 🛠 Expand reducer progressively

You may be interested in external Actions in the future. This helper can expand the context to progressive.
* [Subscriptions](subscriptions.md)

### 🎖 Give the behavior of Model to State

Are you leaking a lot of knowledge in View? This helper recommend to give behavior as model to state.
* [Queries](queries.md)


for state