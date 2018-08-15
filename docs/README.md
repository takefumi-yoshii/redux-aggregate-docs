![image.png](/assets/logo.svg)

## State management is core of the application.

The purpose of this library is to make the application core independent by pure language specification.Persistent code does not need to be closely related to Redux concept.I think it is important to extend the life of the code / accompanying test.Redux already has strong type definition by TypeScript,and ecosystems of supported by community.I believe this will be its hub.

[![Latest Version](https://img.shields.io/badge/npm-redux_aggregate-C12127.svg)](https://www.npmjs.com/package/redux-aggregate)
[![CircleCI](https://circleci.com/gh/takefumi-yoshii/redux-aggregate.svg?style=svg)](https://circleci.com/gh/takefumi-yoshii/redux-aggregate)

___

### [Concepts](concepts.md)

* [InferredTypes](inferred-types.md)
* [Mutations](mutations.md)
* [ActionSources](action-sources.md)
* [Subscriptions](subscriptions.md)
* [Queries](queries.md)

### [APIs](apis.md)

* [createAggregate](create-aggregate.md)
* [createActions](create-actions.md)
* [subscribe](subscribe.md)

### [Advanced Feature](advanced-feature.md)

* [redux-aggregate-immer](redux-aggregate-immer.md)
