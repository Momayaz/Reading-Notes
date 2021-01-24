# Pre-rendering
Before we talk about data fetching, let’s talk about one of the most important concepts in Next.js: Pre-rendering.

By default, Next.js pre-renders every page. This means that Next.js generates HTML for each page in advance, instead of having it all done by client-side JavaScript. Pre-rendering can result in better performance and SEO.

Each generated HTML is associated with minimal JavaScript code necessary for that page. When a page is loaded by the browser, its JavaScript code runs and makes the page fully interactive. (This process is called hydration.)

You should see that your app is rendered without JavaScript. That’s because Next.js has pre-rendered the app into static HTML, allowing you to see the app UI without running JavaScript.



## How to Statically Generate Pages with Dynamic Routes (Links to an external site.)?
In our case, we want to create dynamic routes for blog posts: (Links to an external site.)
We want each post to have the path /posts/, where is the name of the markdown file under the top-level posts directory.Since we have ssg-ssr.md and pre-rendering.md, we’d like the paths to be /posts/ssg-ssr and /posts/pre-rendering. (Links to an external site.)
Development v.s. Production (Links to an external site.)
In development (npm run dev or yarn dev), getStaticPaths runs on every request.
In production, getStaticPaths runs at build time.

## Deploying
General steps for deployment on Vercel:

Initialized the git repository locally
Push to gitHub
Create a Vercel Account
Install Vercel for GitHub
Import your repository
Deploy

 (Links to an external site.)Deploy to Vercel
The easiest way to deploy Next.js to production is to use the Vercel platform developed by the creators of Next.js.


Vercel is an all-in-one platform with Global CDN supporting static & JAMstack deployment and Serverless Functions. We believe Vercel is the optimal place to deploy Next.js apps. You can start using it for free — no credit card required.