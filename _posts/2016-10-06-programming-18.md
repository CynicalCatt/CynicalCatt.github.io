---
layout: post
comments: true
title: Programming Session 18~20
---
 
I’m so sorry for not posting.

I was wrought with sickness for the past few days, so I couldn’t find the strength to post. However, I did do a little bit of programming every day. I meant it when I said I would program every day, even if I only had five minutes to spare!

With the few precious minutes I had each day, I focused my attention on learning the rest of jQuery. As I mentioned in my last post, jQuery is surprisingly easy to understand once you’ve got Vanilla JavaScript down. So it was easy to speed through the videos. jQuery effects in particular aren’t difficult, because my brain associates them with PowerPoint…

Today, before digging my hands into the to-do list exercise, I decided to learn a bit on how to navigate [GitHub](https://github.com/). Went through the famous [“Hello World” guide](https://guides.github.com/activities/hello-world/), then created a repository for the color game exercise I completed earlier in the course. Then created a project page, which hosts the project on GitHub’s servers, letting *anyone* access and play the game! **If you want to try the game, you can [click here](https://cynicalcatt.github.io/color-game-exercise/).**

Going through the to-do list exercise introduced me to new methods and concepts almost immediately. For example, I learned about the **event.stopPropagation()** method, which stops everything other than what I specified from activating. Useful when you’ve specified an object buried inside several layers of code. Also learned about the **.parent()**, a method that’s *extremely* useful for when you want to delete not only what you’ve specified, but what’s directly surrounding your specified object. Sounds confusing, but makes sense if you [look at the documentation](https://api.jquery.com/parent/) and give it a whirl.

Had to go through the solutions video a bit to figure out how to get the **.keypress()** method working, but from there, I was quickly able to search [Stack Overflow](http://stackoverflow.com/questions/9236332/jquery-how-to-empty-input-field) and get the “add a task” function working! 🙂

However, figuring out how to cross out finished tasks and delete them, using the same code, was a bit of a mystery. Had to go through the solutions video for that. Was introduced to [the difference between .on() and .click()](http://stackoverflow.com/questions/9122078/difference-between-onclick-vs-click), as well as a more dynamic way of writing the **.on()** method:

{% highlight javascript %}
$("ul").on("click", "li", function() {
	$(this).toggleClass("strikethrough");
});
{% endhighlight %}

Basically, if you *don’t* target the overall list, any new points created cannot be crossed out when you click on them. So you target the overall list by doing $(“ul”), then specify that when you “click” on a specific point <li>, that point will be crossed out.

With that done, overall functionality of the to-do list was completed!

Tomorrow’s focus is on styling the list to make it look extremely fancy. 🙂