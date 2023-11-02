1. Is JSX mandatory for React?  
     JSX is not mandatory for React, it's a syntax extension of JavaScript. But it's highly recommended as JSX makes it easy for the readability of code, we can define complex code structures easily as it resembles HTML.  

2. Is ES6 mandatory for React?  
     ES6 is mandatory for React as we have many functionalities like arrow functions, classes, let and const etc. It is not mandatory to use ES6 but doing so makes it easy for us to take advantage of the language's capabilities.  

3. {TitleComponent} vs {<TitleComponent />} vs {<TitleComponent> </TitleComponent>}  
     {TitleComponent} - Used to display a piece of Javascript code.  
     Eg: const price = 1000;  
         <h2> {price} </h2>  

      {<TitleComponent />} - Used to display a React component in JSX.  
       Eg: const TitleComponent = () => {  
             return (<h2> Heading </h2>);  
           }  

           const App = () => {  
           return (<div>  
           <TitleComponent />;  
           </div>  
           );  
           }  

   {<TitleComponent> </TitleComponent>} - Used to display a React Component when it has a child, but it is an unusual way of structuring a component and doesn't promote readability.  


4. How can I write comments in JSX?  
     /* */ - to comment multiple lines  
     // - to comment on a single line  

5. What is <React.Fragment> </React.Fragment> and <> </>?  
      <React.Fragment> </React.Fragment> is used when we need to return multiple elements from a component but don't want to wrap them in a container div or any other HTML element.  
     Eg: function MyComponent() {  
  return (  
    <React.Fragment>  
      <p>This is a paragraph.</p>  
      <button>Click me</button>  
    </React.Fragment>  
  );  
}  

 <> </> - is a short hand property for <React.Fragment>.  


6. What is virtual DOM?  
     Virtual DOM is a lightweight tree structure that mirrors the actual DOM structure. In a React application, when a component needs to be rendered a new Virtual DOM tree is created representing the updated UI. It then compares with the actual DOM and calculates the minimum changes required to update the real DOM.  

7. What is Reconciliation in React?  
     Reconciliation helps to provide an efficient and optimized rendering process. It compares the actual DOM and the new virtual DOM 


8. What is React Fiber?  


9. Why do we need keys in React? When do we need keys in React?  
   Keys help us with optimization when we display/render elements in UI. Keys are for Unique Identification of elements to identify which element has been added last and display that element alone along with other existing elements. Else DOM re-renders all the elements again which takes a huge hit in performance.  

10. Can we use Index as keys in React?  
    We can use Index as keys in React but it's not highly recommended. In the absence of Unique keys, Index can be the second option for keys.  
   
11. What are props in React?  
    Props are used to pass dynamic values to components/from one component to another to make them dynamic and reusable.  

12. What is a Config-driven UI?  
    Controlling how our UI looks based on data/config. This helps with Dynamic UI rendering with reusable and customizable code.  
         Eg: In the Swiggy app, we get the list of restaurants to be displayed from backend API. This data controls what is displayed in UI through our dynamic components.  
             
         
     

       
   
     
           
