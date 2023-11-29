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
