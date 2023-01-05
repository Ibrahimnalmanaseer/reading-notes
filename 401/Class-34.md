# Context API

## What is global state with React?

The main purpose of the global state is to share a `state` among multiple components.

There are three ways this communication can happen:

- With a child component
- With a parent component
- With a sibling component


## State traveling down

`State` traveling down through the hierarchy is best managed using the mutable `state`at the highest level to determine immutable properties that define the lower-level components
As a result, the `state` tracked by the lower-level component will persist unless the component disappears.




