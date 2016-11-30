---
layout: post
comments: true
title: Programming Session 10
---
 
More arrays!

To be specific, I’m covering the problem set that I didn’t have the time (and energy) to do in my last session. Functions and arrays are surprising weak spots of mine, so it took me quite a while to complete this problem set.

With a little help from [Stack Overflow](http://stackoverflow.com/questions/4956256/loop-through-associative-array-in-reverse), I was easily able to print out an array in reversed order *without* reversing the entire array itself. Surprisingly, I was also able to create a function, max(), that printed out the max number in an array *all by myself*:

{% highlight javascript %}
function max() {
	var max = list[0];
	for (var i = 1; i <= list.length; i++) {
		if (max < list[i]) {
			max = list[i];
		}
	}
	console.log(max);
}

max();
{% endhighlight %}

However, no matter how much [Stack Overflow](http://stackoverflow.com/questions/16057672/sum-values-from-an-array-in-javascript) I peered through, I was unable to figure out how to get the sum of an array or check if all the items in an array were uniform. Going through the solutions and modifying them to accept a predefined array with a more experienced friend helped me truly realize the difference between return and console.log(). Mainly that one of them doesn’t always show up in the Chrome console while the other does. (Seriously. That’s all I did wrong.)

Now onto objects!

Never studied them before. Or maybe I have, but I have no knowledge of them. JavaScript objects seem to be easy enough to make and call.

…and that’s honestly it for today. I’ve been moving at a slower pace lately. It’s starting to take more time to do each section because I spend more time trying to code by myself before looking at the solutions, including debugging said code. But I’m sure I’ll get through the entire course. After all, I paid for it! 🙂