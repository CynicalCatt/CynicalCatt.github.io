---
layout: post
comments: true
title: Programming Session 11
---
 
A common myth is that [it takes 21 days to create a habit](http://www.huffingtonpost.com/james-clear/forming-new-habits_b_5104807.html). This has already been debunked by science, but my current goal is to study (and post!) every day for **21 days in a row**.

Had classes in the morning and spent some time laughing at the [2016 USA Presidential Debate](https://www.youtube.com/watch?v=EuHuzhzb1nc), so I got to my programming studies quite late today. Ah well. It’s what you make of it that counts, eh?

Creating arrays with nested objects and using array iteration on them helped me learn a **key lesson**: In your array iteration, there’s no *need* to specify the object’s position when retrieving data from it, because the iteration automatically delves into the array for you. This is what I mean:

{% highlight javascript %}
var movies = [
	{title: "Frozen", rating: 5, hasWatched: true},
	{title: "Presidential Debate 2016", rating: 2, hasWatched: true},
	{title: "The Matrix", rating: 3, hasWatched: false}
];
movies.forEach(function(movie) {
	if (movie.hasWatched !== true) {   //NOTE HOW IT ISN'T MOVIES[MOVIE].XXXX
		console.log("You have not watched " + movie.title + " - " + movie.rating + " stars.");
	}
	else {
		console.log("You have watched " + movie.title + " - " + movie.rating + " stars.");
	}
})
{% endhighlight %}

Methods are confusing to write and read. In fact, I have a feeling objects in general will be difficult to read if they have multiple nested properties or methods. But I can see the advantage in using them, I guess. When you get used to them, they can really help in organizing data.

Also learned about the key word *this*, but there were no exercises on it, so I haven’t fully absorbed it yet. It’s something that will be handled later in the course, I guess.

**With this, JavaScript basics are officially finished!** 🙂

Before going to bed, I spent some time learning a bit about the DOM. Specifically, selecting and manipulating document objects. I actually studied briefly on the concept many years ago, but back then, I didn’t know what it was called. To me, it was just a random fact. Now that I know it’s a vital part of creating awesome websites, I’m hyped up to learn more!