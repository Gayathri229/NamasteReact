If we want to run the project, we give the command "npx parcel index.html". But we can also do this by putting the command in package.json file under scripts field. We can name it as anything we want and give the command under that, say  
scripts : {
"devBuild": "parcel index.html",
"prodBuild": "parcel build index.html"
}  

Now we can use the command "npm run devBuild" for building dev build and "npm run prodBuild" for prod build. Here, if we named our devBuild command as "start", we can use the command "npm start" for the dev build command. start is the keyword reserved by npm for this. Same command wont work for any other names.


JSX is a Javascript syntax that is easier to create React Elements.    
JSX is NOT a part of React.  
JSX is a convention where we merge JS and HTML together.  
JSX is NOT HTML in JavaScript. JSX is HTML LIKE / XML LIKE Syntax.  
