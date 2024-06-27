Redux middleware - https://www.youtube.com/watch?v=LvsiqAyFzPk&t=2581s<br>
1. Thunk are functions used to delay a functionality.<br>
2. actions are by default synchronous<br>
3. to have asynchronous action, we can wrap it in a thunk function<br>

Detailed documentation - https://redux.js.org/usage/writing-logic-thunks<br>

Setup:<br>
import { createStore, applyMiddleware } from 'redux'<br>
import { thunk } from 'redux-thunk'<br>
import rootReducer from './reducers/index'<br>

const store = createStore(rootReducer, applyMiddleware(thunk))<br>

Writing Thunk:<br>
A thunk function is a function that accepts two arguments: the Redux store dispatch() method, and the Redux store getState() method. Thunk functions are not directly called by application code. Instead, they are passed to store.dispatch()<br>

![thunk](thunk.png)