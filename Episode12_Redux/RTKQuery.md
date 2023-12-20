RTK Query  
Fetch API:  
createAPI function is used to configure an API in RTK query.  
In the createAPI function,   
- we have a reducer to map it in the redux store.
- we have a baseQuery, in which we configure the base settings of the API. In the given image we've set the base URL using the fetchBaseQuery function.
- we have endpoints, in which we specify and define endpoints for the API. To define an API, we use a function which takes the "builder" object as an argument. And in the function, we provide the endpoint name and its definition as an object. For definition, we the query function provided by the builder object. And query function takes object as arguments. This object takes a function, which we've defined as the Pokemon name.
- Note that, we've appended the URL with "/pokemon/{name}" in the endpoint definition.  
- Also, createAPI automatically provides us with a Hook for us to use the Endpoint. So here it will be "useGetPokemonByNameQuery" which is tailored to fetch data using the getPokemonByName endpoint.
- Note: We need additional middleware functionality along with default middleware of Redux ToolKit as it doesn't have functionalities to handle API requests/caching/other features provided by Redux ToolKit query. So we concat Pokemon middleware to the default middleware for handling API realted functionality. Refer below image for code.
- ![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/ab467883-12ee-4c7b-b5c1-1efcb4cbdb9f)
- Default middleware includes functionality like thunk middleware for handling asynchronous actions.


- ![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/90991c03-fe82-41ad-be24-dc5173f66490)

Below is the image of how we used the API data to display in Contact Us page
![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/209672af-a365-4000-b6d1-011f3bb41693)



"Thunk" in Redux Toolkit Query:  
