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

React Testing Library uses Jest behind the scenes. We are using Jest along with Babel, so we need to install some additional dependencies.  

We know that Parcel uses Babel behind the scenes and has its own configuration for Babel. But since we're using it with Jest we've given our own configuration for Babel. Now Parcel gets confused as to which configuration should be used, as our configuration will be overriding. So, to avoid this we need to change Parcel's behavior to use Babel with Jest. So we configure Parcel to disable default Babel transpilation.  

#Setting up testing in our app
- Install React Testing Library
- Install Jest
- Install Babel dependencies
- Configure Babel. We used configuration lines from here (https://jestjs.io/docs/getting-started) for this step.  
- Configure Parcel Config file to disable default Babel transpilation. We used the configuration from here (https://parceljs.org/languages/javascript/#usage-with-other-tools) for this step.
- Jest Configuration (npx jest --init)
- Install JSDom
- Install @babel/preset-react (When we try to any JSX in JSDom, there is no support for it. This package is needed for that)
- Include @babel/preset-react in babel config (Preset? -> Babel preset helps testing library to convert JSX to HTML, so that it can read properly)
- Install @testing-library/jest-dom (to use toBeInTheDocument() kind of assertions)


  When we try to console log the queried elements, it returns a JSX Element which is nothing but an Object/React Element/Virtual DOM. 

![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/ce91396c-de34-45f7-a891-064b9ae42bbc)  


As we keep writing test cases, it keeps getting big. So, we can group some test cases into one using describe().  
it() can be used instead of test() as well for test cases.  

