Why do we two CDN urls to include react libraries in our code?

<script crossorigin src="https://unpkg.com/react@18/umd/react.development.js"></script>
<script crossorigin src="https://unpkg.com/react-dom@18/umd/react-dom.development.js"></script>

First one is the core React library. Second one acts as a bridge for DOM manipulations. 
React works for web browsers (React) and for Mobile devices (React Native). So to support these web operations and to connect to the DOM we have used react dom url in the code as well.


My First React Code:

Line 16: createElement in React takes 3 arguments: tag we need to create, an object where we can specify the attributes we want to give to the tag, the content we need inside the tag.
Line 17: We need a root element in which the React application will be rendered in our HTML document. We've used ReactDOM object as it is going to be a DOM manipulation. We've mentioned here which html element will 
act as the root.
Line 18: .render function is used to inject the react code into HTML.

![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/957703e6-8d80-4628-bbed-0f366c56efa4)
