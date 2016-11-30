---
layout: post
comments: true
title: Programming Session 13
---
 
I made a bit more progress today.

Got through DOM manipulation basics. The easiest way for me to make sense of event listeners is to compare them to PowerPoint transitions. Also, there’s a surprising amount of functions needed to toggle an event on or off. But I have a feeling I’ll get used to that with time and practice.

Currently working on the score keeper exercise. Before going through the solutions, I attempted to at least make the numbers work by myself. I got around this far before coming into roadblocks on how to implement score limits:

{% highlight javascript %}
var p1Score = 0;
var p2Score = 0;
var score = document.querySelector("h1");
var p1Button = document.getElementsByTagName("button")[0];
var p2Button = document.getElementsByTagName("button")[1];
var reset = document.getElementsByTagName("button")[2];
var limit = document.getElementById("limit");

p1Button.addEventListener("click", function() {
	p1Score++;
	score.textContent = p1Score + " to " + p2Score;
});

p2Button.addEventListener("click", function() {
	p2Score++;
	score.textContent = p1Score + " to " + p2Score;
});

reset.addEventListener("click", function() {
	p1Score = 0;
	p2Score = 0;
	score.textContent = p1Score + " to " + p2Score;
});
{% endhighlight %}

There’s a lot of refactoring that needs to be done, such as changing the scores into spans. But this code *worked*, which is better than what I expected.

Tomorrow I’ll be refactoring this code and adding in score limits and a bit more DOM manipulation. It’s tough, but I’m excited to succeed!

Unrelated, but I just signed up for the December JLPT N1 test. Going to have to double my study to attain it. Unlikely that I’ll pass this round, but there’s no harm (besides a bit of money wasted!) in trying it!