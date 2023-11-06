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
