Single Responsibility Principle:  
Any single identity i.e. function/class/any single identity should have only a single responsibility.  

Modularity:  
Maintaining modularity(splitting code into different small modules) helps to make the code more reusable, maintainable, and testable.  

Custom Hooks:  
Hooks: Special JS utility functions given by React.  
Custom Hooks always start with the keyword "use".  
We extract some responsibility from a component into a Hook so that both the component and Hook become more modular.  
Let's take the RestaurantMenu component for example. It has code for both fetching and displaying data, whereas a component should only be worried about displaying data. So, we move the fetching responsibility into a custom Hook.  

When writing a custom Hook, always think like what it takes as input and what it gives as output. So, here it takes restaurantID as input and returns the Restaurant Menu
