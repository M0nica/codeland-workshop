footer: © Monica Powell, 2018 | twitter: @waterproofheart | web: www.aboutmonica.com
slidenumbers: true


<!-- ![](/Users/monica/Downloads/pexels-photo-257897.jpeg) -->
# Getting Started with Jekyll

### Workshop at Codeland 2018 by Monica Powell

——-

#Hello!

## Monica Powell
Who am I?

## Mia Murrell (TA)
Who is she?

---
# Static vs Dynamic websites

Static websites unlike dynamic websites:
 - Never have databases
 - Display the same information for all readers
 - Less expensive to host
 - Load faster
 - Less prone to hacking
 - Usually don’t have CMS

——

# Today we will be building a static blog using Jekyll

—



# Introduction to Jekyll

Jekyll is static site generator.

—-

# Introduction to Jekyll

A “Jekyll website” is a “static (plain HTML) website that has been created using Jekyll. Jekyll is software that creates websites. Jekyll isn’t actually “running” the live website; rather, Jekyll is a “static site generator”: it helps you create the static site files, which you then host just as you would any other HTML website.” [^1]

[^1]: [Programming Historian](https://programminghistorian.org/lessons/building-static-sites-with-jekyll-github-pages#what-are-static-sites-jekyll-etc--why-might-i-care-)

——


# Examples of websites powered by Jekyll


Ruby documentation https://www.ruby-lang.org/en/


Bootstrap documentation https://getbootstrap.com/



Blog/Personal Website
https://zachholman.com/


www.datalogues.com


https://www.chenhuijing.com/#%F0%9F%8E%AE

—

# [fit] Installation Fest

—-
# Pairing up

Please pair up in groups of 3!

We will be installing Git and Jekyll.


—-

# Installation

[Install git](https://git-scm.com/downloads): [https://git-scm.com/downloads](https://git-scm.com/downloads)


![inline](/Users/monica/Dev/dactl/assets/slide-assets/install-git.png)

——-

# install?

`$ git config --global user.name "John Doe"
$ git config --global user.email johndoe@example.com```

—

# create a share_page.html in the _includes folder

``` html
<div class="share-page">
<h3>Share "{{ page.title }}":</h3>
	<ul class="icons">
 		…
	</ul>
</div>
```


——-


# create a share_page.html in the _includes folder

```html


<ul class="icons">

  <li><a href="https://twitter.com/intent/tweet?text={{ page.title }}&url={{ site.url }}{{ page.url }}&via={{ site.twitter_username }}&related={{ site.twitter_username }}" rel="nofollow" target="_blank" title="Share on Twitter"" class="icon alt fa-twitter"><span class="label">Twitter</span></a></li>

</li>




```


——-



# create a share_page.html in the _includes folder

```


<ul class="icons">

  <li><a href="https://twitter.com/intent/tweet?text={{ page.title }}&url={{ site.url }}{{ page.url }}&via={{ site.twitter_username }}&related={{ site.twitter_username }}" rel="nofollow" target="_blank" title="Share on Twitter"" class="icon alt fa-twitter"><span class="label">Twitter</span></a></li>

</li>
  <li><a href="https://facebook.com/sharer.php?u={{ site.url }}{{ page.url }}" rel="nofollow" target="_blank" title="Share on Facebook" class="icon alt fa-facebook"><span class="label">Facebook</span></a></li>
  <li><a href="https://www.linkedin.com/shareArticle?mini=true&url={{ site.url }}{{ site.baseurl }}{{ page.url }}&title={{ page.title }}&summary={{ page.description }}&source={{ site.title }}"
onclick="window.open(this.href, 'pop-up', 'left=20,top=20,width=500,height=500,toolbar=1,resizable=0'); return false;"
title="Share on LinkedIn" class="icon alt fa-linkedin"><span class="label">LinkedIn</span></a></li>



```


——-



Goal: Successfully install Jekyll and confirm by viewing Jekyll site on local server.

Open terminal (or windows equivalent)

Install dependencies
Mac
Command line tools/xcode
Homebrew
Ruby and rubygems
Node
Windows
Include instructions that are specific to windows users
Unix


All: Install Jekyll on the command line


Go over installation/brief intro to GitHub if necessary.

Login to github on computer and on terminal
(include instructions to login to github)

Clone this repository: https://github.com/M0nica/dactl
I think students should use this Jekyll theme named DACTL  for the workshop
I like that cloning DACTL theme is not gem based as it gives access to all of the style files in the same place as the content files which should make it easier for students to update and explore.
Installation
Running locally
Assuming you've got Jekyll installed, clone or download this repo, cd to wherever you've put dactl folder and run jekyll -s'
Hosting on GitHub
Fork this repo and rename it to yourusername.github.io... and that's it!
Your new dactl-themed Jekyll blog should be up and running at yourusername.github.io.
In my version of the DACTL repository I want to add some images in case they don’t want to look for them and maybe adding a welcome post! With peritent workshop information. (but also have that info avail someplace else -- maybe have it in the README and in a POST and ask them to not delete both until the workshop is over -- or they can turn it into a draft or reference my original repo which they forked from )


Clone by typing git clone https://github.com/USERNAME/dactl.git (replace with your username)
 cd dactl
 jekyll -s  (run bundle install if your jekyll is out-of-date it should prompt you)



Now let’s look at the files in our text editor by opening the folder with Jekyll project in text editor

File structure should look like this:



~/my-awesome-site $ bundle exec jekyll serve
# => Now browse to http://127.0.0.1:4000/dactl// (or whatever URL your terminal provides)
Exercise: Successfully visit local version of our installed Jekyll website outside of the box by typing bundle exec jekyll serve --watch. Click through the local website to see how it mirrors local files.



Success! (this should appear on local 4000 or lime version if it’s cloned from my version!)


3 - Overview of Jekyll project structure
Goal: Understand where various parts of a Jekyll a site live so that everyone is comfortable with project structure before we begin updating the content

We will primarily be editing .md (markdown) files that Jekyll converts into HTML for the final site. Note that any files placed in the _site folder will be deleted/overridden when the website is generated. Therefore make sure you are placing your files in the correct folder.



_config.yml - set sitewide variables (commonly used to stash site’s contact information as it will be referenced in multiple places throughout the site) that do not change often
	# Site settings
# These are used to personalize your new site. If you look in the HTML files,
# you will see them accessed via {{ site.title }}, {{ site.email }}, and so on.
# You can create any custom variable you would like, and they will be accessible
# in the templates via {{ site.myvariable }}.
	TODO - discuss custom data variables that change often and that they should go in data files instead of in the config




“Changes made to _config.yml will not be watched by jekyll serve. You must restart and reserve Jekyll after any config changes.
All indentation is mandatory and must be made with two spaces, or else the file will not work.” source: https://www.taniarascia.com/make-a-static-website-with-jekyll/
Activity: make a change to the config file to a username, title or other section they feel comfortable editing. Then stop and restart the server to see the changes they made appear.

Code should by DRY (Don’t Repeat Yourself)
Templating language allows you to repeat code on various pages of a website without having to write the code multiple times.

Jekyll Templating using the Liquid templating language
Resources:
https://jekyllrb.com/docs/templates/
https://shopify.github.io/liquid/

Ask/check-in: Who is familar with markdown? (and be prepared based on pulse of the room)

Overview of Markdown and YAML front matter
YAML allows you to include metadata -- data associate with each post that can be used for SEO and to display for users
Permalinks - how do permalinks work?
Markdown is a markup language like HTML but xxxx.
“The stuff between the -– dashes is called “front matter” (note that opening the file in a Markdown editor might make the front matter appear on a gray background instead of between dashes). The front matter tells your site whether to format the content below the front matter as a page or blog post, the title of the post, the date and time the post should show it was published, and any categories you’d like the post or page listed under.” from https://programminghistorian.org/lessons/building-static-sites-with-jekyll-github-pages


Markdown

# Title same as <h1>Title </h1>


https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet


4 - Edit the default markdown post and then create a new post with markdown

Goal: Create first post and a draft post; load the local site in production mode and in draft mode to understand how drafts behave differently.
Edit existing markdown post
Create a new file -- write in markdown with YAML at the top and then properly name and save the post
Confirm that this works by reloading page of live server
Create a draft post
Try to run local server with and without the draft being viewable


Activity: write a post about something(s) you’ve learned or enjoyed  at Codeland so far!

5 - Change the color of the header from green to anything else!

Theme colors are set in variables in a JS file for this theme and will need to be updated in the theme.js folder with the js (I also want to show them how to edit the scss files directly) :

6 - Adding images

Edit about page and add a photo of yourself (or a placeholder)
Who are you? How long have you been coding? What brought you to codeland?



Replace the brain in the top of the site with a different svg (provide resource for finding an svg -- or maybe just add one to the github file already)

SVG should be added to assets/img folder and then the dactl.svg should be replaced with the name of their image. It doesn’t have to be an svg but should be small. (Although should explain the benefits of using an svg vs. a pixelized image) maybe by showing them how an svg looks in a text editor:

# Layout configuration
  logo_path                  : "assets/img/dactl.svg" # path to logo file


Resources for stock photos:
https://www.flickr.com/photos/wocintechchat/ (require attribution to #WOCinTech)
https://unsplash.com/
https://www.pexels.com/

We will be editing a random post to add an image

TODO - add instructions for hotlinking (how the theme demo is set up NOT a best practice) -- just paste in the direct URL to image
Better option -- add the image to the assets folder and link relationally to the folder in the URL that references images in the front matter  
Exercise: Add multiple images to blog -- to about page, icon in menu and header image for posts
7 - Adding metatags (updating content in one place which is inherited by other pages)
Editing <head> and adding og meta tags for SEO optimization and to preview properly when social sharing (on Slack, Facebook, Twitter etc.)
Exercise: confirm that OG metatags were updated successfully by checking Facebook’s URL debugger: https://developers.facebook.com/tools/debug/sharing/
8 - Using partials to add social sharing icons to each post
Let’s customize how our posts appear with partials with the liquid templating language
Exercises: Add social icons to each post so that we can share our posts on Twitter/Facebook!!


-- create a share_page.html in the _includes folder

<div class="share-page">
<h3>Share "{{ page.title }}":</h3>


<ul class="icons">
  <li><a href="https://twitter.com/intent/tweet?text={{ page.title }}&url={{ site.url }}{{ page.url }}&via={{ site.twitter_username }}&related={{ site.twitter_username }}" rel="nofollow" target="_blank" title="Share on Twitter"" class="icon alt fa-twitter"><span class="label">Twitter</span></a></li>
  <li><a href="https://facebook.com/sharer.php?u={{ site.url }}{{ page.url }}" rel="nofollow" target="_blank" title="Share on Facebook" class="icon alt fa-facebook"><span class="label">Facebook</span></a></li>
  <li><a href="https://www.linkedin.com/shareArticle?mini=true&url={{ site.url }}{{ site.baseurl }}{{ page.url }}&title={{ page.title }}&summary={{ page.description }}&source={{ site.title }}"
onclick="window.open(this.href, 'pop-up', 'left=20,top=20,width=500,height=500,toolbar=1,resizable=0'); return false;"
title="Share on LinkedIn" class="icon alt fa-linkedin"><span class="label">LinkedIn</span></a></li>
</ul>

</div>

Then in the _layouts folder’s post.html add “    {% include share-page.html %}” in the file where the share icons should appear
Add additional CSS if necessary (need to see what the icons look like w/ the current CSS styles applied -- it may be fine if not then will need to add css that is specific to the icons in this section of the site)


9 - Add multiple authors to site with data files
Add multiple authors ( data files) and display their name and social handles with their articles  (http://www.datalogues.com/adding-author-bios-in-jekyll)
1) Edit/create appropriate folders and files in Jekyll project
front matter of individual blog posts where author should be included
_layouts/post.html
and created the following folders/files:
_data/authors.yml
_includes/author_bio.html
2) Store Author Data
I have stored my author data in a folder called _data that contains a file authors.yml. The author information associated with monica_powell is pulled into my post from the authors.yml data file.
monica_powell:
    name: Monica Powell
    email: monica@aboutmonica.com
    twitter: http://twitter.com/waterproofheart
    bio: Monica Powell is a web technologist that cares about increasing the visiblity of underestimated individuals in technology. In 2015, she received the &#35;GIRLBOSS award from Sophia Amoruso’s Girl Boss Foundation. She’s currently focusing on making tech more enjoyable & accessible and is always up to chat data visualizations, web development or &#35;BlackGirlMagic.
    image: http://www.datalogues.com/assets/images/monica-powell-headshot.jpg


3) Reference relevant authors in the front matter of individual blog posts
In the front matter of each blog post in Jekyll you should reference authors in YAML (YAML Ain’t Markup Language) using the following format author: NAME OF AUTHOR. The name of author should be an exact match one of the variables in your authors.yml
The front matter in Jekyll sets the metadata for a post and is key to properly building posts. YAML is a human friendly data serialization standard for all programming languages.
Here is an example of the front matter for this particular post.
layout: post
title: How to Add Author Bio in Jekyll
description: A guide to adding author bios in Jekyll
image: assets/images/author-bio.png
permalink: adding-author-bios-in-jekyll
author: monica_powell
comments: true


