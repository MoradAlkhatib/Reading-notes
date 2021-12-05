# Next.js - Dynamic Routes
Next.js alllows you to statically generate pages with paths that depend on external data.
enables dynamic URLs in Next.js
How to Statically Generate Pages with Dynamic Rountes
Create dynamic rountes for a blog posts:
each path to have the path /posts/<id>, where <id> is the name of the markdown file under the top-level directory.
ssg-ssr.md and pre-rendering.md, we’d like the paths to be /posts/ssg-ssr and /posts/pre-rendering
  
### How we can generate pages in Next.js and what are the steps in doing that ? 
Next.js allows you to statically generate pages with paths that depend on external data.

create a page called [id].js
export an async function called getStaticPaths from this page.
Implement getStaticProps to fetch necessary data for the post with a given id.

#### The Page must contain
- react component
- getStaticPaths : return array of possible values for id
- fetch necessary data for the post with id.
  
### Implement getStaticPaths 
First, let’s set up the files:
Create a file called [id].js inside the pages/posts directory. Also, remove first-post.js inside the pages/posts directory — we’ll no longer use this. Then, open pages/posts/[id].js in your editor and paste the following code. We’ll fill in … later

Then, open lib/posts.js and add the following getAllPostIds function at the bottom. It will return the list of file names (excluding .md) in the posts directory

Finally, we’ll import the getAllPostIds function and use it inside getStaticPaths. Open pages/posts/[id].js and copy the following code above the exported Post component
  
### Deploy to Vercel
The easiest way to deploy Next.js to production is to use the Vercel platform developed by the creators of Next.js.

Vercel is a serverless platform for static and hybrid applications built to integrate with your headless content, commerce, or database.

We make it easy for frontend teams to develop, preview, and ship delightful user experiences, where performance is the default.
