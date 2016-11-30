---
layout: post
comments: true
title: Programming Session 16
---
 
Don’t think I’ve ever mentioned this, but I have [hyperthyroidism](http://www.endocrineweb.com/conditions/hyperthyroidism/hyperthyroidism-overview-overactive-thyroid). In short, I get tired really easily, even after taking medication. When I have an ample amount of sleep, a good diet, and proper exercise, I can survive a day. When one of them is missing, my energy levels fall and anything that requires concentration – like programming or studying – becomes difficult.

The past few days, I haven’t been getting enough sleep or exercise, so my energy levels were pretty low. I *finally* got enough sleep though and I’ve come up with a way to exercise in quick bursts at home, so I was able to survive today.

I celebrated by finishing the color game exercise! 🙂

I won’t lie. It was daunting. If I didn’t follow Cole Steele as he was coding, I probably wouldn’t have been able to create it. There were a lot of pieces that I just didn’t think about, but that needed to be there, and he showed me how. Heck, even *with* following his instructions, I still had bugs that I had to solve on my own since I decided to add tiny little pieces of my own code to fix a few problems that I found along the way. I learned a lot though and I bet this code will come in very handy when I create *stuff* in the future.

One interesting thing I learned was about the CSS attribute [transition](https://developer.mozilla.org/en-US/docs/Web/CSS/transition). When applied correctly, it can make transitions look ever so pretty! I personally find a transition delay of 0.3 seconds to be optimal, but I guess it differs for everybody. I also learned how to make it more cross-browser compatible using [-webkit-transition and -moz-transition](https://developer.mozilla.org/en-US/docs/Web/CSS/transition#Browser_compatibility).

I also learned about the [ternary operator](https://developer.mozilla.org/en/docs/Web/JavaScript/Reference/Operators/Conditional_Operator). Really shortens the **if and else statements** code, but I guess you have to use it often enough to be able to read it easily. For reference’s sake, here’s one ternary operator in action:

{% highlight javascript %}
this.textContent === "easy" ? squaresNum = 3: squaresNum = 6;
{% endhighlight %}

**It can be read as:** If the text content is equal to “easy”, then squaresNum is 3. Otherwise, squaresNum is 6.

Short and straight to the point, but I can see why some people wouldn’t like it, since it isn’t exactly… *descriptive*.

On top of that, I learned what [design patterns](https://addyosmani.com/resources/essentialjsdesignpatterns/book/#whatisapattern) were and why they exist. Didn’t get into the nitty gritty, since the focus was on creating something and not making the code look pretty, but I’m sure I’ll be learning more about it in the future.

Tomorrow’s a new day and it starts with JQuery.