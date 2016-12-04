---
layout: post
comments: true
title: Programming Session 31
---
 
Started off today learning about [NPM](https://www.npmjs.com/).

Long story short, it’s a manager for [libraries](https://www.quora.com/What-does-library-mean-in-the-case-of-programming-languages), which are also known as *“packages“*. It enables package usage for backend coding. Using the CMD, it also makes installing known packages extremely quick and easy. In short, a very useful tool.

Then I learned about the [difference](http://stackoverflow.com/questions/4099975/difference-between-a-module-library-and-a-framework) between a library and a framework. If I were to put it into my own words: A framework is equivalent to filling out the blank spaces in half-formed sentences (*ex: I am _____!*), while a library is taking an entire quote and figuring out how to make it fit in your paragraph, which *might* include a bit of modification.

Afterwards, I got to learn a bit more about how to judge a framework. Terms like [heavyweight and lightweight](http://stackoverflow.com/questions/19244830/what-is-mean-by-a-lightweight-framework)… [unopinionated and opinionated](http://stackoverflow.com/questions/802050/what-is-opinionated-software)… and such. The answers found through a Google search can be a bit difficult to understand, so in layman’s terms:

* **The “weight” of a framework is determined by how many “blank spaces” there are.** Lightweight has more, heavyweight has less. On a conceptual level, lightweight frameworks are easier to understand than heavyweight ones, because they “do less” for you… hence why there’s more blank spaces.
* **Opinionated frameworks make you follow “their way” of doing things more.** When coding, there are many ways to get the same result. Opinionated frameworks lock you into their way of getting something, while unopinionated frameworks give you freedom of choice.


Finally, the time came to use [Express](https://expressjs.com/)!

Though before doing so, I had to learn a bit more about HTTP requests. Specifically, what **routes** were. Basically, routes are instructions written to receive, decipher, and respond to HTTP requests! Simple.

Creating route instructions using Express was even easier. As long as you know about the different types of HTTP requests, you can understand them easily with a bit of logical thinking. Here’s some of the key points:

* You can make a 404 page using the “*” route! Important to put it last though, because it matches *everything* (like in CSS!) and the computer always reads from *top to bottom*, so it’ll cancel out all other route instructions!
* Route / path parameters let you define patterns to listen for, so you don’t have to repeat app.[HTTP request] a bunch of times.
* The “:” is one such parameter. For example, you can make an instruction that listens for “/r/:sectionName“. So no matter if you search for “/r/cats” or “/r/dogs“, that one instruction will listen to both and respond accordingly.
* Using “req.params“, you can find out the content of *:sectionName* and use it to redirect users to the appropriate pages! Even works for multiple parameters. 🙂


Though understanding the concept is simple, actually applying it is a bit more difficult.

For example, in one of the exercises, I had to create a GET request that returned a user-defined word, a user-defined number of times. So if I typed */repeat/woof/100*, I would expect the page to be filled with “woof” 100 times. The difficulty lies in that *res.send()* itself doesn’t seem to work in loops, so you have to save the loop input into a variable and at the very end, *res.send()* that. My code for that specific section is as follows:

{% highlight javascript %}
app.get("/repeat/:typedInput/:times", function(req, res) {
   var typed = req.params.typedInput;
   var times = parseInt(req.params.times, 10);
   var string = "";
   for (var i = 0; i < times; i++) {
     string += typed += " ";
   };
   res.send(string);
});
{% endhighlight %}

I ended today’s session by going through what a [package.json](https://docs.nodejitsu.com/articles/getting-started/npm/what-is-the-file-package-json/) was and why it was needed.

**For my own reference:** It’s a file that lists all of the other packages that a framework depends on to work properly. You can create a new package.json file using “npm init“and quickly register a package you’re dependent on into it using the “–save” flag during package installation.

Tomorrow I’ll be learning more about Express. Fun times await! 🙂