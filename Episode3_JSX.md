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

Any React component should be named starting with the CAPITAL LETTER.  
A functional component is nothing but a JS function that returns a JSX Element/React Element. It can return a bunch of React elements as well.
![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/0341448b-8557-43eb-b690-3b6e73f71ca8)


Syntax to render a Functional Component:  
root.render(<HeadingComponent/>);  
This is how Babel understands it. When Babel sees the Angular brackets, it understands it might be a component. 

Both HeadingComponent1 and HeadingComponent2 are the same. When we use curly braces, it is mandatory to use return. When no curly braces are used return should not be used.  
![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/207935a8-1324-43fb-9250-6a49cd3958ef)

We can also use normal function as well for Functional Component,  
![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/9adcc664-450d-4807-9d26-7a6832cb4b14)

What if I want to render a Functional component into another Functional Component?  

We just declare a Functional component and include it in the Functional component we want, as below. This is also called COMPONENT COMPOSITION.  
![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/acb8c275-2ced-40e6-a8f3-fe9127778108)

![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/43073f14-a113-4847-ba9c-55f88ef75cd2)

We can also write the above like this,  
![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/aa3b3c94-9ecd-401f-90f7-c10cdcc11472)



We can incorporate ANY JS CODE inside JSX using curly braces "{}". Whatever we put inside these curly braces, gets executed. This is a VERY IMPORTANT CONCEPT. 
![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/a155e7f9-dae7-4060-be5c-c28e113ab33e)

![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/1dcf7cdb-3fa9-4c88-b37d-2204ee4c7e0a)

What if we get an attack through the code we inject through curly braces, let's say I get data from an API, but it contains some code to get my local storage or something dangerous, JSX escapes these kinds of attacks and then only executes the code inside {}. It prevents cross-site attacks for you. JSX has this POWER.


In the same way, JS elements can also be put inside JSX. Example below,   

![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/aa83cda4-c93b-4d55-992d-2a6d56d4ae64)

![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/e4f25247-29a3-4596-a53a-26730b81a6fe)



We can have a Component inside an Element as well.  
![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/ece6930b-cee9-4c65-9dca-7d18c61ab2dc)

Here, we can see div container is inside the h1 tag i.e. Title Element.  
![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/ca18e807-35ad-4ec1-b6db-e44c99ad1bda)



We know that a Functional Component is nothing but a JS function. So, we can write any JS code inside {}. This means, we can also write a functional component like this,

![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/b67b12d2-1e54-4805-b252-3a0dc83300a8)


JSX IS MAKING OUR CODE READABLE.

