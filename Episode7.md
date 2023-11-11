useEFfect() DIVING DEEP:  
  
Every time the component renders, useEffect will be called(default behaviour). Dependency array changes the behaviour of useEffect. 
Dependency array is not a mandatory param.  

no dependency array => useEffect is called on every component render  
if dependency array is empty [] => useEffect will be called on initial render (just once)  
if dependency array is given a value => useEffect will be called everytime when the value is updated  


useState():  

Never create state variables outside your component.  
Used to create Local state variables inside functional components.  
Always call it on the top of the component(in code).  
Never create useState variable inside if else/for loops/functions/condition. Can creact inconsistencies.  
