---
layout: post
comments: true
title: Jekyll Tutorial 1
---
 
To help out those just starting their Jekyll blog journey, I decided to create a tutorial series that'll go through the essentials. By the end, you should have a fully functioning blog that you can customize to fit your needs.

Before starting this tutorial, please note:

* I use **Linux ([Ubuntu](https://www.ubuntu.com/))** for any coding or command line work. If you're unfamiliar with using the Linux terminal, refer to [this tutorial](https://www.davidbaumgold.com/tutorials/command-line/) for command line basics.
* We will be hosting the blog on [GitPages](https://pages.github.com/). So if you don't have an account on [GitHub](https://github.com/) yet, you should make one.
* I use [Sublime Text](https://www.sublimetext.com/) to write my code. You can use the same thing or something similar.


> Initial Set-Up

Create a new repository on GitHub.

* If the blog's just another project, name it whatever you want.
* If you want your blog URL to be "https://[username].github.io", name your repository "**[username].github.io**". Note that you can only create *one website per account* with this type of URL, so decide wisely.
* Add .gitignore by typing into the filter "Jekyll" and select it.

![new-repository](http://www.pixhoster.info/f/2016-12/878f2b088521a041cbc797a3611190af.png){:class="img-responsive img"}

Now create a folder on your computer and give it the same name as your repository. Inside that folder, create the following files:

* _config.yml
* _includes folder
* _layouts folder
* _posts folder

Now open up <span class="attention">_config.yml</span> and type in the following (without the square brackets):

{% highlight yaml %}
name: [insert name of blog]
description: [insert blog description]
url: ""
markdown: kramdown
permalink: /:categories/:title/

gems: [jekyll-seo-tag]
{% endhighlight %}

Gems are plugins that let you add nifty extra features to your blog. A list of plugins made for Jekyll can be found [here](https://jekyllrb.com/docs/plugins/). For simple SEO optimization, I've already included the [Jekyll SEO plugin](https://github.com/jekyll/jekyll-seo-tag). You can click on the link to read more about it.

As the file name suggests, this is a configuration file for your entire blog. We'll play more with it later. For now, save and exit.

Now open up your terminal and move to your blog's directory. Type in <span class="attention">jekyll build</span>. This prompts Jekyll to build your website using the files and folders in the directory. While you'd normally be able to view the built website in the folder <span class="attention">_site</span>, because we haven't created any content for the website yet, this folder doesn't exist. Let's remedy that.

Create a new file, <span class="attention">index.html</span>. Add the following to it:

{% highlight markdown %}
---
layout: default
title: Home
---

{% for post in paginator.posts %}
	<h2 class="title-me">{{ post.title }}</h2>
	<p class="post-date">{{ post.date | date_to_long_string }}</p>
	<p>{{ post.excerpt }}</p>
	<p><a href="{{ post.url }}">Read More</a></p>
	<hr class="post-line">
{% endfor %}
{% endhighlight %}

The part inside the <span class="attention">---</span> lines is called 