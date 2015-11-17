---
layout: post
comments: true
title:  "Assignment 1"
date:   2015-11-17 19:56:12
categories: 1DV022
---

This blog post is a reflection on the first exam assignment for the 1DV022 course. As written in a previous post,
the purpose of this assignment was to build a portfolio site using the Jekyll static site generator, where all styling was
done using the SASS CSS preprocessor.

## CSS Preprocessors

It was very pleasant to work with a CSS preprocessor, as it eliminates several of the inefficiencies experienced when working 
with plain CSS. The ability to use variables was a major difference that saved me a lot of time, as it allows for quick
 changes without having to search through all stylesheets to find where a certain value was used. I used this to experiment 
 with different color schemes rapidly. Another time saver was the possibility to do calculations with CSS values like pixels 
  and percentages, as well as helper functions like darken() to quickly adapt a certain color without having to look it up 
  or memorize hexadecimal codes every time. Nesting of elements allows for better readability, since there is no need to write 
  the same identifiers over and over again.

Besides saving time while developing, another benefit is the fact that all CSS is compiled into a single style sheet when 
the page is served by Jekyll. This allows for fewer HTTP requests and makes for a faster and smoother user experience.

Benefits of CSS preprocessors include, as mentioned above, the use of various programming concepts to speed up development and 
the compilation of all style into a single style sheet for faster page loads.

Disadvantages of using CSS preprocessors may be that they add slightly more complexity to a site, since they require a build step 
before they can be read by the browser. Also, debugging could become harder since the browser will refer to a line number in 
the compiled CSS instead of the actual line number in the source code (although there are workarounds for this). In larger projects,
there must be a consideration about the amount of mixins and includes of various smaller stylesheets; while these make for easier 
initial development they may make the code harder to debug and more unstable due to various dependencies.

## Static Site Generators

For this project I used the Jekyll static site generator. It is very easy to use and allows for fast development as it has 
most of the boilerplate code built in, and lets you just write pages and blog posts in Markdown after which it builds the site
from the content provided.

Since there is no database connection the site loads very fast, with minimal HTTP requests. The two main benefits of this are 
that the user does not have to wait very long for the pages to load, and that a site like this will scale quite well to a larger
 number of users. 
 
Static site generators are well suited for content that is, as the name suggests, static. Blogs, informational company websites, 
and portfolios are examples that come to mind. These pages typically aren't changed or updated very frequently, and do not need 
dynamic elements (like an e-commerce site or a site heavy on user-generated content such as a forum).

This particular setup, Jekyll on Github Pages, is most suited to people with a certain technical knowledge as there is no 
admin panel with visual editor and easy interface for settings (as opposed to a database-driven blogging platform like WordPress).

## Robots.txt and Humans.txt

These are two plain text files placed in the sites root, as the name suggests aimed at robots and humans, respectively.
 Robots.txt is the point of entry to a site for robots (also known as bots, crawlers, spiders or scrapers). It defines which parts of 
 a website may be crawled by these bots, with the possibility to specify pages or directories as well as different permissions 
 for different user agents (bots). This site was configured so that Google may crawl the entire site, but no other bots are allowed.
 
Humans.txt is a text file that specifies which people (humans) were involved in the creation of the site. Apart from the name(s), location
 and contact information of its creator(s) it may also contain information on the technology and tools used to create the site. 
 The one on this site contains name and contact information as well as technology and tools used and the standards it complies with.
 
## Comments

Comments on this project are served using Disqus, a free service which allows the user to paste in some code which will then render
 a comments section. 
 
## Open Graph

With more and more traffic coming to Web sites via social media and sharing, it is important to be able to control the information 
(such as description, title and image) displayed when a page is shared. Open Graph is a tool for this, allowing the site developer 
to add the preferred information using a set of meta tags. It was implemented here through adding it to the head section of 
the Jekyll templates, dynamically retrieving information based on the pages' specific parameters.
