1. What are various ways to add images into our App? Explain with code examples.
   - Using 'import' statement [path mentioned is relative to the file & when used in single component]  
     Eg: import greenStar from "../../images/Green_star.svg";  
     
   - Using 'require' for dynamic imports  
     Eg: <img src={require('./my-icon.png')} />  

   - Using public folder when an asset is used across different components [serves as static asset]  
     Eg: <img src="/images/logo.png" alt="Logo" />  
     
   - Base 64 encoded images [We can convert images to Base64 and use it]  
     Eg: const base64Image = 'data:image/png;base64,iVBORw...';  
     <img src={base64Image} alt="image" />  

   - Using background images in CSS  
     Eg: background-image: url('./images/background.jpg');  

2. What would happen if we do console.log(useState())?  
   We are getting a list of objects where one has the name dispatchSetState and has some arguments.  

4. How will useEffect behave if we don't add a dependency array?  
   Dependency array is optional but not adding it lead to useEffect getting rendered each time the component re-renders which results in performance issues and doesn't provide a good user experience.  

5. What is SPA?  
   SPA stands for Single Page Application. React helps to build Single Page Applications, as it's just an exchange of components as it relies on Client Side Routing where the whole app is loaded initially and the components are updated dynamically when the user interacts with the app.  
   
7. What is the difference between Client Side Routing and Server Side Routing?  
   Server Side Routing:  Makes an API call to fetch the mentioned file and reloads the entire page to display the new content.  
   Client Side Routing: Refreshes the components alone as all the components are already present when the app is loaded for the first time and the transition looks smoother than Server side rendering.  
   
