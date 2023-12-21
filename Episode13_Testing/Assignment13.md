1. What are the different types of testing?  
   - Unit testing
   - Integration testing
   - End-to-end testing  
  
2. What is enzyme?  
   Enzyme is a testing library which is useful specifically for unit testing React components. Enzyme allows developers to shallow render react components, traverse and manipulate the rendered output and make assertions about the component's behaviour. It provides a range of utility functions that simulate user interactions such as clicking buttons or changing input values and check the resulting changes in the component's state or output.  

3. Enzyme vs React Testing Library
   React Testing Library:
   - Emphasizes user interactions and behaviour
   - Doesn't support shallow rendering. Encourages simulating real application
   - Encourages writing tests that mimic user behaviour
   - Provides simple query methods to interact with rendered components
   - Encourages developers to write tests that ensure application is usable by all users, including those with disabilities.
  
  Enzyme:  
  - Allows shallow rendering. Can be useful for isolating the component being tested.
  - Provides set of utility functions that allows you to traverse and interact with component's internal state and methods
  - Supports full rendering with mounting
  - Returns a wrapper object around the component, providing a set of methods for interacting with the component, querying the DOM and simulating events


4. What is Jest and why do we use it?  
   Jest is a testing library used for testing React applications. It is used because  
   - Zero configuration
   - Includes its own assertion library
   - Provides powerful mocking capabilities, allowing you to mock functions, modules and even entire libraries
   - Watch mode: Automatically reruns tests when files are changed
   - Coverage Reports
   - Comes preconfigured for testing React components. Integrates seamlessly with tools like Enzyme or React Testing Library.  
   
 
   
   
