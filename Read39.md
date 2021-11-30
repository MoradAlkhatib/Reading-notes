# Next.js Assets, Metadata, and CSS
Assets
When we put static files like images and video under top-level ‘public’ folder. Files in the public folder can be referenced by pages.

So we can use the picture vercel.svg into our first-post page.

Metadata
Metadata like html tag <head> has been instead of <Head> , which is React component in Next.js. We can add <Head> into our first-post.js
  
  CSS
Next.js use styled-jsx which is a CSS in JS, we can write the CSS only for the specific component. Besides, Next.js allows to import .css and .scss files.
We can also create the _app.js for the global entry point, then import CSS file for the global CSS styling.
  Layout Component
We can create a layout as a component with CSS styling import.

Create the folder components and styles in the top level.
Create layout.js and layout.module.css in the components folder.
Create the folder in the top level
Create a utility CSS classes utils.module.css in styles folder for reuse css style.
Now we can easy use the layout.js in our first-post.js
```
import Head from 'next/head'
import Layout, { siteTitle } from '../components/layout'
import utilStyles from '../styles/utils.module.css'

export default function Home() {
  return (
    <Layout home>
      <Head>
        <title>{siteTitle}</title>
      </Head>
      <section className={utilStyles.headingMd}>
        <p>[Your Self Introduction]</p>
        <p>
          (This is a sample website - you’ll be building a site like this on{' '}
          <a href="https://nextjs.org/learn">our Next.js tutorial</a>.)
        </p>
      </section>
    </Layout>
  )
  
 ```
# React Context 
React context is an essential tool for every React developer to know. I lets you easily share state in your applications.
In this comprehensive guide, we will cover what React context is, how to use it, when and when not to use context, and lots more.
  
### What is React context?
React context allows us to pass down and use (consume) data in whatever component we need in our React app without using props.
In other words, React context allows us to share data (state) across our components more easily.
### When should you use React context?
React context is great when you are passing data that can be used in any component in your application.
These types of data include:

Theme data
User data (the currently authenticated user)
Location-specific data (like user language or locale)
Data should be placed on React context that does not need to be updated often.

Why? Because context was not made as an entire state management system. It was made to make consuming data easier.
You can think of React context as the equivalent of global variables for our React components. 
### What problems does React context solve?
React context helps us avoid the problem of props drilling.
Props drilling is a term to describe when you pass props down multiple levels to a nested component, through components that don't need it.
Here is an example of props drilling. In this application, we have access to theme data that we want to pass as a prop to all of our app's components.
As you can see, however, the direct children of App, such as Header, also have to pass the theme data down using props.
  
### How do I use React context?
Context is an API that is built into React, starting from React version 16.
This means that we can create and use context directly by importing React in any React project.
There are four steps to using React context:
Create context using the createContext method.
Take your created context and wrap the context provider around your component tree.
Put any value you like on your context provider using the value prop.
Read that value within any component by using the context consumer.
  
Let's break down what we are doing, step-by-step:

Above our App component, we are creating context with React.createContext() and putting the result in a variable, UserContext. In almost every case, you will want to export it as we are doing here because your component will be in another file. Note that we can pass an initial value to our value prop when we call React.createContext().
In our App component, we are using UserContext. Specifically UserContext.Provider. The created context is an object with two properties: Provider and Consumer, both of which are components. To pass our value down to every component in our App, we wrap our Provider component around it (in this case, User).
On UserContext.Provider, we put the value that we want to pass down our entire component tree. We set that equal to the value prop to do so. In this case, it is our name (here, Reed).
In User, or wherever we want to consume (or use) what was provided on our context, we use the consumer component: UserContext.Consumer. To use our passed down value, we use what is called the render props pattern. It is just a function that the consumer component gives us as a prop. And in the return of that function, we can return and use value.
What is the useContext hook?
Looking at the example above, the render props pattern for consuming context may look a bit strange to you.

Another way of consuming context became available in React 16.8 with the arrival of React hooks. We can now consume context with the useContext hook.

Instead of using render props, we can pass the entire context object to React.useContext() to consume context at the top of our component.
  
You may not need context
The mistake many developers make is reaching for context when once they have to pass props down several levels to a component.
  
#### React context caveats
Why it is not possible to update the value that React context passes down?

While it is possible to combine React context with a hook like useReducer and create a makeshift state management library without any third-party library, it is generally not recommended for performance reasons.

The issue with this approach lies in the way that React context triggers a re-render.

If you are passing down an object on your React context provider and any property on it updates, what happens? Any component which consumes that context will re-render.

This may not be a performance issue in smaller apps with few state values that are not updated very often (such as theme data). But it is a problem if you will be performing many state updates in an application with a lot of components in your component tree.

### Conclusion
I hope this guide gave you a better understanding of how to use React context from front to back.
If you want an even more in-depth grasp of how to use React context to build amazing React projects, check out The React Bootcamp.

#### Want to become a React pro? Join The React Bootcamp
The React Bootcamp takes everything you should know about learning React and bundles it into one comprehensive package, including videos, cheatsheets, plus special bonuses.
  
