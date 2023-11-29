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
Is it a good practice to keep all the data inside one Object?  
Yes. But it shouldn't become very big and clumsy. So, to avoid this we have Slices inside our Redux Store.  
Slice - small portion of Redux Store.  
![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/9a98ecf8-bfa2-4bc5-8317-9176204c6d1d)  
