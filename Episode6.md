Monolith and MicroService Architecture:

Microservices:  
Different services for different Jobs. This is known as Separation of Concerns. Single Responsibility principle. With this, we can have our UI written in React, BE in Java, DB in Python, SMS service in GoLang. We can write our microservice written in any architecture/language.  All services run on their own specific ports. All these ports can be mapped to domain name, say /api for BE, /sms for SMS, / for UI. If UI wants to contact BE, it can call '/api' or different port.  


We have 2 ways to fetch data from API on the fly:  
1. Page loads ----> API call(wait for data from API) ----> Render UI
   Let's say if API call takes, we wait for it before rendering. 

2. Page loads ----> Render UI ----> API Call ----> Re-render app with new data from API

In React, we always use 2nd method. Because in the 1st method, user sees nothing as soon as they land the page, and it doesn't give a good User Experience. 
In the 2nd method, we first display the skeleton/ whatever data we have, and then as soon as we receive the data from API, we re-render the page which gives better User Experience. Here, re-rendering doesn't cause an issue as React is more efficient with its rendering cycles. 


UseEFfect() hook:  
useEffect() takes two arguments. 1 - callback function, 2 - dependency array. 
The callback function will be called, AFTER the COMPONENT loads/renders/as soon as the render cycle is finished. 

So, for the 2nd approach of fetching data from API, useEffect will be helpful. 

Shimmer UI:  
A shimmer UI resembles the page's actual UI so users will understand how quickly the web or mobile app will load even before the content has shown up.  
We load a fake page until we get a response from API


Why do we need state variables? Why not use the normal JS variables?
   when we use JS variables, let's say we need the Login button to be changed to Logout button as soon as it's clicked, so in the onclick method we set the variable to "Logout". When we click on it, we can see that it is getting logged as "Logged out" as printed in the method but the button text in UI hasn't changed. Because the UI was not re-rendered or refreshed to update the new components/changes.  
   So the page has to be re-rendered when there is a change in the components and the JS variables are not capable of this. In state variables, we have two params where one is the variable and one is a function which we can use to update the value of the state variable. This is possible because, each time the value of the variable is set, it triggers re-rendering. The setValue method acts as a trigger to re-render the whole component again.  
   Re-render the component is nothing but, the state variable calls the component once again with the updated values. But when we check the elements tab, we can see only the logout element changes, because React calculates the minimum difference between the old and new state of the virtual DOM.


If the State variable is a constant how can we update it?
   When we update the state variable through the setValue method, another instance of the variable is created with the updated value. 

   
