Best practices for coding/maintaining clean code:
  - Separate files for separate components.  
  - All the main code should be under the "src" folder.
  - https://legacy.reactjs.org/docs/faq-structure.html  
  - For a file with a component, try to match the file name exactly as the component name. File name: Header.js, Component name: Header.
  - Using .js or .jsx extension when naming files doesn't matter.
  - 

If we move the component to a separate file, we should export the component from the new file and import it to the file where it is used.  

Here, I've exported Header from Header.js, 

![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/eed50713-de91-439e-a7d3-03f103cd10d0)

And imported it into App.js file. While importing the file, we can or cannot use the ".js" extension, it works the same for both. React identifies the file as JS file with or without extension.  
![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/9e327476-0026-4487-bb9c-7004f451a596)
  
  
HARDCODED CODE'S PLACE:    
You never keep hardcoded data in components file. It's kept in Config/Constants/utils file


EXPORT AND IMPORT:  
We have two types of export and import. Default and named import/export. A file can have only ONE DEFAULT export. 

Eg: Named export  
![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/d35705d3-85bd-4595-a2fe-84b4163ba374)

Eg: Named import. We have to use curly braces to import named exports.  
![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/ff816b75-cc42-43ab-a745-601f6cf2319b)



Eg: Default export  
![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/50cdbbab-f90c-46a6-b028-0a57679bd3e6)

Eg: Default import  
![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/0308e30c-7de7-49e5-bd77-c4f962ea4a53)


IT IS NOT GOOD PRACTICE TO USE NAMED EXPORT FOR COMPONENTS. USE NAMED EXPORT ONLY WHEN YOU HAVE TO EXPORT MULTIPLE THINGS.  
![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/ae42953a-9aaf-4caf-bd9e-26715b2a286a)
  
  
  

HOOKS:  
- To keep the DATA AND UI layer consistent/in sync.   
- If Data changes UI layer changes.   
- React updates DOM efficiently.   
- State variable -> state of the component?  
- A normal JS utility function, Pre-built.
- There are multiple hooks in React  
- Import as named import  

2 Important Hooks are:  
- useState()  
- useEffect()
  

    
useState():  
  
- used to create State variables.  
- Maintains the state of the component.
- A Local state variable's scope is inside that component.
- const [listOfRestaurants] = useState(); -> this is how we create a State variable. Whatever we pass inside the brackets will be its default value.
    Eg: const [listOfRestaurants] = useState([]); -> here empty list is passed as default value.
- to use this variable, we can use it like a normal variable.
- How to modify this variable? -> We have a second parameter when we create the variable which takes the name same as the state variable but with "set" as prefix. We can name it anything but for industry convention, we name it the same as the state variable. This is a method. Whenever we want to change the state of UI, we pass the modified data to this function.  
  Eg: const [listOfRestaurants, setListOfRestaurants] = useState([]);  
  Let's say I want to make the listOfRestaurants empty,  
  setListOfRestaurants([]); -> this will do it.


Whenever a State variable updates, React re-renders the components. React is efficient with Re-rendering[super power of react]. 



Reconciliation Algorithm[React Fiber]:  (Was introduced in React16)
Whenever something changes on the UI, it's called Reconciliation. 
React Fiber new way of finding the diff and updating the DOM. 

React creates a Virtual DOM[not an actual DOM] of UI. Virtual DOM is a representation of the Actual DOM. 

Actual DOM:
<div>
  <h1>
    <img>
  </h1>
</div>

Virtual DOM:
The Object we get when we create any React Element. 
Eg: We've printed the content inside Body tag of the app here. We get an Object printed in console. This JS Object is the Virtual DOM. 
![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/ff1fe04f-212f-4be6-9f2c-8f28a1f374ff)


Diff Algorithm: 
Finds the difference between the updated Virtual DOM and previous Virtual DOM. 

Let's say, there are 7 cards, we clicked a button, (now a new Virtual DOM/ new Object is created) and only 4 cards have to be displayed. It compares the updated Virtual DOM and the old virtual DOM and calculates the difference[i.e. 4 cards here] and then actually updates the DOM on every render cycle. React doesn't touch the DOM much. This makes React FASTER because it does Efficient DOM Manipulation. This happens every time the State variable changes. React keeps monitoring the State variable. So, the second param of the State variable is the trigger for React to start the diff algorithm. 

Virtual DOM was not introduced with React. This concept existed far before, this was taken and React algorithm was built upon the Virtual DOM.

Core of React Algorithm: Because it has Virtual DOM. It can find out the Diff and manipulate DOM efficiently.
