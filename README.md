# Redux Interview Questions

#### Sourced from:

- https://www.fullstacktutorials.com/interviews/redux-interview-questions-and-answers-33.html
- https://dev.to/fullstackcafe/26-reactredux-interview-questions-you-should-know-in-2018-41je
- https://medium.com/@sepineda/react-redux-interview-questions-b7f6611823f

---

1. What is Redux?

<details>
<summary><b>Answer</b></summary>
<p>
Redux is a javascript library for managing application state.
</p>
</details>

2. What are some the benefits of using Redux?

<details>
<summary><b>Answer</b></summary>
<p>

1. Single-Source of Truth
2. Predictable State
3. No need to lift State "up"
4. Debugging enhancements via the Redux Dev Tools
5. Separates logic from components

</p>
</details>

3. What are the three core principles of Redux?

<details>
<summary><b>Answer</b></summary>
<p>

- The state of your application is stored in an object tree within a single store, aka "Single Source of Truth"
- State is immutable. You can only make changes by emitting an action.
- Changes, actions that transform state, are made using Pure Reducers.

</p>
</details>

4. What is the Redux Workflow?

<details>
<summary><b>Answer</b></summary>
<p>

- Store - Where you keep your application data
- Dispatch - **Actions** are dispatched by events
- Reducers - Pure functions that take previous state + action and return a new state
- Subscribe - Components can subscribe to the store for actions or state

</p>
</details>

5. How do your provide the store to your app?

<details>
<summary><b>Answer</b></summary>
<p>

- Wrap your `<App>` component in the `<Provider>` component.
- Pass the `store` as a prop to your `<Provider>` component:
  - `<Provider store={store}>`

</p>
</details>

6. What are the Store Methods?

<details>
<summary><b>Answer</b></summary>
<p>

- `getState()`
  - Returns the current state of your application
- `dispatch(action)`
  - Dispatches and action. This is the _only_ way to trigger a state change
- `subscribe(listener)`
  - Adds a change listener
- `replaceReducer(nextReducer)`
  - Replaces the reducer currently used by the store to calculate the state

</p>
</details>

7. What is the name of the reducer that _combines_ all the reducers?

<details>
<summary><b>Answer</b></summary>
<p>
The `rootReducer` combines all reducers. 
</p>
</details>

8. Can Redux _only_ be used with React?

<details>
<summary><b>Answer</b></summary>
<p>
Nope!  It's most commonly associated with React, but can be used standalone, or with other frameworks (i.e. Angular, VueJS).
</p>
</details>

BONUS: Where does Redux store data?

<details>
<summary><b>Answer</b></summary>
<p>
The "store" is kept in memory.  Redux technically keeps references to the data in memory, not the actual data itself (aka, it's _not_ a database).
</p>
</details>

BONUS: What is a Pure Function?

<details>
<summary><b>Answer</b></summary>
<p>
A function that...

- Given the same input, will always return the same output.
- Produces no side effects.
- Relies on no external mutable state

</p>

```
function square(x){
   return x * x;
}
return items.map(square);
```

</details>
