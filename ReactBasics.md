Why do we two CDN urls to include react libraries in our code?

<script crossorigin src="https://unpkg.com/react@18/umd/react.development.js"></script>
<script crossorigin src="https://unpkg.com/react-dom@18/umd/react-dom.development.js"></script>

First one is the core React library. Second one acts as a bridge for DOM manipulations. 
React works for web browsers (React) and for Mobile devices (React Native). So to support these web operations and to connect to the DOM we have used react dom url in the code as well.

REACT JS IS A LIBRARY.

My First React Code:

Line 16: createElement in React takes 3 arguments: tag we need to create, an object where we can specify the attributes we want to give to the tag, the content we need inside the tag.
Line 17: We need a root element in which the React application will be rendered in our HTML document. We've used ReactDOM object as it is going to be a DOM manipulation. We've mentioned here which html element will 
act as the root.
Line 18: .render function is used to inject the react code into HTML.

![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/957703e6-8d80-4628-bbed-0f366c56efa4)

Line 18: When we do React.createElement what will be stored in heading? Is it just a h1 element?
When we write React.createElement, a React element is created which is a Javascript Object. So, heading is a react element. 
When we assign those tags, attributes and content to the heading element, it is not a HTML tag/element yet. The ".render" function in Line 18 converts the heading to h1 tag as HTML code under the root node. This is what
happens behind the scenes.


How to create the nested element structure using React JS?

Let's say we want the below structure:

![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/e96f848c-06bc-48e3-95f0-79a6c09b0593)

![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/80c023b3-9f8b-4b24-861e-8165884477fb)

As we have 3 attributes for createElement method in react, for the 3rd attribute we give the children which should be under that particular tag. So here we need another div tag with the id: child. So we give that. Again under that we need a h1 tag, which goes in the 3rd attribute of the child div element and so on.

![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/a9d2adc0-f543-430a-8623-4e1367f4d637)
