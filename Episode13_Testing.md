Writing even a single line of code can mess up the entire application or introduce bugs somewhere else.  

Types of testing DEV can do:  
- Unit Testing - Testing React Components in Isolation. Eg: Is the Header component rendered?
- Integration Testing - Testing the Integration of the components. Eg: Perform Search, here many components work together
- End to End Testing [E2E] - Testing flows from when the user enters the app to leaving the app. Simulating the user throughout the application. Tools required: Cypress, Puppeteer, Selenium.

As a DEV we're concerned about the first 2 types of testing.  

We use React Testing Library(most standard library) to write test cases in our React app. There are other testing libraries like Vue Testing library, Angular Testing Library etc and all are built upon the DOM Testing Library.  
React Testing Library is like a Wrapper around DOM Testing Library and adds features to test the React components.  
If we've created our App using "create react-app" command then the testing library comes along with it. Since we've built it from scratch, we've to install it now.  

</br>

React Testing Library uses Jest behind the scenes.

  
