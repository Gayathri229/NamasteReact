# NamasteReact

CDN - It is a place where React libraries are hosted. We are fetching it from there and using it in our code.


In React and web development in general, a CDN stands for "Content Delivery Network." It is not specific to React but is a concept that applies to serving and delivering various types of content, including JavaScript files used in React applications.

A CDN is a network of servers distributed across different geographical locations. Its primary purpose is to store and deliver web content, such as JavaScript files, images, stylesheets, and other assets, to users more efficiently and quickly. Here's how a CDN works in the context of a React application:

1. **Faster Content Delivery:** When you build a React application, it often includes various JavaScript libraries and dependencies. These files can be quite large. CDNs store copies of these files on multiple servers around the world. When a user accesses your React application, the CDN serves these files from a server location that's physically closer to the user, reducing the time it takes to load the content.

2. **Load Balancing:** CDNs automatically distribute the incoming requests to the nearest or least busy server. This helps in load balancing and ensures that your React application loads quickly and is available even during high traffic.

3. **Caching:** CDNs often cache content. Caching means that frequently requested content is stored temporarily on the CDN servers. This reduces the load on your web server and speeds up content delivery. However, you need to ensure that your files are correctly versioned or cached to avoid serving outdated content to users.

4. **Reliability:** CDNs are designed to be highly available and reliable. They have redundancies in place, so if one server fails, another can take over. This helps in ensuring your React application is available to users even during server outages.

To use a CDN in a React application, you typically reference external libraries or resources (e.g., React itself, React Router, or other third-party JavaScript libraries) from their respective CDN URLs in your HTML or JavaScript code. Here's an example of how you might include React from a CDN in your HTML file:

```html
<script src="https://cdnjs.cloudflare.com/ajax/libs/react/17.0.2/umd/react.production.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/react-dom/17.0.2/umd/react-dom.production.min.js"></script>
```

By using a CDN for these libraries, you don't need to host the files on your own server, and your users can benefit from faster load times and a more reliable experience when accessing your React application.
