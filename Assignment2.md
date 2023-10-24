1. What is NPM?  
     NPM helps with managing packages.

2. What is Parcel / Webpack? Why do we need it?  
    Parcel/Webpack is a bundler that helps with making the app perform faster by optimizing, minifying code, etc. And helps with packaging the app so that it can be pushed to production.

3. What is '.parcel-cache'?  
     Parcel uses the .parcel-cache folder to save files in it to reduce build time each time we build a project.

4. What is npx?  
    npx is used in the command to execute node packages. Helps with installing a package globally or locally in our system.  
    Eg: npx parcel index.html executes the parcel package.

5. What is the difference between 'dependencies' and 'devDependencies'?  
      Dependencies are packages that our application needs to function properly.
   Dependencies are used in Production. They are smaller in size compared to devDependencies.  
   devDependencies are used when we develop but are not needed in the production environment. Whenever we install devDependencies we add -D to the command.  

6. What is Tree Shaking?  
     Tree Shaking algorithm is used by Parcel to remove unused code automatically. It is one of the key functionalities of Parcel.

7. What is Hot Module Replacement?  
     Each time we make some changes and save the file the website reloads automatically. This is because the files are updated using Hot Module Replacement Algorithm so that the latest content is displayed on the website.

8. List down any 5 superpowers of Parcel. Describe any 3 of them in your own words.  
       File compression, Differential Bundling, Error Handling, File Watching Algorithm, Consistent Hashing.  
   
     - File compression - Removes all white spaces in code, renames variables to shorter names to reduce the size of the code, etc.
     - Differential Bundling - Provides support for older versions of Browser and in different browsers.
     - Error Handling - Displays syntax errors, dependency issues, and other issues in your code in the console.

9. What is .gitignore? What should we add and not add to it?  
    Files which doesn't need to be pushed to production are put into the git ignore file. Basically, files that can be generated from files that already exist need not be pushed to production.  
   Eg: node modules need not be pushed as it can be generated from package.json and package-lock.json files. 

10. What is the difference between package.json and package-lock.json?  
      package.json file contains the approximate versions of dependencies. Those versions have either a ~ or ^ symbol as a suffix so that they can be automatically updated when upgrades are available.
      package-lock.json file contains the exact versions of all dependencies including transitive dependencies.

11. Why should I not modify package-lock.json?  
     It has the exact locked version of all dependencies. package-lock.json is used to regenerate node modules in production. So modifying it may lead to malfunction of the website in production along with some other vulnerabilities etc.

12. What are node modules? Is it a good idea to push it into git?  
      Node modules contain all the dependencies/packages needed for the application to function properly. Due to this, it is big in size. It is not needed to push node modules to git as we can regenerate it using package-lock.json file.

13. What is the 'dist' folder?  
       Dist folder contains the files that are needed to display the website(html,css,js) in binary code form. Basically our website is displayed from the files of dist folder. It gets created when we execute the parcel package. When we build it for production minification, compression, image optimization etc all are done to reduce the size and make it faster.

14. What is 'browserlists'?  
      Browserlist is the configuration used to mention in what browsers and versions of browsers the website/application gets supported. We mention it in the package.json file.