4) Define HTML for author bio
in the folder _includes create a file called author_bio.html to define the HTML for how author bio’s should be displayed


<hr>


<span>


  <div>


     # include author image if there is an author image


     {% if author.image %}


        <img src="{{author.image}}" class="author-img">


     {% endif %}


     <div>


        <h3> {{author.name}} &nbsp;


           # include link to author's twitter if they have provided a twitter account


          {% if author.twitter %}


             <a href="{{author.twitter}}" class="icon fa-twitter"><span class="label">Twitter</span></a>


           {% endif %}


         </h3>


     </div>


  </div>


  {{ author.bio }}


</span>


<br>
view rawauthor_bio.html hosted with ❤ by GitHub
5) Add author bios to the post layout
Add a line in post.html where author bio should appear and pull in the HTML as defined above in author_bio.html. The logic is set so that it will only call that HTML template if there is author information associated with this particular post.
 ## if there is an author bio

  {% if author.bio %}
      {% include author_bio.html %}
  {% endif %}






9 . Deploy to GitHub
Deploy to GitHub pages (may want to do this earlier or throughout workshop)

Exercise: Publish the site on github pages!


Fork this repo and rename it to yourusername.github.io... and that's it!
Your new dactl-themed Jekyll blog should be up and running at yourusername.github.io.
(also included this up higher - depending on where we want this step to go in the lesson plan)



