# Hack The Web
Just a repo gathering a usefull list of HTML, CSS or JS workaround that help me to easily and fastly dev web-app that are cross-browser compatible. Feel free to add your 2 cents 🤘

**EDIT: Work In Progress**

-------
# Web Usage & Dev Practices

### Stats *[USAGE]*
Lists of websites to check web features compatibily between browsers, plus divers stat websites useful to compare browser usages and others...

http://caniuse.com

http://gs.statcounter.com/

### Workflow & Tips *[GETTING STARTED]*
Google's Web Fundamentals to better understand what is important while developping on the web today
https://developers.google.com/web/fundamentals/getting-started/

A useful documentation created by the Mozilla Community and translated into many languages
https://developer.mozilla.org


-------
# CSS
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
Still prefer `transform` css rule more than `zoom` except if you really need it. `Zoom` is NOT a solution for mobile display.


-------
# JS
### Detecting IE *[WORKAROUND]*
While developping web-app IE has always been a time killer to found workaround, due to its different versions bringing each time different "unique" rendering. It can also be a pain to detect IE and which version the user is using.

Here is a ready-to-use solution brought by @gapcode on Code Pen that does the job.

 - *Solution:*

https://codepen.io/gapcode/pen/vEJNZN

-------
# HTML
### DOM *[EXPERT]*
Today React.js is popular to create web-app, and more and more framework like Vue.js get their ways too. They tend to ease the developement of web-app and help you to better/fastly produce, although they add more complexity to DOM rendering.

 - *Here you can started understand what is DOM:*

https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model/Introduction

It can be useful to understand the interaction your rendering process is doing with the DOM ; especially when you tend to come from JQuery and you'd like to use it with React. You'll understand it's not the best thing to do, but if you really need to that

 - *React + JQuery:*
  
https://stackoverflow.com/questions/38836553/how-to-use-jquery-ui-with-react-js/40350880#40350880
