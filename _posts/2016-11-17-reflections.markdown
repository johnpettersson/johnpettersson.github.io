---
layout: post
title:  "Reflections!"
date:   2016-11-17 10:00
comments: true
---

### Questions
- What do you think of pre-compiling your CSS?
  - Compare to regular CSS
  - Which techniques did you use?
  - Pros and cons?
- What do you think of static site generators?
- What type of projects are they suitable for?
- What is robots.txt and how have you configure it for your site?
- What is humans.txt and how have you configure it for your site?
- How did you implements comments to blog posts
- What is Open Graph and how do you make use of it?

### Answers

I'm not completely new to Sass, i have used it a little bit before.
Compared to regular old CSS it's great. I like the modularity, the ability to change a colour just once in the top of your stylesheet, nestings and mixins also makes making changes much easier.
I did not spend a lot of time on the style in this project so I only tried out a few techniques like saving colours in variables.
Though there are some cons with using a pre-compiler. For starters it makes debugging a bit harder. But you can fix that with source-mapping i suppose.
It do takes a little bit more time to get started with it though.


SSGs is a nice addition to my "tool-belt".
Especially since i'm coming from the previous html and css course where everything had to be written in every single file over and over again.
Making a change to a header or a footer on a site with multiple pages quickly gets time-consuming.
Jekyll reminds me a little bit of what you can do with php, (including headers and footers etc).
Except that this is all generated once and not per page request. That makes SSGs a lot faster and simpler.
SSGs are suited for sites where the content is all static, where there's no need for dynamic data or user input.
(Though there are some exceptions and solutions for this aswell in static sites aswell, for example disqus)


robots.txt is a file at the root of a web-directory that instructs the server what search engines to allow visits from, and to what parts of the website.
I created a very basic robots.txt that tells all robots that it should not visit my site.

```
User-agent: *
Disallow: /
```

A humans.txt is a file that contains information about the author(s) of the site. I created a simple one with my name and hometown.

I used disqus to implement comments on my site. After some "googling" i discovered that jekylls default theme [minima](https://github.com/jekyll/minima) contains code to embed disqus.
All i had to do was creating a disqus-account for my website and adding my disqus-shortname to my _config.yml file. (Though i did change minimas default embed-code a bit so that disqus was embedded below the post-div and not inside it.


Open Graph protocol is a way of determining what part of your content is previewed when shared in social media, such as facebook or slack.
I made use of it by adding some code into my _includes/head.html. If the page has a date variable set i treat it as an article and if it does'nt i treat it as a website.
The difference between the two being what data i include in meta-tags, such as author, publishdate etc.
