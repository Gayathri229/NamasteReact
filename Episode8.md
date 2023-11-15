Class based components:  

This is the older way of creating components.  
In interviews class based components are asked.  

A class based component is nothing but a normal Javascript class. 

"extends React.Component" tells React that this is a class-based component. "React.Component" is a class given by React. UserClass inherits some properties from it.  And the React.Component comes from the React package.   
![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/7ac13a57-9462-4cbd-8e9c-6eab494017cc)  

In class based component render() method is used to return the JSX.  
![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/9a046bba-b8de-4990-b0e6-5de708ca8823)  


PROPS IN CLASS-BASED COMPONENTS:  

We set props in class based function using constructor method.  In the constructor method, it is mandatory to send the props in the super method. It is used to make a call to the parent class (Component) to initialize the values in the parent class and to make sure that the initialization logic of the parent class is executed before executing the logic specific to the created component.  
And we access it using "this" keyword.  
![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/42c75a76-962f-49bd-a21a-65292ed09f13)

Sending the props is same for both class components and functional components  
![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/c5244736-24c9-4707-a108-b0a854c87186)


Whenever the class is initialized the constructor is called i.e. When a new instance of the class is created(i.e. when we use the component in another component or in the root of our application, a new instance is created), the constructor is called. Props is extracted and can be used anywhere when super keyword is used.  

When we load/render a functional component, its basically invoking/mounting the function or functional component.  
When we load a class-based component, it means we are creating a new instance of that class.  


STATE INSIDE CLASS-BASED COMPONENTS:  
Previously we didn't have hooks. We used the reserved word state to create state variables. State variables are created inside constructor.  

State is a big object which contains state variables. We declare all the state variables inside this object.  
Also in a state variable of a functional component, eventhough we declare 2 state variables separately, React converts it into one single object and treats it like we write for class-based components. 

![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/4de4f8ed-c10f-451b-8013-f0e2c4566105)  
![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/d8ad0747-0cc2-49be-9a86-646d5ac21c3f)


To update the state variables, we have a function called setState and it can be used to update all the state variables. And each time the state variable changes, the component gets re-rendered and the updated part alone gets changed.  

![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/9c8c49e3-c468-4549-b33c-48e3a95e4c16)  

Example to update multiple state variables:  
![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/47d495a4-6796-4ddc-9e8e-ffab92734401)  


Behind the scenes, let's take the above example. When the button is clicked, setState will be called and React takes the object which was passed from the setState and updates it. It doesn't touch the other objects which was not updated.  Say, there were count, count2, count3 and we passed only count in setState, only count will be updated.  
So here, when the button is clicked the RECONCILIATION is triggered and React finds the diff between the previous and current states and updates it.  


HOW THE COMPONENT IS LOADED/MOUNTED ON THE WEB PAGE:   
Let's take the About.js file for example. AboutUs component is the parent component. When we load this component onto the web page, it goes line by line, sees the UserClass class-based component, and now moves to UserClass and loads it. Now, when a class loads, an instance of the UserClass is created, then its constructor is called(which is the first thing that happens when a class loads), then render is called. 
![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/b432b280-3a25-4582-bb59-0b98dd72f381)  

Let's make the About component as class-based component, so that it'll be class based component (UserClass) in a class based component(AboutUs). We can see that it is printed in the order => Parent constructor, Parent Render, Child constructor, Child Render. This is how the lifecycle of class-based components works.  

![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/3bd8836a-21ec-4f79-936f-0b265ccbdc6c)  

ComponentDidMount():  
React class-based components also have another method called, ComponentDidMount(). Once the class loads, first constructor is called, then render, and once the component is loaded and present in the DOM, componentDidMount is called. 

LIFECYCLE OF CLASS BASED COMPONENTS:  

Now, lets add the component did mount console log to both Parent(AboutUs) and Child(UserClass). Now, it will be printed in the order => Parent constructor, Parent Render, Child constructor, Child Render, Child Component Did Mount, Parent Component Did Mount. As the Parent component is fully rendered only when its child is completely rendered/mounted, only then the ComponentDidMount method of Parent will be called. This is the lifecycle of Parent-child relationship.   

![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/595a7b71-5c78-4770-9143-c6e97394a36d)


Why ComponentDidMount is used?   
It is used to make API calls once the Component is mounted.  
Why we make API calls inside ComponentDidMount?  This is similar to useEffect in Functional Components. We use it so that we quickly render the component and then make the API call and then fill the data inside the component to re-render.  


When we render the same component twice, it means we are creating two different instances of the same class. 



