Higher Order Components:  
A function that takes a component and returns a component.  Takes the component, enhances/modifies the component(adds some features), and returns it back.  
Higher Order Components are Pure Functions. They don't change the existing behaviour of the input Components but they will just enhance the input Components.  

<br>

Let's take the Promoted Restaurant cards in Swiggy. So, it looks like other cards but has a Promoted label on it. So, we are going to enhance the Restaurant cards using Higher Order Components.  
Here, we have taken the RestaurantCard component and included the Promoted label to the restaurants with rating > 4.6. So, we've passed RestaurantCard as input. Since a higher order component returns a component, and a component is nothing but a function, withPromotedLabel component returns a function(a component). And inside that, we've included the Promoted label on the RestaurantCard. Since, the component inside the higher order component needs its props to get displayed we've received it in the return function and used a spread operator in the RestaurantCard component to pass all the props as individual props to the RestaurantCard component. If we don't use the spread operator all the props will be passed as a single prop to the component.  

![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/f27b6313-10f6-47ac-ac56-b70b28733121)


The RestaurantCard displayed in withPromotedLabel also needs props to get displayed, so we've passed props to RestaurantCardPromoted as well. Refer the below image.

![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/b765e9ff-2225-48a6-ab4b-4460d251a24d)

This is how we use the higher order component in the imported file.  
![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/28104209-3a6f-4dff-8acd-8fb1acf6d308)

<br/>

React applications has two layers: UI layer & Data layer.  
UI layer(JSX) is powered by Data layer. [UI layer - JSX]  
Data layer consists of States, Props etc. [Data layer - States, Props]  

<br/>
React Dev Tools extension:  
Components Tab - Gives a representation of all the components used in that page. We can say its a Representation of the Virtual DOM on the left side. And when clicked on any component, displays the Data layer i.e the State variables and hooks used in that component.  
Profiler - Records the React application and tracks the actions we perform while recording.  

<br/>

Lifting State Up [State lifting to the Parent]:  
The parent component has the state control of its child component. We pass the state as a prop to the child component from the parent component.  

<br/>
Controlled and Uncontrolled components:  
Uncontrolled: A component has its own state.  
Controlled: A component's state control is with another/Parent component giving it the power to control its child components. Relies on its parents to tell what to do.  


<br/>

Props drilling:  
READ ABOUT PROPS DRILLING IN REACT DOCS...
React is a one way data stream[top to bottom]. Let's say we want to send a prop from the topmost level component to its 10th or 11th level child. What we do is we pass the prop from the top most level to its child. then to its child and so on till 11th level. But is this correct? the components in-between doesnt use that prop but simply passes it. This is not a good way. This is known as Prop drilling.  

So, in larger applications this will be a common scenario and we cant pass props like above. For this React provides us with REACT CONTEXT.  

<br/>

React Context:  
Prop drilling is the problem and React Context is ONE OF THE solutions for it.  
We keep data in a Global/central place and anybody can access it. [DO NOT USE the WORD Global object in INTERVIEWS]  
React gives us access to a utility function createContext which comes from react library. We can use this Context anywhere in the project using useContext() Hook.  
We can have as many Contexts as we want to.  
Only keep data that is used in multiple places in the app or the data you think will be used in multiple places in Context.   
Let's take a LoggedIn User name for example which needs to be shown throughout the app in different places and we need to access it from anywhere in the app. We hold this data in a Context and use it anywhere in the app.  
![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/ceaec97a-7d85-4f5a-a919-b0b0e1076783)  

To use a context,  
![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/5e4c5a81-92cb-4f97-868c-9ff5698d2fdb)  
![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/643343fe-e9a3-44b0-a743-b5995d9043b8)  
![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/c8b93714-2aca-4790-9b49-be52db354027)  


Using Context in Class-Based Components:  
In class-based components, we do not have hooks. So to access it using <UserContext.Consumer> component. It has a function that helps us to access the current Context values.  
![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/868e9e50-d66d-49c0-9ac6-98a202bcd038)


