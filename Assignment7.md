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

3. How will useEffect behave if we don't add a dependency array?
   The mentioned element will get rendered each time the component re-renders which results in performance issues and doesn't provide good user experience.  

4. What is SPA?

5. What is the difference between Client Side Routing and Server Side Routing?
   Server Side Routing:  Makes an API call to fetch the mentioned file and reloads the entire page to display the new content.
   Client Side Routing: Refreshes the components alone as all the components are already present when the app is loaded for the first time and the transition looks smoother than Server side rendering.  
   
