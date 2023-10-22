*IGNITING OUR APP*

React alone doesn't make an app faster. React along with many other libraries help making the app faster.

NPM DOES NOT HAVE A FULL FORM. It manages packages but doesn't stand for Node package Manager.

"package.json" file is the configuration for npm. After we provide all the configurations for our npm, this file gets generated.

Most important package:
Bundler - Helps to Minify/cache/compress/clean the code before it is sent to production. (Webpack, Vite, Parcel). Packages the app so that it can be shipped to production.

We can install 2 types of dependencies. Dev dependencies and normal dependencies. 
Dev dependencies - Used when we develop. Eg: npm install -D parcel.
Normal dependencies - Used in production

* ^ and ~ symbol in package.json:*

^ symbol means it'll automatically upgrade to the latest minor version if any without us incrementing it. Say we installed 2.8.3 today and 2.8.4 gets released tomorrow, ^ symbol upgrades to 2.8.4. But if there is a major upgrade ^ symbol won't do the upgrade.

~ symbol automatically upgrades to the lastest major version.

![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/708e7ba4-7228-4d06-8d63-26f087984c0a)

After installing parcel, we can see a new file "package-lock.json". It tracks the exact version of all the packages/dependencies. Even though we have the version mentioned in package.json, even when the version gets increased version in package.json shows the same one we manually installed but package-lock.json has the exact version of the package.

We would also have a folder called "node modules" in our vscode after installing parcel. This contains the code for parcel. It is like a place where the code for all our packages exist. 

Now you get a question I installed only parcel why did get some other packages as well?
Parcel has its own dependencies, and those dependencies will have some other dependencies and so on. That is why and this is called "Transitive dependency".

Node modules is a collection of Dependencies.


Our project's dependencies are present in package.json, likewise, each dependency will have a package.json for its own dependencies. Rg: If we look into parcel under node modules, it has a package.json file for its own dependencies. So, in that aspect, we have multiple package.json. 


![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/b0851be6-a83e-4af6-9d88-39c29920457d)


We don't need to push node-modules to git. If we have package.json and package-lock.json, we can regenerate the node-modules again. It's because we have all the dependency information in these 2 json files and it is enough for it to regenerate it. 

Command to regenerate node-modules in our local: npm install


npm - command to install a package
npx - command to execute a package


npx parcel index.html [source file of project]
creates a development build, server and hosts it in a port and provides the url.


We can inject react and react-dom into the project using npm as well. Including cdn urls is not a good practice.
Fetching cdn url is a costly operation(as it tries to hit the unpkg url). If version changes we need to keep changing the url as well. We can have react as a dependency in node modules as well and use it.


What all things Parcel does?
Creates a Dev Build
Creates a Local Server
HMR - Hot Module Replacement [Each time we save the file, the browser reloads automatically to update the content. This is because of HMR].
File Watching Algorithm [HMR is done through this algorithm written in C++].
Parcel helps with Caching which helps with faster builds each time we save the file.
Image Optimization [Costliest operation]
Minification
Bundling
File Compression [Remove all white spaces]
Consistent Hashing - Renames files each time we update the content so that browser can fetch lastest content except files which require a stable name
Code splitting
Differential Bundling - support older browsers / support to open the app in different browsers
Diagnostics of app
Error handling
Provides HTTPs support as well when needed
Tree Shaking - remove unused code
Creates different Dev and Prod builds [When we give "npx parcel build index.html" command a prod build is created and put in the "dist" folder. And gives just 3 files with html,css and js files. Does minification, compression, tree shaking, optimization etc and everything. The same happens when created dev build as well execpt all other minification, compression etc wont be to that level of production build.]



To make our app compatible with old browsers: 
We use browserslist package[https://browserslist.dev/?q=bGFzdCAyIHZlcnNpb25z], to mention in which all browsers we support 100%. Check the mentioned website to know what we should write for browserslist package.
