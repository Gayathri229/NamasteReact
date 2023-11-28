1. What is Prop drilling?  
   Passing the data from a Parent component to its child component which is on the nth level. Sometimes we need to pass down data from one component to another through multiple nested levels of components until we get to the component where the data is needed. Here, we are unnecessarily passing props to components that never need them. This is called Prop drilling.  

2. What is Lifting the state up?  
   Moving the state variable of the child component to its parent component. Here, the power of managing the State variable is not given to the Child component. This is done so that the child/multiple components can share the state to maintain controllability/synchronize their state. Then the state is passed as Props to the child component. Eg: Accordion  

3. What are Context Provider and Context Consumer?  
   Context Provider component is used to update the values in a Context through the "value" prop. This data will override the default context value.  
   Context Consumer component is used in class-based components to access the values in a Context using a function we wrap in the component.  

4. If you don't pass a value to the Provider does it take the default value?  
   - Provider doesn't take the default value when value is not passed. Instead, it throws a typeError saying the value is undefined.
     ![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/cb7da09f-8415-42c3-81cc-c018a8d11d24)  

     ![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/443ef73f-efc8-4841-9c8e-b7b2c4f18b20)  

   - If we don't use the Provider component itself, then it takes the default value. Let's take the below code as example for this second point.  

In the below code, I've displayed the Header twice with the Provider component & value passed and without the Provider component. Here, loggedInUser value is being used in the Header component.  
![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/eac47036-d1bd-493a-a386-da12fb1e8fcc)

As we can see here, the first Header has taken the passed value and the second one has taken the Default value.  
![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/85157b93-363c-4cb5-983b-91ed91221109)  

So, this means we need to pass the value prop when the Provider component is used. Provider doesn't work without the value prop. When we use Provider, it means we're updating the default context value, so when we don't pass the value to be updated, it throws an error as the expected value i.e the updated value is not present (For my understanding)  
