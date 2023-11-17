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


When we render the same component twice, it means we are creating two different instances of the same class. Let's say we display UserClass twice and let's see how the lifecycle goes.  

When the component is mounted it is mounted in 2 phases, render phase and commit phase.  

Render phase: Constructor is called -> Render is called
Commit phase: Updates the ACTUAL DOM -> Component Did Mount is called

Since, Component Did Mount is called after DOM updation, Component Did Mount is the best place to make an API call.  

Now, let's go back to displaying the same class component twice inside a Parent class component.  

Consider only the Mounting box in the diagram, '
When we render two children, React optimizes this process and batches together the Render phase for both the children, and then executes the Render phase for both the children together.
![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/b71f6ff7-eb24-449f-b061-f05b6a0319a7)

That's why we see, the constructor and render of both children being called first, then the componentDidMount was called for both the children as part of combining the Render phase. This is because once the commit phase starts, DOM Manipulation has to be done which is a very very expensive operation. Render phase completes quickly where it updates the Virtual DOM, finds the Diff between old and new Virtual DOMS, triggers the Reconcilication process, but the Commit phase takes time and that's why it combines the commit phase of all the children.  

![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/c3920eeb-6e66-4c53-83c3-cf8e866553cb)



Below is an example for how LIFECYCLE WORKS where I introduced ANOTHER CHILD INSIDE A CHILD (UserClass.js), which is SuperChild.  

![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/924e682c-da27-46a0-bef2-8b45013965b4)  

So, we can see the render phase is batched for all the children i.e. even for children of children. That is why we see, Parent Render phase -> First child render phase -> (First Child's) Super child render phase -> Second child render phase -> (Second child's) Super child render phase -> (First Child's) Super Child Component Did Mount phase -> First Child Component Did Mount -> (Second Child's) Super Child Component Did Mount phase -> Second Child Component Did Mount -> Parent Component Did Mount  
PS: Ignore useEffect printed at the end.  

![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/72533b85-acfa-4fe8-92bf-0073d58118c6)  


How do we make API call in ComponentDidMount()?  

We make the componentDidMount method as an async function and use the fetch api given by browser, mostly like we do in functional component. For setting the response and displaying we use the local state variables like the below.  

![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/b1b8a062-c4b7-4bde-a9a6-2155e1bd5e74)  

![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/88bd7847-88b7-4817-b9b2-407e16c6051c)  

Let's see behind the scenes now...  
Let's take the lifecycle flow,   
------ MOUNTING --------  
Constructor (Dummy data is set in the state variable)  
Render (Virtual DOM is updated with Dummy data)  
DOM Update (Actual DOM gets updated with dummy data - which we see for few ms)  
ComponentDidMount is called  
    API call  
    this.setState (State variable is updated)  
  

-------- UPDATING ----------  
RENDER (API data is updated in virtual DOM)  
DOM update (Actual DOM gets updated with API Data)  
ComponentDidUpdate is called (called after the update cycle)  

![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/fca104ac-2cda-421a-9a75-c0574654b408)  


Now, let's see the unmounting phase.  
What is unmounting?  
When the component will disappear from the UI. Then willUnmount will be called. Here, in the below image for unmount to be called we clicked on ContactUs button, so that this component will unmount.  

![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/5c87b409-78ca-4117-a2a9-145205498ab4)



DO NOT COMPARE REACT LIFECYCLE METHODS TO FUNCTION METHODS.  
ComponentDidMount is not equivalent to useEffect. useEffect does not use ComponentDidMount behind the scenes.  
After the initial render componentDidMount is called. Then for every subsequent render, componentDidUpdate is called, it is not mounted it is updated. So componentDidMount, componentDidUpdate, componentWillUnmount are all different and called at different times.  


componentDidUpdate() lifecycle method is called after every render.  

this is shared by all the lifecycle methods.  

Why do we need or when will be componentWillUnmount() method be used?  
For this let's include a setInterval() in componentDidMount() method with an interval of 1s. Now, when we go to the About page, we can see the setInterval console log in the terminal. When we move to the Contact Us page, component unmount got printed but still we can see the setInterval console log printing and running, so this indicates that the component just got replaced when we moved to Contact page, but was not unmounted properly and this will cause performance issues.  

![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/779aefff-aaf1-424d-9f05-b20e1fde83f0)  


One more thing to note here: When we move to Contact page, then come back to About page, we see the interval getting increased at 2s at a time, this is because the interval that was set is not unmounted yet and as we come back to the same page again, another interval with 1s starts again. This increases as we keep moving to another page and coming back to About page.  

In the below image, we can see that even after the unmounted message, interval keeps running.  
![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/7d13433a-5280-4abb-9d7e-efdb64e5e3a4)  


So, to avoid this kind of issues we need to unmount the component always. So, for setInterval in componentDidMount we do clearInterval in componentWillUnmount.  

![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/11c47380-dc3b-4865-b42d-82fa74f9fb66)  

![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/7e27038f-c2cf-43f2-b666-0b50c4e6c4f3)  



Now, if we include the same setInterval in useEffect how do we unmount it?  
It behaves the same like setInterval i.e. setInterval keeps running even when we move to a different page.  
For unmounting in functional components, we can return a function from useEffect(), and that will be called when we need to unmount the component i.e. return will be called when we leave the page or when the component gets replaced.  

![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/aad7ab2d-cccf-4ac3-952a-acdad400c9f0)  
  
Here, we can see useEffect return printed once we moved to Home page.  
![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/c3ce5cd6-0253-4ae4-a0b3-63f6d92097c4)  

![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/fd079569-067a-4395-8460-d612904cde5e)  


With the setInterval example,  
![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/f10c3fe1-2f6a-4b45-a0e1-599a3bf2f998)

![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/faacf565-887e-43e9-b5fc-8e1f9b490177)

![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/1670dbe1-a6b6-42be-bb16-0bc155a1a8f9)



