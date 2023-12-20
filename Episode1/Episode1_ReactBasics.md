![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/c14f9296-41f6-45aa-ae01-cdefbf9d1beb)Why do we two CDN urls to include react libraries in our code?

<script crossorigin src="https://unpkg.com/react@18/umd/react.development.js"></script>
<script crossorigin src="https://unpkg.com/react-dom@18/umd/react-dom.development.js"></script>

First one is the core React library. Second one acts as a bridge for DOM manipulations. 
React works for web browsers (React) and for Mobile devices (React Native). So to support these web operations and to connect to the DOM we have used react dom url in the code as well.

REACT JS IS A LIBRARY, NOT A FRAMEWORK.

My First React Code:

Line 16: createElement in React takes 3 arguments: tag we need to create, an object where we can specify the attributes we want to give to the tag, the content we need inside the tag.
Line 17: We need a root element in which the React application will be rendered in our HTML document. We've used ReactDOM object as it is going to be a DOM manipulation. We've mentioned here which html element will 
act as the root.
Line 18: .render function is used to inject the react code into HTML.

![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/957703e6-8d80-4628-bbed-0f366c56efa4)

Line 18: When we do React.createElement what will be stored in heading? Is it just a h1 element?
When we write React.createElement, a React element is created which is a Javascript Object. So, heading is a react element. 
When we assign those tags, attributes and content to the heading element, it is not a HTML tag/element yet. The ".render" function in Line 18 converts the heading to h1 tag as HTML code under the root node. This is what happens behind the scenes.


How to create the nested element structure using React JS?

Let's say we want the below structure:

![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/e96f848c-06bc-48e3-95f0-79a6c09b0593)

![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/80c023b3-9f8b-4b24-861e-8165884477fb)

As we have 3 attributes for createElement method in react, for the 3rd attribute we give the children which should be under that particular tag. So here we need another div tag with the id: child. So we give that. Again under that we need a h1 tag, which goes in the 3rd attribute of the child div element and so on.

We can see the HTML structure we wanted below here:
![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/a9d2adc0-f543-430a-8623-4e1367f4d637)



What if we want to create siblings in the nested structure?
We can convert the 3rd attribute to an array.

So here we've just put the child attribute(3rd attribute) of the child div element in an array.

![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/17564fc2-8b2f-4b14-b069-1faf27c0d8b5)

![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/c7fc12c3-c483-4fea-92fd-aa34f20e73ae)


But what if we need, 2 sibling children tags under the parent tag. Should we put those 2 children in an array for the parent div's child attribute? like below.

![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/44bc8da6-0e7a-44f2-8ad5-40162cad574e)

![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/3211539c-000d-4c43-a095-0c777d918cbe)

![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/65daec7b-1620-44ad-9040-69290867f889)

It makes the code look long and messy. We will need to create more complex nested structures when we move forward. So for this JSX helps in this place when we need to create multiple tags/elements. We will be using React inside JSX.


Next is, if we try having a h1 in html file under root and render the same content we've rendered now. Content in html file gets REPLACED by the content we rendered using React.

![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/ec87111a-e003-4b5f-aa17-5a75e39a3503)

![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/b574d782-bc0c-42fd-b3f7-7c83859236fd)

To prevent this we can render the React content in a separate container i.e under a different div [react-container] and separate it from the root that we set for React[root]. This means react renders only under the root that we set for it.

![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/c7f55222-f655-4285-993d-ecfb7696c840)

![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/0d7291b7-5712-46a9-b1f9-2ac54f29644d)


Since React is a library, we can use it even in an already existing app to build a small part of the application(which was not built using React already) as well. We can create a large-scale application also using React.



Async and Defer attributes in script tag:

When we load the web page, 2 things happen -> HTML parsing & loading of scripts. Loading of script contains 2 parts - one is fetching the script from the network and second is executing the script line by line. 

<script src=""> </script>
When HTML parsing is happening and it encounters a Script tag, parsing is paused, it fetches the script and executes in then and there. Then parsing continues again. So here, Javascript is actually blocking the rendering of HTML.

<script async src=""> </script>
When async is used in the script tag, the script is fetched asynchronously when the parsing is going on. Once fetched, parsing is paused and the script is executed then and there as soon as the scripts are available in the browser. Then parsing continues.

<script defer src=""> </script>
When defer is used, the script is fetched parallelly when HTML parsing is going on but doesn't get executed as soon as the script is available. Only when parsing is completed, the scripts are executed.

Figure explanation from YT video:

![image](https://github.com/Gayathri229/NamasteReact/assets/60467364/559524a7-9ffa-4e8c-a856-27ecd74c5a33)


Which should be used where?
Async doesn't guarantee the order of execution of scripts but defer does. When we have multiple dependent scripts, we cannot rely on Async. So defer will be good to use here.

When we are fetching scripts that are independent of our code, Async can be used. 

Using Defer is like getting the best of both worlds. Mostly defer should be used.
