Higher Order Components:  
A function that takes a component and returns a component.  Takes the component, enhances/modifies the component(adds some features), and returns it back.  
Higher Order Components are Pure Functions. They don't change the existing behaviour of the input Components but they will just enhance the input Components.  

<br>

Let's take the Promoted Restaurant cards in Swiggy. So, it looks like other cards but has a Promoted label on it. So, we are going to enhance the Restaurant cards using Higher Order Components.  
Here, we have taken the RestaurantCard component and included the Promoted label to the restaurants with rating > 4.6. So, we've passed RestaurantCard as input. Since a higher order component returns a component, and a component is nothing but a function, withPromotedLabel component returns a function(a component). And inside that, we've included the Promoted label on the RestaurantCard. Since, the component inside the higher order component needs its props to get displayed we've received it in the return function and used a spread operator in the RestaurantCard component to pass all the props as individual props to the RestaurantCard component. If we don't use the spread operator all the props will be passed as a single prop to the component.  

![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/f27b6313-10f6-47ac-ac56-b70b28733121)


The RestaurantCard displayed in withPromotedLabel also needs props to get displayed, so we've passed props to RestaurantCardPromoted as well. Refer the below image.

![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/b765e9ff-2225-48a6-ab4b-4460d251a24d)

This is how we use the higher order component in the imported file.  
![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/28104209-3a6f-4dff-8acd-8fb1acf6d308)

