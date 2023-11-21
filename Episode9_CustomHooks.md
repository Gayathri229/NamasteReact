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
