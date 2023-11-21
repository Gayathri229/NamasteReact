Single Responsibility Principle:  
Any single identity i.e. function/class/any single identity should have only a single responsibility.  

Modularity:  
Maintaining modularity(splitting code into different small modules) helps to make the code more reusable, maintainable, and testable.  

Custom Hooks:  
Hooks: Special JS utility functions given by React.  
Custom Hooks always start with the keyword "use".  
We extract some responsibility from a component into a Hook so that both the component and Hook become more modular.  
Let's take the RestaurantMenu component for example. It has code for both fetching and displaying data, whereas a component should only be worried about displaying data. So, we move the fetching responsibility into a custom Hook.  

When writing a custom Hook, always think like what it takes as input and what it gives as output. So, here it takes restaurantID as input and returns the Restaurant Menu.

  
Chunking/Code Splitting/Dynamic Bundling:  

Our bundler i.e. Parcel(used for the Swiggy app)  bundles all the JS code into one and makes it into a single JS file behind the scenes. As the code grows, the size of JS file increases, which is not good for the app as it becomes slower with increasing size. So, we make smaller bundles of these files.  

Logical splitting of bundles:  
A bundle should have enough code for a major feature. Eg: Makemytrip - a bundle for Flights feature, a bundle for Homestays, one for Hotels etc.  

How do we do this?  
We do not import those components directly into that file instead we import it using the lazy() function given by React. It takes a callback function, where we will use the import function to import those components. So, NOW that part of the code won't load as soon as we go to our app page, it only gets loaded when we go to that particular page where that code is used.  

Now, let's take an example of grocery inside our app like Swiggy Instamart.  
Let's say we have a major feature for Grocery inside our app, we have 10 components inside this Grocery component.  
![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/5170a41b-bad4-4f03-9156-5f6fbd4a4a39)  

Now, in the page where we need to use this we do not import it like a normal import, instead we use the lazy() function given by React and dynamically import it. lazy() is a named export. And the import we use here is not the same as normal import, it is a function and will take the path of the component to be dynamically imported. This is known as LAZY LOADING/ON-DEMAND LOADING/DYNAMIC IMPORT.  
What happens behind the scenes is that, as soon as we land on our app, this particular Grocery file won't be loaded. Only when we click on the Grocery button we can see in the network call that a file named Grocery gets loaded.  

![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/5e4bbd3a-996a-4b8a-8234-2f3fc12325d7)  

Another thing is that, when we are in home page, we just have one file as shown below.  
![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/5c8bad93-1dc9-4eb4-b0cc-c90d8e0dad18)  

Now when we try moving to the Grocery page, we will get an error like the below image. This is because the Grocery code took more time to come to the browser i.e. React tried to load the Grocery component, but the code was not there, so React suspended the rendering. This state in the middle, caused it to throw the below error.  

![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/8e5c2863-73c3-4ac9-93d8-24f336746d0b)  

Now, for this issue we use a component called Suspense from React library. And we wrap our component in this Suspense component. This acts as a fallback or placeholder for what should be rendered when the expected code is not available.  

![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/ae7be3ba-3cce-42b4-8beb-07c5ea6436b6)

Here, when clicked on Grocery, we can see the Loading screen when the code is not available.  
![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/00b243bc-8819-49f2-836b-c09b8d9f3837)

And here, we can see the code being rendered. And in the network tab, we can see a separate file being loaded for Grocery apart from index.js.  
![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/f602d24f-ae62-42b4-acaf-aebf0b4504ef)




