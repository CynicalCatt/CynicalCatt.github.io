---
layout: post
comments: true
title: Programming Session 21
---
 
I set a goal to program and post every day for 21 days. While I couldn’t complete the “posting” part, I did complete the programming part! Feel extremely proud of myself. 🙂

Today’s focus was on styling the to-do list. Generally easy, but learned a few essential tips and tricks.

For instance, I learned [the difference](https://css-tricks.com/how-nth-child-works/) between :nth-child(2) and :nth-child(2n). The former selects only the 2nd child element, while the latter selects every 2nd child element. Simple algebra answers “why”, but the website I linked to explains it more thoroughly.

Also learned about the [box-sizing](https://developer.mozilla.org/en/docs/Web/CSS/box-sizing) CSS property and the [:focus](https://developer.mozilla.org/en/docs/Web/CSS/:focus) CSS selector class (aka pseudo-class). Important thing to note about the box-sizing property is that it isn’t automatically compatible with all browsers, so cross-browser compatibility code will need to be added.

Surprisingly, the transitions could also all be done using CSS, using a combination of pseudo-classes and transition properties. However, as expected, the toggle button needed jQuery to work. However, I personally found it a lot easier to use than Bootstrap. No wonder jQuery is so popular!

**With the styling over, the exercise was completed! Hurrah!**

Before uploading it to [my GitHub page](https://github.com/CynicalCatt), I decided to make some minute changes. Instead of a to-do list, I changed it to be a motivational quote list! Changed a few icons and the color scheme to match the overall “product”. Even added a motivational quote below the list! (That *might* eventually change to an overhead fixed banner… oh, the possibilities!)

Currently, I’m unable to store the data permanently so people can come back and still have the quotes they left. But as soon as I learn more about the backend, I’ll be coming back to add this functionality.

[**Here’s the live project page.**](https://cynicalcatt.github.io/motivation-quote-list/) Have fun experimenting with it! 🙂