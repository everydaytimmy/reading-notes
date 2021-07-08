### Next JS

https://nextjs.org/learn/basics/create-nextjs-app

Next.js provides a solution to all of the above problems. But more importantly, it puts you and your team in the pit of success when building React applications.

Next.js aims to have best-in-class developer experience and many built-in features, such as:

An intuitive page-based routing system (with support for dynamic routes)
Pre-rendering, both static generation (SSG) and server-side rendering (SSR) are supported on a per-page basis
Automatic code splitting for faster page loads
Client-side routing with optimized prefetching
Built-in CSS and Sass support, and support for any CSS-in-JS library
Development environment with Fast Refresh support
API routes to build API endpoints with Serverless Functions
Fully extendable

#### Create a Next.js app
To create a Next.js app, open your terminal, cd into the directory you’d like to create the app in, and run the following command:

`npx create-next-app nextjs-blog --use-npm --example "https://github.com/vercel/next-learn-starter/tree/master/learn-starter"`

Pages in Next.js
In Next.js, a page is a React Component exported from a file in the pages directory.

Pages are associated with a route based on their file name. For example, in development:

`pages/index.js` is associated with the `/` route.
`pages/posts/first-post.js` is associated with the `/posts/first-post route.`
We already have the pages/index.js file, so let’s create pages/posts/first-post.js to see how it works.

Create a New Page
Create the posts directory under pages.

Create a file called first-post.js inside the posts directory with the following content:

```
export default function FirstPost() {
  return <h1>First Post</h1>
}
```

The component can have any name, but you must export it as a default export.

Now, make sure that the development server is running and visit http://localhost:3000/posts/first-post. You should see the page:
