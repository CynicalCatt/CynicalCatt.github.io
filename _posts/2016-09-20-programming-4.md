---
layout: post
comments: true
title: Programming Session 4
---
 
I’m trying to approach coding like building a habit. Doing a bit every day will eventually help it all stick in my head. Typhoon days like today really bring that motivation down, but I’m still going at it! 🙂

The Tic Tac Toe exercise was a bit difficult. Cole Steele’s hints set up the basic table, but it took some Googling to discover [how to get rid of the table border](http://www.w3schools.com/css/css_table.asp), put borders only on certain sides, and [center the whole table](http://stackoverflow.com/questions/22285633/how-to-align-entire-table-to-right-with-css). I’m pretty sure there are better ways of going about this exercise, but as a newbie using just a tad bit more than what my instructor taught me, here’s what I did:

**HTML**
```html
<body>
	<h1>Tic Tac Toe</h1>
	<table>
		<tr>
			<td></td>
			<td></td>
			<td></td>
		</tr>
		<tr>
			<td></td>
			<td></td>
			<td></td>
		</tr>
		<tr>
			<td></td>
			<td></td>
			<td></td>
		</tr>
	</table>
</body>
```

**CSS**
```css
/*TITLE*/
h1 {
	text-align: center;
}

/*REMOVE BORDER, CENTER TABLE*/
table {
	border-collapse: collapse;
	margin-right: auto;
	margin-left: auto;
}

/*BOX SIZE*/
td {
	width: 100px;
	height: 100px;
}

/*LEFT OF MIDDLE SQUARE*/
tr:nth-of-type(2) td:nth-of-type(1) {
	border-top: 2px solid black;
	border-bottom: 2px solid black;
}

/*RIGHT OF MIDDLE SQUARE*/
tr:nth-of-type(2) td:nth-of-type(3) {
	border-top: 2px solid black;
	border-bottom: 2px solid black;
}

/*MIDDLE SQUARE*/
tr:nth-of-type(2) td:nth-of-type(2) {
	border: 2px solid black;
}

/*ABOVE MIDDLE SQUARE*/
tr:nth-of-type(1) td:nth-of-type(2) {
	border-left: 2px solid black;
	border-right: 2px solid black;
}

/*BELOW MIDDLE SQUARE*/
tr:nth-of-type(3) td:nth-of-type(2) {
	border-left: 2px solid black;
	border-right: 2px solid black;
}
```

Looking at the solutions video taught me that CSS classes were made to reduce redundant code. In short, be a lazy programmer! The less you have to type to get a result, the *better*! Or maybe not, but that’s what I got out of this. Incredibly similar to writing an English essay…

Before moving onto the next exercise, I attempted to replace all the images with some of [my favorite fan art](https://www.google.co.jp/search?q=%E3%81%91%E3%82%82%E6%9D%BE&source=lnms&tbm=isch&sa=X&ved=0ahUKEwjYv6ed7Z3PAhUaHGMKHcn7DFgQ_AUICCgB&biw=1280&bih=616) so I could take a screenshot and show off to my friends. To my surprise, I came across a conundrum: [When you have images (or anything, really) of differing sizes, you can’t put them all in the same line using floats.](http://stackoverflow.com/questions/5234749/css-floating-divs-at-variable-heights) At least, it’s not possible with pure CSS. Hopefully later on, I’ll stumble across a way to solve this issue!

The “make a blog from scratch” exercise was really fun! I went into it a bit nervous, but Cole Steele taught well enough for me to pull off the general look without needing to look at the solution! I even found a nifty, easy way to [get my <hr> to look incredibly cool](https://css-tricks.com/examples/hrs/). The best part about this trick is that it’s a background color, which means it’s applicable on other elements as well. I tested it on my “quote” paragraphs and got a really nice effect:

![cool-quote](http://www.pixhoster.info/f/2016-11/b0424308363ee1c60c936d087e0aeb80.png){:class="img-responsive img"}

My thinking process went like this:

1. Style the border on the body.
2. Write all the text, including that <hr>.
3. Sort out body width, margins, padding.
4. Group dates, article titles, quote blocks, and regular text as separate classes.
5. Style each class.
6. Style the <hr>.

Next session will focus on Bootstrap. I’ve never used it before, so I’m really excited to see what that’s like! I heard it can make my coding experience a little easier and faster. 🙂