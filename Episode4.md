Before starting to build an APP - FOOD ORDERING APP
1. Planning
     You should know exactly what you're going to build. - Food ordering app    
     A UI Mock. Once we have a visual picture of what we're going to do, it'll be very easy to code. - UI mock/ Wireframe/ hand-drawn design etc  
     Low-level planning. What components can my app have? - Header, Body, Footer
         In header - Logo Component, Nav items
         In Body - Search Component, Restaurant Container - Restaurant Cards
         In Footer - Copyright, Links, Address, Contact

   ![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/17414fc4-c505-45a5-a18a-49d32df3563a)
  
  
PROPERTIES:  
If we want to pass dynamic values to Components, we can do it through PROPS. Props are nothing but arguments. i.e. Components are functions in JS and Props are arguments to functions/Components.  
React  wraps the Props into an Object and passes to the component as Arguments.

Here, we have passed resName and cuisine as arguments to the RestaurantCard component as props. Since, functions and arguments are part of JS, we've accessed the JS code using the curly braces. Also since the properties are wrapped as an object, we've accessed it using the dot notation.

![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/c81e45f0-0158-426a-863d-cff6182413d6)

We can also destructure the arguments as well, as shown in the below images, this is called DESTRUCTURING ON THE FLY.  
![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/07c14054-a806-4e94-9a75-58eb78053f74)

OR like below  
![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/719743ad-f51e-4b78-8ddf-bdb663698bf6)


CONFIG DRIVEN UI:  
Controlling how our UI looks based on DATA/Config. Where does the config come from? BACKEND  
  
  
If we have too much data, i.e. say for a restaurant we will have a lot of data like price, location, rating, cuisine, travel time, etc.  
So, can we include each property one by one in the component? No, we create a JS object, assign all the properties to it, and use it with the dot notation.
Eg:  Here we have list of restaurants with each restaurant having its own rating, price for two, distance and so on.

![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/55a64af8-7c95-4758-826c-e679af5e7cab)



We use map to iterate over each restaurant object from the restaurant list. Whenever we use map, make sure to add the key property with a unique value assigned for each item in the array list. WHY?  

Because, say there are already 15 restaurant cards, and now a new restaurant comes to be displayed before the first one, now the DOM doesn't know which card is the new one and re-renders all the cards again. When we give an ID, it knows which ID is the new one this time and renders that particular card alone. This helps hugely with OPTIMIZATION. So, whenever we write a loop-like thing/map to render the elements it's important to add the key property and it should be UNIQUE. Not using Unique key, takes a PERFORMANCE HIT in the website.

But here, we cannot use INDEX as keys as it's not recommended. But it is better than not using a key when we don't have a unique ID.

not using keys (not acceptable) <<<< index as key <<<<<<<<<<< Unique ID as a key (best practice)
