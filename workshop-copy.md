# Introduction to creating a blog with Jekyll
Created for #CodeNewbie's Codeland 2018 at Microsoft NYC.


# Static vs Dynamic Websites
Static websites are websites created using HTML/CSS and (optional) JS that do not have a database. Static sites appears the same for all visitors and generally have to be manually updated to display updated information. Whereas, dynamic websites have databases and can display different data for different users that can change dynamically or in real-time.

# Static vs Dynamic websites

Insert graphic visualizing the differences b/w static vs dynamic websites.

When should you use a static site?
  - Note static sites are generally faster because they don't have to make any database calls to display information.
When should you use a dyanmic website?

# Let's create a static site
In today's workshop we will be creating a functional static blog using Jekyll. Jekyll is a static site generator which allows us to create various HTML/CSS templates for different types of pages/content without having to re-write the HTML for every single page.

# What is Jekyll?
 "Jekyll is software that creates websites. Jekyll isn’t actually “running” the live website; rather, Jekyll is a “static site generator”: it helps you create the static site files, which you then host just as you would any other HTML website.” from  [https://programminghistorian.org/lessons/building-static-sites-with-jekyll-github-pages#what-are-static-sites-jekyll-etc--why-might-i-care-
](https://programminghistorian.org/lessons/building-static-sites-with-jekyll-github-pages#what-are-static-sites-jekyll-etc--why-might-i-care-
)

[insert link to Jekyll documentation if people want to learn more about Jekyll]


# Let's get started

# First let's install git

[ insert git set up instructions]
[check github version to confirm that it installed]

# let's clone a repo from GitHub

Cloning a repository means downloading code from GitHub.com onto your machine locally.

cd [to the folder/directory where you want to build blog]
Git clone [insert project url]


# next let's install Ruby on the command line

[check command to install ruby]

[check the ruby version to confirm install]

(inside of project directory) Brew install (double check command to install dependencies of the website)


# What have we done so far?

Installed dependencies to successfully run our Jekyll blog. Let's check to see if everyone successfully installed everything.

[insert command to run Jekyll locally]

	- Exercise: Successfully visit local version of our installed Jekyll website outside of the box.



# Let's look at the code


Open the files in your text editor!


# Jekyll Project Structure 1/4

  [Use jekyll project overview from Programming Historian]


	- Overview of Jekyll project structure

# Jekyll Project Structure 2/4
# Jekyll Project Structure 3/4
# Jekyll Project Structure 4/4


	- Overview of Markdown and YAML front matter
  	- How to edit posts in markdown

    [insert example image of markdown -- maybe have them go to an online markdown editor where they can see the markdown and rendering side by side]


# How to name files     

		- How to make posts as drafts vs published
How do permalinks work?
    - Change published date for an article    


# Let's create our first blog post

		- Exercise: Create first post and a draft post; load the local site in production mode and in draft mode to see how drafts behave differently.

    - Hint create a new file in the same directory as the current posts. Follow the naming conventions and edit as appropriaate.






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
