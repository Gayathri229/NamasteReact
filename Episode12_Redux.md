REDUX is not Mandatory.  
REDUX and REACT are different libraries.  
REDUX is not the only library to maintain state. We have Zustand(Recently gaining popularity).  
Redux is primarily used for handling state of the application. Offers easy debugging.  

<br/>

Redux offers 2 libraries:  
React-Redux - kind of a bridge between React and Redux  
Redux Toolkit - New way of writing Redux(Current and Standard way used in Industry). The older way is called Vanilla Redux.  

<br/>
Redux ToolKit Architecture:  

Redux Store - A Huge JS Object with data kept in a Central/Global place.  
Is it a good practice to keep all the data inside one Object? Yes. But it shouldn't become very big and clumsy. So, to avoid this we have Slices inside our Redux Store.  
Slice - small portions of Redux Store.  
We create multiple Slices inside our Redux Store. 
What can be different Slices? We make Slices based on logical partitions (Logical separations are Slices).  
Eg: We can have a separate slice for Cart Data, a separate slice for logged-in user data, separate slice for Theme/UI related data.  

![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/9a98ecf8-bfa2-4bc5-8317-9176204c6d1d)  

Now, let's take an example from our App to use the Redux ToolKit and build the Cart feature. So, if we click on the Add button for any item in a Menu it should reflect in the Cart. Let's say we have a Slice for Cart. 
How does the Data go into the Cart Slice?  We can't add data directly into the Cart Slice. Redux doesn't allow this.  
When we click on the Add button, it DISPATCHES an ACTION. The action calls a FUNCTION(REDUCER function). And this Reducer function internally modifies the Cart/ Cart Slice of the Redux Store.  
The function is known as a Reducer.  
![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/1a933a46-4682-4c57-a561-c31a32641aa2)  

What we saw above is how to write data.  
How to READ data from a Slice?  
We use a SELECTOR. The Selector will read the data from Redux Store and the Selector will update/modify the React Component. Using the SELECTOR is known as SUBSCRIBING TO THE STORE. When we say subscribed to the Store, it means the React Component(in this Eg, Cart/Cart component) is in SYNC with the Store. If the Data in the Store changes, the Cart component will update automatically.  
We can say that the Cart in the Header has SUBSCRIBED to the Store using the SELECTOR. And because of this, the item count in the Cart changes automatically when we click on the ADD button.  
![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/3cde01cb-558a-4f2e-9847-84635e90160f)  

<br/>

![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/84656ce1-5fa3-4d3a-a0a0-5f19a45a6a9c)


Commands to install redux toolkit and react-redux:  
npm install @reduxjs/toolkit  
npm install react-redux  
<br/>

Now let's build our Redux store:  
configureStore() function which is provided by the Redux toolkit helps us to create a store.  
Now, we've to give/link the Store to our application. Provider component given by react-redux will help to link the store and our application. We wrap the whole app in the Provider component with store as a prop and pass the "appStore" as the prop value. We can also wrap only a part of the code with the Provider component where it is needed alone as well.  
Note: React-redux helps in bridging the store and app. Redux toolkit helps in creating the Store.  
![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/1816e3e3-14b6-4f4a-b980-815fc7838d32)  

Now, to create a Slice, we use the function createSlice given by Redux toolkit. The createSlice function takes few configurations for a Slice like name, initialState(Object), actions, and reducers(Object).  
Reducers - reducer function corresponding to each action(say add/remove item, clear cart)  

![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/ebc08873-1aa3-4d1d-8286-266f3b768a79)  

Now, we add the Slice to the Store. The store also has a reducer which is responsible to modify the app store. And it consists of reducers from all the different Slices in the app.  
![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/8a24ed0f-3046-4cee-be01-4c42cd5f9e21)  

How will we Read those values from the Store(Cart Slice)?  
Using the Selector Hook. React-redux gives us a Selector Hook to Subscribe to the Store. It also helps to identify what portion of the Store we need. In useSelector hook we can directly access the store, as Redux provides support for it. 

![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/faa5a78d-9e27-4b6d-a65e-65384c8fda86)

Now, let's move to adding the items to the cart when user clicks on add button, 
When user clicks on the ADD button, we need to dispatch an action. React-redux provides useDispatch hook for this. And we use the actions we created in the Slice and pass the item as a payload(Refer the below image). So, when we create a payload, Redux creates an Object out of it (something like {payload: "pizza"}). So the action.payload we used in the Cart Slice addItem Action will be Pizza here. And the argument order doesn't matter here as Redux takes care of it in the background.  

Behind the Scenes:  
So, now when we click on any add button, pizza gets added in the Cart. When Add button is clicked, addItem action is dispatched with Pizza, item is getting pushed in the Cart through reducer function and Slice in the store gets modified. And since we've subscribed to the store using Selector in Header, Cart gets updated with the item count.  

![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/fb0cc8b8-eeab-4841-9a21-e826f957ab30)  
![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/6a1c0151-efd3-4f61-a547-250522f235b0)




MISTAKES WE MAKE IN A REDUX STORE:  
<br/>

1. ALWAYS NAKE SURE TO SUBSCRIBE TO THE CORRECT PORTION OF THE STORE. IF NOT DONE CORRECTLY WILL LEAD TO BIG PERFORMANCE LOSS.  

![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/b40ffdf9-ff4a-4f0b-b86b-fea41299f3b2)  

![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/98612db8-6640-49b3-892f-aeaa6ceacff0)  

1st and 2nd image works the same. But in the first one we've only subscribed to the Cart slice of the Store.  
And in the second one we've subscribed to the whole Store and from that we've extracted the cart slice. So, now when anything changes in the Store, the Cart component will also get affected. Let's say a User logged in, so the default user name Slice gets affected and since we've subscribed to the whole store in Cart, the Store in Cart component also gets the update which is unnecessary. NEVER DO THIS. IT IS INEFFICIENT.  


2. Difference between Reducer and Reducers.
  A Store always has one BIG REDUCER for the WHOLE APP and within that it will have multiple small Reducers of different Slices. So, here the keyword is REDUCER.  
   ![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/a8d03c64-64bb-4f49-a36e-8f28382599bf)  

  When we write it in a Slice, we create multiple REDUCERS. Keyword here is REDUCERS.  
   ![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/c0b3f7fa-c668-4a6b-bff8-7a5c5593da8d)  
   
  And when exporting Reducers from a Slice, we export A Reducer which is a combination of Small Reducer functions which means it is ONE Reducer for that Slice.  
  [Image of exporting Reducer from Cart slice]   
   ![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/dad88a4d-b5cf-49c1-99cb-728836fff4aa)  


3. Vanilla Redux vs Redux Tool kit:  
   In Vanilla(Older) Redux State was not mutable i.e. can't change/modify state directly. A copy of the state variable(newState) was created and then newState was changed. Returning State is mandatory.  
   [Older way of mutating state]  
   ![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/ccbc6204-3f37-459c-940b-1e6593b37827)  

   In Redux Took Kit, we HAVE to MUTATE the state which makes it impure function. Returning State is not mandatory. Redux takes care of it automatically.  
   Behind the scenes, Redux is still creating a Immutable state and works the same as Older Redux, but doesn't ask the Dev to do it. Redux uses the "Immer" library to do this. It finds the difference between the Original State and the Mutated state and gives a new State/new copy of the State that is Immutable.  

   
5. Why state = [] doesn't work?  
   





