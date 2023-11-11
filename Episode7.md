useEFfect() DIVING DEEP:  
  
Every time the component renders, useEffect will be called(default behaviour). Dependency array changes the behaviour of useEffect. 
Dependency array is not a mandatory param.  

no dependency array => useEffect is called on every component render/ re-render 
if dependency array is empty [] => useEffect will be called on initial render (just once)  
if dependency array is given a value => useEffect will be called everytime when the value is updated  


useState():  

Never create state variables outside your component.  
Used to create Local state variables inside functional components.  
Always call it on the top of the component(in code).  
Never create useState variable inside if else/for loops/functions/condition. Can creact inconsistencies.  


Routing:

Whenever we develop routes, we've develop a routing configuration.  
Configuration - information that will define what will happen in a specific route/ that will tell the browser router what will happen in a specific path.  
createBrowserRouter takes list as an argument. Here we mention the list of paths. 
Path is an object
Once we define the paths, we need to render it to the screen. This will be done by ReactProvider which is a component, that will provide the routing configuration.  
There are many routers but createBrowserRouter is the recommended one for React Projects.  
React router dom gives us access to a Hook useRouterError


