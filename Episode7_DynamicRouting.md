useEFfect() DIVING DEEP:  
  
Every time the component renders, useEffect will be called(default behaviour). Dependency array changes the behaviour of useEffect.  
Dependency array is not a mandatory param.  
  
no dependency array => useEffect is called on every component render/ re-render  
if dependency array is empty [] => useEffect will be called on initial render (just once)   
if dependency array is given a value => useEffect will be called everytime when the value is updated  


useState():  

Never create state variables outside your component.  
Used to create Local state variables inside functional components.  
Always call it on the top of the component(in code).  
Never create useState variable inside if else/for loops/functions/condition. Can creact inconsistencies.  


Routing:

Whenever we develop routes, we've develop a routing configuration.  
Configuration - information that will define what will happen in a specific route/ that will tell the browser router what will happen in a specific path.  
createBrowserRouter takes list as an argument. Here we mention the list of paths. 
Path is an object
Once we define the paths, we need to render it to the screen. This will be done by ReactProvider which is a component, that will provide the routing configuration.  
There are many routers but createBrowserRouter is the recommended one for React Projects.  
ReactRouterDom gives us access to a Hook useRouterError. This hook gives us more information about the error. [check Error.js file]  


Children Routes:  

When we move to About page/contact page, we are losing the header. But we want other pages also to be displayed with the Header and Footer.  
For this we create Chidren Routes. The Outlet component from ReactRouterDom helps us with this. With the child element we create, it helps to replace the Outlet component with the respective component.  
  
  
Don't use Anchor tag in React when we want to route to a different page. This will reload the whole page while taking us to the new page.  
We can move to a new page without refreshing the whole page which helps to increase performance.  
Super power given by ReactRouterDom is the Link component. This will just refresh the components. There is a difference between reloading the whole page and refreshing the components alone. If we see in the elements section under inspect, we can see that when we click on the Contact Us/About button, the Header remains intact and only the div below it changes.  
  
Link is given by React Router Dom. It is a wrapper around anchor tag. Link Component uses Anchor tag behind the scenes. And React Router Dom keeps track of the element as a Link. The browser doesn't understand Link, it understands Anchor tag and that's why we see Anchor tag in Elements tab where Link is used.  
  

And this is why React Applications are called Single Page Applications. It's just exchange of components.  


TYPES OF ROUTING:  
We can have 2 types of Routing in React Web apps:  Server Side Routing, Client Side Routing.  
Server Side Routing: When we've used the Anchor tag and clicked on About us, It makes an API call to the about us.html page, fetches it, reloads the whole page, and displays it.  Here, aboutUs.html is coming from the server.  
Client Side Routing: We are not making any API calls when we are moving to a new page. Because all the components are already loaded in our app when we loaded the app for the first time.  


Dynamic Routing:

url: restaurants/:resId - :resId in url denotes the dynamic value.  


When using a map, always use a Key.  

useParam Hook given by React Router Dom helps to fetch the dynamic param of the url. [check :resId in RestaurantMenu.js]  
