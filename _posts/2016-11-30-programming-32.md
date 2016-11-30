---
layout: post
comments: true
title: Programming Session 32
---
 
It took me over a month, but I finally finished my first big project - *this blog*!

I wanted blogging to be simple, so I turned to a static site generator called [Jekyll](https://jekyllrb.com/). Using it on Windows was a pain, so for the first time ever, I downloaded and learned how to use Linux ([Ubuntu](https://www.ubuntu.com/)). Guided by Andrew Munsell's [free preview lesson](https://www.andrewmunsell.com/lesson/building-a-website-with-jekyll/), I set up the initial site layout.

**Overall setup time:** 1.5 weeks

I knew right away that I needed a collapsible sidebar, but I wasn't sure how to do it. [Bootstrap templates](http://www.designerslib.com/bootstrap-sidebar-menu-templates/) provided some answer, but customizing the template was incredibly difficult. Took a very long while to parse through the code, pick out what I needed, and use it to construct my own sidebar.

**Overall sidebar creation time:** 1.5 weeks

Creating the theme was also a bit tricky, because I didn't know where to start. In the end, looking at a [Tumblr theme's code](http://theme-hunter.tumblr.com/) helped me remember how to put things together to create cleaner, more organized code.

**Overall theme creation time:** 1 week

Next up was the smaller stuff, like sidebar links, pagination, creating loops to display multiple posts, etc. Those didn't take much time since the free preview lesson went into enough detail.

What *did* take more time was adding a few big features. Like a [Disqus](https://disqus.com/) comment section for every post. Or [Google Analytics](https://analytics.google.com/). Or even just code highlighting using [Rouge](https://github.com/jneen/rouge) and [Pygments style sheets](https://github.com/richleland/pygments-css).

Tips for those planning on implementing their own Jekyll site:
* [Stack Overflow](http://stackoverflow.com/questions/38486498/vertical-scroll-bars-in-jekyll-rouge) helped me customize the code highlighter to my liking.
* [This tutorial](https://sacha.me/articles/jekyll-rouge/) on implementing Rouge to a Jekyll site helped me get started on implementing the code highlighter.
* Michael Lee's [Google Analytics Setup for Jekyll tutorial](https://michaelsoolee.com/google-analytics-jekyll/) is all that's needed to get it set up.

**Overall feature implementation time:** 1+ weeks

Finally, I had to learn a little Git to get it up online using GitPages. [This page](https://help.github.com/articles/setting-up-your-github-pages-site-locally-with-jekyll/#step-1-create-a-local-repository-for-your-jekyll-site) helped a lot.

**Overall time spent learning Git:** Few hours

Now that basic functionality and design for this blog is done, I can go back and finish off the web development course I was taking!

Of course, more stuff will be added in the future and the template will probably become more modern and slick too. But for now, this is my blog.

Welcome!