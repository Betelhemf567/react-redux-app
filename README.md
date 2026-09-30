# React Redux State Management

This project is a React application built with TypeScript and Redux. It demonstrates how Redux can be used to manage global state in a React application without using Redux Toolkit.

The project was created as part of a React learning activity to understand the main concepts of Redux, including stores, actions, reducers, middleware, and connecting Redux to React.

## Features

* Redux store setup
* Counter state management
* Increment, decrement, and reset actions
* Counter reducer
* Combined reducers using `combineReducers`
* React Redux `Provider`
* `useSelector` for reading Redux state
* `useDispatch` for dispatching actions
* Redux Logger middleware
* TypeScript
* CSS Modules
* Vite development environment

## Technologies Used

* React
* TypeScript
* Vite
* Redux
* React Redux
* Redux Logger
* CSS Modules

## Project Structure

```text
src/
├── components/
│   ├── Counter.tsx
│   └── Counter.module.css
│
├── store/
│   ├── actions/
│   │   └── counterActions.ts
│   │
│   ├── reducers/
│   │   ├── counterReducer.ts
│   │   └── index.ts
│   │
│   └── store.ts
│
├── App.tsx
├── main.tsx
└── index.css
```

## How the Application Works

The application contains a simple counter that is managed by Redux.

When the user clicks one of the counter buttons, an action is dispatched to Redux. The reducer receives the action and returns the updated state. React then receives the new state and updates the user interface.

The three available actions are:

* **Increment** — increases the counter by 1
* **Decrement** — decreases the counter by 1
* **Reset** — returns the counter to 0

## Redux Flow

The application follows the basic Redux data flow:

```text
User clicks a button
        ↓
Action is dispatched
        ↓
Reducer receives the action
        ↓
Redux updates the state
        ↓
React receives the new state
        ↓
The UI updates
```

## Redux Store

The Redux store is created in:

```text
src/store/store.ts
```

The store uses the `rootReducer` to manage the application's state.

Redux Logger middleware is also added to the store. This allows Redux actions and state changes to be viewed in the browser console while developing the application.

## Actions

The counter actions are located in:

```text
src/store/actions/counterActions.ts
```

The application has three actions:

```text
INCREMENT
DECREMENT
RESET
```

These actions are dispatched when the user interacts with the counter buttons.

## Reducer

The counter reducer is located in:

```text
src/store/reducers/counterReducer.ts
```

The reducer manages the counter state and determines how the state changes depending on the dispatched action.

The initial counter value is:

```text
0
```

The reducer returns a new state instead of directly changing the existing state.

## Combined Reducers

The application's reducers are combined in:

```text
src/store/reducers/index.ts
```

The `combineReducers` function creates the root reducer used by the Redux store.

The current Redux state has the following structure:

```text
state
└── counter
    └── value
```

## Connecting Redux to React

The Redux store is connected to the React application through the `Provider` component in:

```text
src/main.tsx
```

The `Provider` makes the Redux store available to React components throughout the application.

The `Counter` component then uses:

* `useSelector` to read the counter value
* `useDispatch` to dispatch actions

## How to Run the Project

### 1. Clone the repository

```bash
git clone https://github.com/Betelhemf567/react-redux-app.git
```

### 2. Move into the project folder

```bash
cd react-redux-app
```

### 3. Install dependencies

```bash
npm install
```

### 4. Start the development server

```bash
npm run dev
```

Open the local URL shown in the terminal to view the application in your browser.


## Learning Outcome

This project helped me understand how Redux can be used to manage state outside individual React components.

Through this activity, I practiced:

* Creating a Redux store
* Creating actions
* Creating reducers
* Combining reducers
* Connecting Redux to React using `Provider`
* Reading state using `useSelector`
* Updating state using `useDispatch`
* Using middleware with Redux Logger
* Managing state with TypeScript

The project also helped me understand the flow of data in Redux and how actions, reducers, the store, and React components work together.

````

