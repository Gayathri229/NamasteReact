1. What is JSX?  
     JSX is an extension to Javascript syntax that makes it easier to create React Elements due to its HTML-like syntax. It is a convention where we merge JS and HTML together.  

2. Superpowers of JSX.  
     It helps to escape cross-site attacks.  
     Makes the code readable.  
     Helps with Component composition, Element in a Component, Component in an element.

3. Role of "type" attribute in script tag. What options can I use there?  
    The "type" specifies the content type of the script.  
     - text/javascript - default value for type  
     - module - to refer to ECMA script module in JS. Way to structure JS code into separate files and export/import functionality between them.  
     - text/html - to embed html content  
     - application/json - to embed json data  
     - text/css - to embed css styles  
     - text/x-template - to embed client-side templating libraries.
  
4. {TitleComponent} vs {<TitleComponent/>} vs {<TitleComponent></TitleComponent>}  
     {TitleComponent} - {} displays/executes any JS code. So here, TitleComponent is considered as a JS code/expression.  
     {<TitleComponent/>} - is used to render a functional component  
     {<TitleComponent></TitleComponent>} - means the same as 2nd one and is used to render a functional component  
