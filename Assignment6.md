1. What is a microservice?  
   Microservice is an architecture where there will be small services which has its own responsibility which can be scaled/deployed independently from other services. Microservices can communicate with each other through APIs. They are used to build complex applications.  

2. What is a monolith architecture?  
    Monolith architecture is a traditional architecture where all the components, modules, functionalities are placed in a single container. It becomes difficult to scale them as the whole application has to be scaled even when few components require scaling. Small changes in few parts of the application may result in testing out the whole application.  
   
3. What is the difference between microservice and monolith architecture?  
   Microservice:  
   - loosely coupled  
   - Easy to maintain, test, scale, etc.  
   - Each service is independent of each other.  
  
  Monolith:  
  - Tightly coupled  
  - The whole application is integrated into a single unit.  
  - Not easy to scale/test/maintain  
  - Changes in one part of the system have ripple effects on other parts as well.  

4. Why do we need a useEffect hook?  
   useEffect hook is used to give a better userExperience. It is used to render anything without disturbing the initial/primary rendering so that it doesn't disturb the render cycle. It has a dependency array, changing the dependencies trigger the effect. We can use it for api calls, timeouts etc.  

5. What is optional chaining?  
   ? is the Optional chaining operator. We use it when accessing properties/calling methods , if the object is undefined or null or doesn't have the expected value in the object it helps to handle the error gracefully and throws an undefined error. Helps to make our application less error prone.  

6. What is Shimmer UI?  
    Shimmer UI helps with better User Experience. When the page is in loading state, instead of making the user look at a blank screen we display a fake/look alike components on the page which resembles the page giving a feeling that the page has about to load quickly when it is in loading state.  

7. What is the difference between JS Expression and JS Statement?  
   JS Expression - Produces a value. Eg: 2+3.    
   JS Satement - Performs an operation. Eg: var x=5. Here, it assigns 5 to x.  

8. What is conditional rendering? Explain with a code example.  
   When we want to display any component under a condition. Let's say when we toggle a button a paragraph should be displayed.  
   <div>  
     <button onClick = {() => {  
       paraVisible===true ? setParaVisible(false) : setParaVisible(true)  
     }}>Toggle</button>  
     {paraVisible && (<p> Toggled Para </p>)}  
    </div>  
  
   Here, we are displaying the paragraph under the condition when paraVisible is set to true.  
  
9. What is CORS?  
    Cross-Origin Resource Sharing - communicate/request for a resource from one domain to a different domain. The server hosting the resource can specify the origins which are allowed to make a request using the HTTP headers in responses. When we make a request to a domain, from which requesting is not included/allowed in the requested origin, origin mismatch error will be thrown.  
   
