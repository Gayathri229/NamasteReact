Best practices for coding/maintaining clean code:
  - Separate files for separate components.  
  - All the main code should be under the "src" folder.
  - https://legacy.reactjs.org/docs/faq-structure.html  
  - For a file with a component, try to match the file name exactly as the component name. File name: Header.js, Component name: Header.
  - Using .js or .jsx extension when naming files doesn't matter.
  - 

If we move the component to a separate file, we should export the component from the new file and import it to the file where it is used.  

Here, I've exported Header from Header.js, 

![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/eed50713-de91-439e-a7d3-03f103cd10d0)

And imported it into App.js file. While importing the file, we can or cannot use the ".js" extension, it works the same for both. React identifies the file as JS file with or without extension.  
![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/9e327476-0026-4487-bb9c-7004f451a596)
  
  
HARDCODED CODE'S PLACE:    
You never keep hardcoded data in components file. It's kept in Config/Constants/utils file


EXPORT AND IMPORT:  
We have two types of export and import. Default and named import/export. A file can have only ONE DEFAULT export. 

Eg: Named export  
![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/d35705d3-85bd-4595-a2fe-84b4163ba374)

Eg: Named import. We have to use curly braces to import named exports.  
![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/ff816b75-cc42-43ab-a745-601f6cf2319b)


Eg: Default export  
![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/50cdbbab-f90c-46a6-b028-0a57679bd3e6)

Eg: Default import  
![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/0308e30c-7de7-49e5-bd77-c4f962ea4a53)

