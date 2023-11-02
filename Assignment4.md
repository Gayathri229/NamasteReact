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
     
   

       
   
     
           
