1. What is Prop drilling?  
   Passing the data from a Parent component to its child component which is on the nth level. n denotes say 10th or 11th level. So since the child is on the 11th level or more than that, and the Prop comes from the top most level, we need to pass the data through other 10 components which doesn't use it. This is called Prop drilling.

2. What is lifting the state up?  
   Moving the state variable of the child component to its parent component. This is done so that the child/multiple components can share the state to maintain controllability/synchronize their state. Then the state is passed as Props to the child component.  

3. What are Context Provider and Context Consumer?  
   Context Provider component is used to update the values in a Context through the "value" prop.  
   Context Consumer component is used in class-based components to access the values in a Context through a callback function.

4. If you don't pass a value to the Provider does it take the default value?
      
