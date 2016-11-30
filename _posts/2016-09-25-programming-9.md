---
layout: post
comments: true
title: Programming Session 9
---
 
Arrays!

Another part of most programming languages that I don’t really like, but have to learn and master anyway. Luckily, every time I review it, I end up understanding it a little bit more.

This time, I learned about [push](https://developer.mozilla.org/en/docs/Web/JavaScript/Reference/Global_Objects/Array/push)/[pop](https://developer.mozilla.org/en/docs/Web/JavaScript/Reference/Global_Objects/Array/pop), [unshift](https://developer.mozilla.org/en/docs/Web/JavaScript/Reference/Global_Objects/Array/unshift)/[shift](https://developer.mozilla.org/en/docs/Web/JavaScript/Reference/Global_Objects/Array/shift), and all the other interesting array methods that exist out there. Most textbooks or courses usually don’t cover these until way later, after I’ve already given up on them. Cole Steele also covered [basic nested arrays](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Indexed_collections), which are surprisingly easy once you get used to them.

**Next up was creating a small to-do list web application.** After learning about what it *should* be able to do, I was easily able to create most of it myself. The only part I stumbled upon was how to get the web application to *remember* the new to-dos that I put into the variable “list”. Going through the solutions video made me realize that if you’re going to prompt the user for input *repeatedly*, you’re going to need to ask once outside the loop and one more time at the very end, inside the loop. My finished code ended up like this:

{% highlight javascript %}
var list = [];
var toDo = prompt("What would you like to do?");

while (toDo !== "quit") {
	if (toDo === "list") {
		console.log(list);
	}

	else if (toDo === "new") {
		list.push(prompt("Enter task here!"));
	}

	toDo = prompt("What would you like to do?");
}

console.log("You've successfully quitted the app.");
{% endhighlight %}

Remember anonymous functions? Yeah, they’re back for array iterations… or in simpler words, array loops. As usual, I don’t enjoy them, but *now* I can see how useful they’d be on my future blog, especially when combined with the forEach function.

Applying it to the to-do list web application turned out to be surprisingly simple. Without listening to Cole Steele’s explanation, I was able to make it function mostly by myself, with [only a little research](http://stackoverflow.com/questions/5767325/how-to-remove-a-particular-element-from-an-array-in-javascript) on how to remove an array item. The way I went about deleting a to-do item differs from his, but it achieves the same result:

{% highlight javascript %}
var list = [];
var toDo = prompt("What would you like to do?");

while (toDo !== "quit") {
	if (toDo === "list") {
		listTask();
	}

	else if (toDo === "new") {
		addTask();
	}

	else if (toDo === "delete") {
		deleteTask();
	}

	var toDo = prompt("What would you like to do?");
}

console.log("You've successfully quitted the app.");

// FUNCTIONS BELOW

function listTask() {
	console.log("***********");
	list.forEach(function(task, index) {
		console.log(index + ": " + task);
	})
	console.log("***********");
}

function addTask() {
	var task = prompt("Enter task here!");
	list.push(task);
	console.log(task + " was added to the list.");
}

function deleteTask() {
	toDelete = prompt("What do you want to delete?");
	list.forEach(function(task) {
		var index = list.indexOf(toDelete);
		if (index > -1) {
			list.splice(index, 1);
		}
	})
	console.log("Task is removed.");
}
{% endhighlight %}

Alright, that’s it for today. Got school tomorrow.

By the way, before calling it quits for today: I answered my first coding question on [/r/learnprogramming!](https://www.reddit.com/r/learnprogramming/) 🙂   It’s a sign that I’m steadily improving. I may not be able to refactor my code perfectly, but I can figure out a way to achieve certain things, and I’m pretty darn proud I’ve gotten this far.