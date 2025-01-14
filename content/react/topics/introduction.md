---
date: 2024-12-31T00:00:00.000+02:00
instructor: "[[Marina Shafiq]]"
---
# 1	intro
## 1.1	what is react?
React is a JavaScript library for building user interfaces (UIs) on the web and mobile devices. Developed by Facebook, React allows developers to create reusable UI components, manage state changes, and optimize rendering performance.
## 1.2	why react?
- easy to get to if you know javascript
- improve performance using virtual DOM
- reusable components
- dedicated tools for debugging
# 2	SPA (single page application)
## 2.1	in the past
when users in the past request a page. the request an html page from the server and they wait until the server responds and sends the page back.
## 2.2	now in react
application is not dependant on request html pages. your webpage is dependant on javascript code on client. It doesn't request a new html page but rather it changes the actual page using javascript. Page essentially doesn't reload and reduces
## 2.3	SEO
Sometimes there are issues with SPAs with search engines because when you request initial page,  it returns blank page that has not content. Next.JS solves this by serverside rendering 
# 3	Virtual DOM
normally, when any change happens on the dom. the page reloads the dom. When a change happens react compares virtual dom to real dom then it only changes the actual dom that had changes to it
## 3.1	exmaple
![[Pasted image 20241231094953.png]]
when the timer here updates. Native DOM reloads the entire div to update the element being changed.
# 4	NPM
node package manager
## 4.1	node_modules
where pages are put

if you delete the node_modules. Does that mean that the package is not here? no the package json tells 'npm install' what to install
## 4.2	package
dependencies and their version
## 4.3	packacge lock
dependendies of package that you installed in detail
# 5	to install react
![[Pasted image 20241231100255.png]]
## 5.1	alt way
![[Pasted image 20241231100334.png]]
# 6	App Structure

## 6.1	node modules
node modules has all dependendies and 
## 6.2	public 
has all global images
## 6.3	assets
has small scale assets that are not site wide
## 6.4	app.jsx
## 6.5	index.css
global styles of application
## 6.6	main.jsx
main function that renders your application 
## 6.7	index.html
the only html page
typically you ony include SEO metadata only here
## 6.8	package
devDependencies
plugins that help you while writing project but don't affect production
## 6.9	vite.config.js
# 7	React components
![[Pasted image 20241231105633.png]]
functions return JSX which stands for Javascript XML, which looks like HTML. Which is used to return HTML elemnts i think.

It has a few limitations:
- class is called className

[babeljs.io](https://babeljs.io) shows you how jsx is rendered

- You cannot return more than one element. If you want to return multiple elements then return them inside a div. You can also use a Fragment to return multiple elements
![[Pasted image 20241231110002.png]]
in the above picture you still need to import the fragment module from react

- All tags need to have their closing tags present. as shown below
![[Pasted image 20241231110202.png]]

 - camelcase
 - for styles, you need two curly braces to retunn the styles in the inlines styles of the component
![[Pasted image 20241231110400.png]]

[transform.tools](https://transform.tools)

All components have first letter be capital.

You can use arrow functions as well to return components.
![[Pasted image 20241231111137.png]]
- calling compents in the application

![[Pasted image 20241231111818.png]]
- styles in react are global are not isolated to a certain component
- to handle events in react due to buttons or other elements you can inline ![[Pasted image 20241231113710.png]]
you can send event or callback

# Lab
![[Pasted image 20241231114422.png]]
