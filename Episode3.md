If we want to run the project, we give the command "npx parcel index.html". But we can also do this by putting the command in package.json file under scripts field. We can name it as anything we want and give the command under that, say  
scripts : {
"devBuild": "parcel index.html",
"prodBuild": "parcel build index.html"
}  

Now we can use the command "npm run devBuild" for building dev build and "npm run prodBuild" for prod build. Here, if we named our devBuild command as "start", we can use the command "npm start" for the dev build command. start is the keyword reserved by npm for this. Same command wont work for any other names.

JSX  

JSX is a Javascript syntax that is easier to create React Elements.    
JSX is NOT a part of React.  
JSX is a convention where we merge JS and HTML together.  
JSX is NOT HTML in JavaScript. JSX is HTML LIKE / XML LIKE Syntax.  

The JSX element when printed is the same as the React element when written with React core i.e a JS object. So both are objects. Only when rendered is getting converted into HTML element.
![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/b856c808-7822-4344-9150-e9c222b21508)


JS Engine doesn't understand JSX. It only understands ECMAScript6/JS.
Before the code goes to the JS Engine JSX is transpiled(converted) to React code by PARCEL. So JS Engine gets the code that is understandable by browsers.  
This code conversion is done by the BABEL package.  
BABEL also converts ES6 code for old browsers to Simple JS as some old browsers only understand Plain JS.  

JSX => React.createElement => React Element => JS Object => HTML Element when rendered  
const jsxHeading = <h1 id="heading"> Namaste React by JSX! </h1>;

This is why we got the same object when we printed both JSX Element and React.createElement


If we have to use Attributes in JSX, it should be in Camelcase.  
Eg: <h1 tabIndex=1> </h1>

For class attribute in HTML, should use "className" in JSX.

HOME WORK: Explore various attributes of various tags in JSX. Eg: <img src="">, <a> etc...


If we want to write JSX code in more than one line, it is mandatory to wrap those lines in round braces.
Eg: ![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/13bc6d5b-0e8b-49f5-8625-d01a5f3c78a7)


REACT COMPONENT:  
Two ways to create a React component:  
Class Based Components - OLD  
Functional Components - NEW  



FUNCTIONAL COMPONENT:

Any React component should be named starting with the Capital letter.  
A functional component is nothing but a JS function that returns a JSX Element.  
![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/0341448b-8557-43eb-b690-3b6e73f71ca8)

