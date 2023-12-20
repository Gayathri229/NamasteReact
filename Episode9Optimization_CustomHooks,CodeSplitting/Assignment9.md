1. When and why do we need lazy()?  
   We use the lazy() function given by React for dynamic imports when we do code splitting/chunking of code. The part of the code used in lazy(), loads on-demand and helps to optimize the app by making it light-weight and better performance.  

2. What is suspense?  
   Suspense is a component given by React with which we can wrap the component that was dynamically imported so that we can handle the fallback state caused when the file doesn't load in the browser as quickly as expected.  

3. Why we got this error: A component suspended while responding to synchronous input. This will cause the UI to be replaced with a long indicator. To fix, updates that suspend should be wrapped with startTransition? How does suspense fix this error?  
   This error was caused because the dynamic import file took longer time than expected to load in the browser. We handled this by wrapping the dynamic import components in the Suspense component with the fallback code which will act as a placeholder for this state.

4. Advantages and disadvantages of using code splitting pattern?  
   Advantages:  
   - Faster initial page load
   - Lazy loading
   - Better User experience
   - Improved performance

   Disadvantages:
   - Complexity - code splitting introduces complexity to build process.
   - Dependency on network conditions - May introduce a delay in loading of features/components if network conditions are poor.
   - Potential for overhead - overhead of loading additional code chunks may be noticeable on very fast networks.
  
5. When and why do we need suspense?  
   Suspense is needed when we plan to optimize our code by chunking/code splitting/on-demand loading. It helps to act as a placeholder when the dynamically imported files take more time to load on the browser when accessed. We can mention the code to be displayed in the fallback attribute of the Suspense component.  
   
