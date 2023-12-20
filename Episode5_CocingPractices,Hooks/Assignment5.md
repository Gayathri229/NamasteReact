1. What is the difference between Named export, Default export, and '* as' import?  
   - Named Export - Used when you have to export multiple values from a file.  
   - Default Export - Used to export one value as a default one from a file.  
   - '* as' Import - Used to import all the named exports from a file using a common name.  

2. What is the importance of config.js file?  
   It is not a good practice to have hardcoded values along with other code, so we put them in a separate config/constants file to make it easier to access them.  

3. What are React Hooks?  
   Hooks are a set of utility functions that help us to keep the UI layer in sync with the data layer. It helps to update the UI when there are changes in data layer when user interacts with the page and displays the latest/updated UI. They form a Virtual DOM. Updates DOM efficiently using the Diff algorithm. Helps with re-rendering components in UI when there is a change in data. 2 important hooks are: useState() and useEffect().  

4. Why do we need a useState() hook?  
   It is used to create State variables. useState() hook helps to maintain the State of the Components i.e data which changes when a user interacts with the page. Its scope is limited to the component in which it was created. It returns a list with 2 variables, first one takes the default value, second one is a function that is used to pass the updated value for state change.  
Eg: const [listOfRestaurants, setListOfRestaurants] = useState([]);  
Here, we've set an empty list as its default value.  
setListOfRestaurants({
resName: efewfewf,
rating: efwfwef,
...
});  
Here, we have set the updated state to a list of restaurants.  
