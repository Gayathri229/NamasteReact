1. How do we configure tailwind?  
   - Install tailwind using the commands given in tailwind website  
   - Create a file for postcssrc and paste the configuration given in the website  
   - Give the paths to the template files(html,css,js) in tailwind config file  
   - Add the tailwind directives given in the website in index.css file
     
  <br/>
  
2. In tailwind.config.js, what does all the keys mean (content, theme, extend, plugins)?  
   - content => This key is used to mention the path for template files so that tailwind CSS can scan those files for classes.  
   - theme => This key is used to default styles and configurations for your project. It includes various sub-keys like colors, font, spacing, breakpoints, etc that we can customize.  
   - extend => This key is used to override styles in the default theme. It's used to add custom colors, fonts, spacing, and other styles that are not included in the default Tailwind CSS setup.  
   - plugins => This key allows you to use and configure external Tailwind CSS plugins. Plugins are additional modules that add functionality and styles to Tailwind. Eg: we can use plugin that provides additional                    utility classes.  

  <br/>

3. Why do we have .postcssrc file?  
   .postcssrc file is used to tell the bundler that tailwind css is used in this project/app. Bundler(Parcel) uses postcssrc file to read & understand tailwind CSS.  
   Tailwind CSS relies on Post CSS for processing and transforming its utility classes in actual CSS (for my understanding).  
