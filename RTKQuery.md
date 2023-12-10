RTK Query  
Fetch API:  
createAPI function is used to configure an API in RTK query.  
In the createAPI function,   
- we have a reducer to map it in the redux store.
- we have a baseQuery, in which we configure the base settings of the API. In the given image we've set the base URL using the fetchBaseQuery function.
- we have endpoints, in which we specify and define endpoints for the API. To define an API, we use a function which takes the "builder" object as an argument. And in the function, we provide the endpoint name and its definition as an object. For definition, we the query function provided by the builder object. And query function takes object as arguments. This object takes a function, which we've defined as the Pokemon name.
- Note that, we've appended the URL with "/pokemon/{name}" in the endpoint definition.  
- Also, createAPI automatically provides us with a Hook for us to use the Endpoint. So here it will be "useGetPokemonByNameQuery" which is tailored to fetch data using the getPokemonByName endpoint.

- ![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/90991c03-fe82-41ad-be24-dc5173f66490)