---

# Footnotes

Manage your footnotes[^12] directly where you need them. Alongside numbers, you can also use text references[^Sample Footnote].

Include footnotes by inserting`[^Your Footnote]` within the text. The accompanying reference can appear anywhere in the document:

`[^Your Footnote]: Full reference here`

[^2]: This is the first footnote reference

[^Sample Footnote]: This is the second footnote reference

---

# Footnotes

Footnote references need to be *unique in the markdown file*. This means, that you can also reference footnotes from any slide, no matter where they are defined.

When there are multiple references are listed, they must all be separated by blanks lines.

---


# Nested Lists

- You can create nested lists
    1. by indenting
    1. each item with
    1. 4 spaces
- It’s that simple

---

# Links

Create links to any external resource—like [a website](http://www.decksetapp.com)—by wrapping link text in square brackets, followed immediately by a set of regular parentheses containing the URL where you want the link to point:

`‘[a website](http://www.decksetapp.com)’`

Your links will be clickable in exported PDFs as well!

---

# Display formulas

Easily include mathematical formulas by enclosing TeX commands in `$$` delimiters. Deckset uses [MathJax](http://www.mathjax.org/) to translate TeX commands into beautiful vector graphics.

<a name="formulas"></a>

---

## Schrödinger equation

The simplest way to write the time-independent Schrödinger equation is $$H\psi = E\psi$$, however, with the Hamiltonian operator expanded it becomes:

$$
-\frac{\hbar^2}{2m} \frac{d^2 \psi}{dx^2} + V\psi = E\psi
$$

---

# Captioned Images and Videos

![inline](room.jpg)

Easily create captions using [inline] images/videos with text underneath.

---

# Plus:

- PDF export for printed handouts
- Speaker notes and rehearsal mode
- Switch theme and ratio on the fly
- Animated GIFs for cheap wins and LOLs :-)
