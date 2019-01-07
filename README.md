# Hack The Web
Just a repo gathering a usefull list of HTML, CSS or JS workaround that help me to easily and fastly dev web-app that are cross-browser compatible. Feel free to add your 2 cents 🤘 (with a PR of course)

You will also find a lot of article I find usefull or giving me inspiration to efficiently produce: startups, workflow, design, understanding hunder the hood...

**Work Always In Progress**

-------
## Table of Contents
  **TO CONTINUE**
- [Web Usage & Dev Practices](#web-usage--dev-practices)
  - [Getting Started *[START POINT]*](#getting-started-start-point)
  - [Stats *[USAGE]*](#stats-usage)
  - [Into Production *[WORKFLOW]*](#into-production-workflow)
  - [Design *[WORKFLOW]*](#design-workflow)
  - [Intiution vs Programing *[WORKFLOW]*](#intiution-vs-programing-workflow)
  - [How to succeed VS Learn to fail *[STARTUP]*](#how-to-succeed-vs-learn-to-fail-startup)
- [JS](#js)
- [CSS](#css)
- [HTML](#html)
- [Server](#server)
- [Legal Notice & Juridic stuff](#legal-notice--juridic-stuff)

### Contents Type
- *[START POINT]* : stands as a good starting for those who just begin in web
- *[USAGE]* : some handful informations to develop
- *[WORKFLOW]* : a given way to handle a project
- *[WORKAROUND]* : solution ready-to-use for developement issues
- *[EXPERT]* : more tricky or under-the-hood stuff
- *[STARTUP]* : for those who are interested in creating their own business

-------
## Web Usage & Dev Practices

### Getting Started *[START POINT]*
Google's Web Fundamentals to better understand what is important while developping on the web today
https://developers.google.com/web/fundamentals/getting-started/

A useful documentation created by the Mozilla Community and translated into many languages
https://developer.mozilla.org

### Stats *[USAGE]*
Lists of websites to check web features compatibily between browsers, plus divers stat websites useful to compare browser usages and others...

http://caniuse.com

http://gs.statcounter.com/

### Into Production *[WORKFLOW]*
Create large app at scale can be a pain... especially when you only focus on what tutorials teach you. Actually - eg with react - they tend to show you a workflow that works with one single page app. Here are alternativs that will help you:

- *Build large app at scale*

https://medium.com/@alexmngn/how-to-better-organize-your-react-applications-2fd3ea1920f1

http://engineering.kapost.com/2016/01/organizing-large-react-applications/

You may consider to structure your project by features, instead of by type.

- *And do I need redux ?*

https://stackoverflow.com/questions/35411423/how-to-dispatch-a-redux-action-with-a-timeout/35415559#35415559

- *Asynchronous actions - Redux example*

https://medium.com/@jtbennett/asynchronous-actions-in-redux-8412cf92a26f

### Design *[WORKFLOW]*
- *Design Sprint by Google Ventures - How to solve problems in five days with new ideas*

http://www.gv.com/sprint/

- *Invest in early database design to succeed - How to smartly build database architecture*

http://firstround.com/review/your-database-is-your-prison-heres-how-expensify-broke-free/

### Intiution vs Programing *[WORKFLOW]*
- *What is Functional Programming?*

https://medium.com/javascript-scene/master-the-javascript-interview-what-is-functional-programming-7f218c68b3a0

- *Overcoming Intuition in Programming*

https://amasad.me/intuition

- *Practical Functional Reactive Programming -take a breath-*

https://medium.com/appnroll-publication/practical-functional-reactive-programming-ae9bfc35897

### How to succeed VS Learn to fail *[STARTUP]*
- *Kill project before they kill you - learn when it's time to give up*

http://firstround.com/review/dont-play-with-dead-snakes-kill-projects-before-they-kill-you/

- *Growing startup*

http://firstround.com/review/fighting-factions-how-startups-can-scale-without-mutiny/

-------
## JS

### How to better use Fetch *[EXPERT]*
`fetch` is the hot new way to make HTTP requests in the browser. More than just being a better, more ergonomic API than XMLHttpRequest, it brings a lot of exciting new capabilities:

https://medium.com/cameron-nokes/4-common-mistakes-front-end-developers-make-when-using-fetch-1f974f9d1aa1

### Detecting IE *[WORKAROUND]*
While developping web-app IE has always been a time killer to found workaround, due to its different versions bringing each time different "unique" rendering. It can also be a pain to detect IE and which version the user is using.

Here is a ready-to-use solution brought by @gapcode on Code Pen that does the job.

 - *Solution:*

https://codepen.io/gapcode/pen/vEJNZN

-------
## CSS

### Flexbox *[WORKAROUND]*
Flexbox is a magic css rule that will help you to create responsive content more easily without the real needs of media queries: https://css-tricks.com/snippets/css/a-guide-to-flexbox/

However there might be a lot of differents issues depending on browser rendering, here is a list of workaround brought by the community.

 - *Workaround:*

https://github.com/philipwalton/flexbugs

### Zoom *[WORKAROUND]*
Not compatible with Firefox at all (https://bugzilla.mozilla.org/show_bug.cgi?id=390936). Better use `transform: scale(1.2)` being fully compatible now. However `scale` and `zoom` don't behave the same way at all ; while `scale` resize the content, zoom can resize a whole page and make it fit to viewport size (`scale` will leave empty spaces or make the page scroll). 

Even if `zoom` is not recommend as it can break your css page, you might really need it e.g. for printing purpose. Actually it can make your web-app fit the page size. Here is a possible workaround for Firefox:

 - *Workaround:*

```
body {
  transform-origin: top left;
  transform: scale(0.7);
  width: 142.85vw;
  height: 142.85vh;
}
```

 - *Issues:*

There might be issues while your content can be cut in height e.g. while printing with Chrome whereas `zoom` doesn't cut the content.
Still prefer `transform` css rule more than `zoom` except if you really need it. NB: `Zoom` is NOT a solution for mobile display.

-------
## HTML

### DOM *[EXPERT]*
Today React.js is popular to create web-app, and more and more framework like Vue.js get their ways too. They tend to ease the developement of web-app and help you to better/fastly produce, although they add more complexity to DOM rendering.

 - *Here you can start to understand what is DOM:*

https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model/Introduction

It can be useful to understand the interaction your rendering process is doing with the DOM ; especially when you tend to come from JQuery and you'd like to use it with React. You'll understand it's not the best thing to do, but if you really need to that

 - *React + JQuery (if needed):*
  
https://stackoverflow.com/questions/38836553/how-to-use-jquery-ui-with-react-js/40350880#40350880

------
## Server

### Deployement *[START POINT]*

List of service to deploy web-app:

- Heroku
- Now (from Zeit)

More to come...

### Serverless *[EXPERT]*

More to come...

------
## Legal Notice & Juridic stuff

### Licensing *[START POINT]*
- *Understanding React Patent licences*

https://medium.com/@raulk/if-youre-a-startup-you-should-not-use-react-reflecting-on-the-bsd-patents-license-b049d4a67dd2
 	
### Cookies and Privacy *[USAGE]*
- *Handling cookies with european laws*

https://github.com/AmauriC/tarteaucitron.js
