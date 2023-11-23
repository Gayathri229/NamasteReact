Different CSS usages:

Normal CSS
Sass & Scss - Doesn't work well with large apps
Styled components
Material UI - React component library which gives Pre-built, Pre-styled components
Bootstrap
Chakra UI
ANT design
Tailwind CSS
<br/>
<br/>

Tailwind CSS:  
- Works with all frameworks like React, Angular, any other UI frameworks.  
- Go to tailwind CSS website -> Go to framework guides -> Choose the bundler -> Follow the steps.  
- npm install -D tailwindcss postcss - command to install tailwind css. Here Post CSS is nothing but a tool for transforming CSS with Javascript. Tailwind CSS uses Post CSS behind the scenes.  
- npx tailwindcss init => creates tailwind css configuration file.  
- Configure postcssrc file -> here we telling postcssrc that we are using tailwind. Parcel needs to use postcssrc to read & understand tailwind  
- content: ["./src/**/*.{html,js,ts,jsx,tsx}"], => with this configuration we are telling tailwind can be used in these type of files. Here it is html, js, ts, jsx, tsx files under the src folder.  
- Below is the code to import tailwind css in our project which we include in our index.css:  
@tailwind base;
@tailwind components;
@tailwind utilities;


