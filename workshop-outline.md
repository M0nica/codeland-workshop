# Introduction to creating a blog with Jekyll 
Created for #CodeNewbie's Codeland 2018 at Microsoft NYC. 

## Lesson Plan Outline 

- Introduction 
	-  As an introduction I want to discuss the differences between a static website and a dynamic website so that students have a basic understanding how how a static site generator like Jekyll works.

	- I will likely reference the following:
“Jekyll is software that helps you “generate” or create a static website (you may see Jekyll described as a “static site generator”). Jekyll takes page templates—those things like main menus and footers that you’d like shared across all the web pages on your site, where manually writing the HTML to include them on every webpage would be time-consuming. These templates are combined with other files with specific information (e.g. a file for each blog post on the site) to generate full HTML pages for website visitors to see. Jekyll doesn’t need to do anything like querying a database and creating a new HTML page (or filling in a partial one) when you visit a webpage; it’s already got the HTML pages fully formed, and it just updates them when/if they ever change.

	- Note that when someone refers to a “Jekyll website”, they really mean a static (plain HTML) website that has been created using Jekyll. Jekyll is software that creates websites. Jekyll isn’t actually “running” the live website; rather, Jekyll is a “static site generator”: it helps you create the static site files, which you then host just as you would any other HTML website.” from  [https://programminghistorian.org/lessons/building-static-sites-with-jekyll-github-pages#what-are-static-sites-jekyll-etc--why-might-i-care-
](https://programminghistorian.org/lessons/building-static-sites-with-jekyll-github-pages#what-are-static-sites-jekyll-etc--why-might-i-care-
)
 
- What are static websites?
	- Basic types of files in a website
 	- Static website vs dynamic web
		- Pros and cons
		- Different use cases
- Let’s get started with Jekyll 
	- Brief history of Jekyll  
	- Clone a project repo with sample Jekyll project installed for this workshop
		- Go over installation/brief intro to GitHub if necessary. 
- Install Jekyll on command line 
	- Install Ruby
	- Install Jekyll
	- Exercise: Successfully visit local version of our installed Jekyll website outside of the box.
- Now let’s look at the files in our text editor 
	- Overview of Jekyll project structure 
	- Overview of Markdown and YAML front matter 
		- How to edit posts in markdown
		- How to make posts as drafts vs published
How do permalinks work?
		- Exercise: Create first post and a draft post; load the local site in production mode and in draft mode to see how drafts behave differently.
	- Adding images 
		- Exercise: Add an image to blog
	- Adding metatags
   		- Editing <head> and adding og meta tags for SEO optimization and to preview properly when social sharing (on Slack, Facebook, Twitter etc.)
		- Exercise: confirm that OG metatags were updated successfully by checking Facebook’s URL debugger: [https://developers.facebook.com/tools/debug/sharing/]( https://developers.facebook.com/tools/debug/sharing/)
- Let’s customize how our posts appear with partials with the liquid templating language
- Exercises: 
	- Add social icons to each post 
	- Add multiple authors ( data files) and display their name and social handles with their articles  (http://www.datalogues.com/adding-author-bios-in-jekyll)
- Deploy to GitHub pages (may want to do this earlier or throughout workshop)
- Exercise:
	- Publish the site on github pages!





