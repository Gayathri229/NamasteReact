1. useContext vs Redux.  
   useContext: useContext is provided by React to access data from a Central place in the app. Context can be used for small and medium-sized applications.  
   Redux: Redux is an external state management library which also allows data to be accessed from anywhere in the app. Redux provides scalability for Huge applications.  

2. Advantages of using Redux Toolkit over Redux.  
   - Reduces boilerplate code. RTK provides utilities like createSlice and configureStore which reduces the boilerplate code needed to setup Redux.
   - Configuring the Redux Store was too complicated. Redux Toolkit doesn't require configuration.
   - Redux needed a lot of packages but Redux Toolkit doesn't

3. Explain Dispatcher.  
   The dispatcher is responsible for triggering the actions that are dispatched to update the Redux Store when user performs any action that needs the Redux Store updation.

4. Explain Reducer.  
   A Reducer is nothing but a function which is responsible to modify the Cart/Cart Slice of the Redux Store internally.

5. Explain Slice.  
   Since Redux Store is a Huge JS object, to avoid all the data being placed in a Single Object, we make Logical partitions to store the data which is known as Slice.  
   It is a combination of Reducer functions and actions. A slice encapsulates a portion of the Redux state along with the logic to update that part of the state.

6. Explain Selector.  
   A Selector is used to read data from the Redux Store and to update/modify the React component. Using Selector to read data is called Subscribing to the Store.

7. Explain createSlice and the configuration it takes.  
   createSlice is a utility function provided by Redux Toolkit that simplifies the process of defining Redux reducers and actions.  
   We give the name of the Slice and its initial state if any.  
   Reducers, where keys are Actions and values, are functions.  
   extraReducers (builder function): The extraReducers option is a function that takes a builder object as its argument. This object provides methods for adding additional reducers. These reducers can handle actions from other slices or async actions. The addCase method is used to add reducers for specific action types, and addDefaultCase is used to handle any other actions.  

<br/>

   extraReducers: (builder) => {
    // Additional reducers for handling actions from other slices or async actions
    builder
      .addCase(someOtherAction, (state, action) => { /* ... */ })
      .addDefaultCase((state, action) => { /* ... */ });
  },
<br/>
The createSlice function returns an object that includes the generated reducer function and action creators. 
   
