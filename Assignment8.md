1. How do you create Nested Routes react-router-dom configuration?  
   We can create Nested Routes using the children array in the createBrowserRouter object. Here we can mention the path of the URL in the path parameter and the component that has to be displayed in that path, in the Element parameter.  

2. What is the order of lifecycle method calls in class-based components?  
   Constructor => Render => DOM updation => Component Did Mount => Render => DOM updation => Component Did Update => Component Will Unmount.  

3. Why do we use componentDidMount?  
   componentDidMount is called after the initial rendering with dummy data. Because of this, we make API calls in componentDidMount, so that after the initial render page gets filled with the actual API data to give a better user experience.  

4. Why do we use componentWillUnmount? Show with example.  
   componentWillUnmount is used to perform clean-up tasks for a component. For eg, Let's say we've set an interval in a component, when this component gets replaced, we can see the UI working properly, but behind the scenes the interval keeps running leading to memory leaks and performance issues, so to avoid this we use the componentWillUnmount method to clear the interval. It is also used to free up any resources used/ to clean up side-effects such as eventListeners etc.

5. (Research) Why do we use super(props) in the constructor?  
   Super keyword helps to invoke/initialize the parent class which helps to inherit the functionalities of the parent class. Using the super keyword for props helps to access props anywhere inside the class using "this" keyword.

6. Why can't we have the callback function of useEffect async?  
   Having useEffect callback function as async will return a Promise to the return/cleanup function. The callback function expects a return function or nothing at all. So when a promise is returned either will not be handled properly or leads to unexpected behavior. This also leads to the return function never being called which can cause unnecessary errors.  
   
7. Read about createHashRouter and createMemoryRouter from React Router Docs.  
   createHashRouter - Uses the portion of url after the # to represent different routes. It is used when we are unable to configure web sever to direct all the traffic to the React application.
   createMemoryRouter - Manages it's own history stack in the memory instead of using browser history. Navigation doesn't affect the browser URL, making it suited for scenarios where the state change in page doesn't need a URL change.  
   
   
