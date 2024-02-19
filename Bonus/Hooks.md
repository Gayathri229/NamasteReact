useParams, useContext - not core react Hooks.
useParams - Given by React router.

useMemo():  
https://react.dev/reference/react/useMemo  

PS: It caches only the last computed value, until the dependant value doesn't change. DOESN'T cache anything more than the LAST COMPUTED VALUE.  

Increases performance of app.
[Refer Demo.js file from YouTube clone project]


useRef() Hook:  

Why do we need this hook?   
When you have a value in your component for which you dont want the component to re-render.  

  
Refer Demo2 component example in YT project for the below explanation:  


A local variable, say a "let" variable doesn't trigger a re-render in our component. If we have a button which increases its value, each time we click the button, value gets increased in the back, but doesn't  
reflect in UI as a let variable doesn't trigger a re-render.  
Now, That is why, we use a state variable where it increases the value and triggers a re-render as well.  
Now, if we try to increase the value of X (let variable), after incrementing the State variable, it again starts from 0. This is because X gets refreshed after each re-render. A re-render means, the component   
i.e. the function is displayed again, which means its getting called again, a new execution context is created, a new memory space is created, new thread of execution is created and the thread is pushed into  
call stack.  

Ref variable:  
- So, a Ref variable is like a Let variable, where a re-render won't be triggered if its value is changed, BUT the value won't get RESET after a re-render. It will remember the value and display it when a  
component re-render occurs (due to some other reasons like, let's say the value of State variable changed or useEffect dependency value changed) and then we'll be able to see the updated value of Ref on Screen.  
- This means the value persists between re-renders i.e. React tracks the useRef value.  
- Ref is not a normal value. It's an Object which React gives you. We can access/update Ref's value directly using its "current" property i.e ref.current.  

![Screenshot 2024-02-19 185652](https://github.com/Gayathri229/NamasteReact/assets/60467364/be227886-726a-4d9d-a846-888f6c38f2ec)

