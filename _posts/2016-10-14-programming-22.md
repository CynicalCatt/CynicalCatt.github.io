---
layout: post
comments: true
title: Programming Session 22~28
---
 
Next exercise is a [Patatap](http://patatap.com/) clone. 🙂

Immediately, I learned something new: [Paper.js](http://paperjs.org/). Along with it, I learned about the [HTML canvas element](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API), which is similar to a drawing canvas on Word or PowerPoint, except that you can add animations and even *videos* on it.

Right afterwards, I learned about [cross-origin resource sharing](https://developer.mozilla.org/en-US/docs/Web/HTTP/Access_control_CORS). Took me a while to get it, but I’ll break down my thoughts like so:

* Cross-origin HTTP requests are basically requests for “stuff” (e.g. images, CSS style sheets) that one website makes to another separate website. So for example, A.com wants to load an image that’s originally from B.com, so it sends a request to B.com.
* Websites can accept or deny cross-origin HTTP requests. The act of being able to control access rights is known as HTTP access control.
* The entire act of sending, receiving, and controlling HTTP requests is called cross-origin resource sharing.


Fascinating and extremely useful. I can envision several scenarios where caring about it will make a huge difference.

Before getting into the meat of creating the clone, I went through a Paper.js exercise. Long story short, I failed so bad it was cringe worthy. On the bright side, I learned more about nested loops. Cole Steele’s explanation didn’t fully click into my head, so I took to Google to learn more.

[This visual example](http://labs.codecademy.com/BJwV#:workspace) helped me the most. If I were to explain it to myself, I’d say:
> Every time the outer loop goes through another iteration, the inner loop restarts. This continues until the outer loop has reached its limit.

Still not entirely confident in actually using nested loops, but now the concept makes sense! 🙂

Creating the clone by myself, without any guidance, was extremely difficult. I chalk that up to a lack of general programming experience, along with documentation that’s kind of difficult to understand. Tutorials were easy enough, but diving into Paper.js’ [reference page](http://paperjs.org/reference/global/) felt a little bit like wading through mud. In comparison, the [MDN documentation](https://developer.mozilla.org/en-US/) for HTML, CSS, and JavaScript was a lot easier to understand and parse through.

After muddling through the Paper.js code, diving into [Howler.js](https://howlerjs.com/) was a welcome move. The hardest part was actually installing it. First, I had to downgrade from Version 2.0 to Version 1.2.9 to get the script to work. Afterwards, I couldn’t find the sound pack that Cole Steele used, so I ended up downloading my own off [Freesound.org](https://www.freesound.org/). From there, it was a smooth ride.

One complaint I have is that there doesn’t seem to be a way to easily attach sound files to specific keys. I’d like to avoid having to create an object, individually name keys, and attach sound files to each key. I’d imagine that there’s a function out there to achieve that, but Google hasn’t been able to help me thus far. **If anyone has a quick and easy solution, please do tell me!**

Before moving on, I made slight alternations. I thought that circles looked a bit ugly, so I went through the tutorials a bit more and found out how to only get the outline to show up. Also inserted a random RGB color function to get random colors out of every keypress, since I don’t really like having a set color for each key.

Though I spent a ridiculously long time on this exercise, I’m not going to put it on GitHub. **One reason being that it’s kind of broken.** If you press any key that you haven’t specified in an object, something will show up, but none of the animations will work. Tried to fix it, but haven’t been able to.

More than anything, I’m not fond of working with Paper.js. I’ve tried liking it, but I just can’t summon up the urge to do anything more with it.

I spent many days stuck on this exercise (and this blog post!) because I fell sick and had to take a few days off studying. Hopefully, my recovery will bring about another round of constant studying.

Sorry for the wait everyone. Hope you enjoy this post! 🙂