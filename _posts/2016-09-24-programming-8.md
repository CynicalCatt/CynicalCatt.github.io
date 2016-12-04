---
layout: post
comments: true
title: Programming Session 8
---
 
Started learning quite late today. Had work on the morning, then chilled back with some [Days (anime)](https://myanimelist.net/anime/32494/Days_TV). Which, by the way, went exactly like I expected… but was still awesome nonetheless. My heart pains for Seiseki! 😦

Today I began learning about functions. Did it before, so nothing new, just revision. I did, however, finally learn about [the difference between console.log() and return](http://stackoverflow.com/questions/21020608/difference-between-console-log-and-return-in-javascript). I’ve been taught it several times, but I never seemed to get it. The explanation was too vague, peppered with too many technical terms, or just plain not there. Cole Steele’s method of dedicating a video to actually *show* the difference finally got it through my thick skull. Thank you, Cole Steele! 🙂

That said, the functions problem set wasn’t easy. I was able to create a function that asked for a number and determined if it was even quite easily:

{% highlight javascript %}
function isEven(number) {
	var number = prompt("Enter a number!");
	if (number % 2 === 0) {
		return "True";
	}
	else {
		return "False"
	}
}

isEven()
{% endhighlight %}

And with [a bit of research](http://stackoverflow.com/questions/1144783/replacing-all-occurrences-of-a-string-in-javascript), I was easily able to turn a kebab string into a snake string:

{% highlight javascript %}
function kebabToSnake(string) {
	return string.replace(/-/g, "_");
}

kebabToSnake()
{% endhighlight %}

But because of my shitty math skills, I was unable to figure out how to find the factorial of an inputted number on my own. In the end, [Stack Overflow](http://stackoverflow.com/questions/4438131/factorial-of-a-number) saved my butt, but it took going through the solutions video to really make sense of the answer. I also learned about the [*= operator](https://www.tutorialspoint.com/cplusplus/cpp_operators.htm).

I know I’m still learning, so it’s not expected for me to get these right. But it’s still frustrating nonetheless. I’m still going to power through anyway. Practice and constant learning will eventually make close to perfect.

Functions are crucial for any and all programming languages, so I spent a lot of time today trying to understand them in their entirety. Went through scopes (again, revision) and higher order functions. Learnt about [anonymous functions](http://www.w3schools.com/js/js_function_definition.asp), but find them annoying to read and type. Hopefully I don’t have to use them a lot…

Next up is arrays! Another topic that I don’t particularly like, but have to do well at. Hopefully all goes well.