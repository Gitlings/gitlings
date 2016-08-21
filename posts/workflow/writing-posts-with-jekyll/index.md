---
layout: post
title: "Writing posts with Jekyll"
date: 2016-08-20 10:28:00 +3000
author: mvlabat
categories: [mainpage, workflow]
---

Hi everyone! In this post I'll tell you about writing posts for our site. :)

{: .center }
![image](jekyll-logo.png "Jekyll logo")

<!--more-->

## Requirements
* [Git][installing-git] (check the instructions for your OS)
* [Ruby][installing-ruby] (this step is required only for UNIX)
* [Jekyll][installing-jekyll] (this step is required only for Windows)

## Running Jekyll and checking our site
After you successfully install all the requirements, we'll have to clone the repository of our site.
This is where all its posts and resources are stored. Our site (like everything else) is hosted on github, so run the following command:
{% highlight bash %}
git clone git@github.com:Gitlings/gitlings.github.io.git
{% endhighlight %}

After that we have to run a few commands in order to setup the requirements specifically for the site:
{% highlight bash %}
cd gitlings.github.io
bundle install
{% endhighlight %}

The previous two steps are needed to be proceeded only once.

So finally we can view it! Just run the following command and go to `127.0.0.1:4000` in your browser:
{% highlight bash %}
jekyll serve
# I myself can't run Jekyll with this command,
# I have to use `bundle exec jekyll serve`.
# Try it, if just `jekyll serve` fails for you too.
{% endhighlight %}

## Writing your brand new awesome post

### About site structure
All our posts are parts of our projects. Projects are the essential part of our activity: every topic we study is a separate project.

All the posts are contained inside `posts/` folder. Here is a `post/workflow/` folder, which contains everything about our workflow: this post itself, guides about working with git and so on. All the other folders have the same names as our projects.

Each directory contains `index.md` - file defining contents of its relative path. For example `posts/workflow/index.md` is responsible for showing every post under `workflow` category, this page will be accessible via `gitlings.github.io/post/workflow/` path.

Each post should be placed into a separate folder inside a category directory. Post folders also have to contain `index.md` and all the resources (usually images) used in it.

### Writing a post
You can use this post as a template, it's located at `posts/workflow/writing-posts-with-jekyll/index.md`.

So let's assume you've created a file. Every page has a header, telling Jekyll about itself.
{% highlight kramdown %}
---
layout: post                        <!-- For posts you should always use this layout. -->
title: "Writing posts with Jekyll"  <!-- Title of your post. -->
date: 2016-08-20 10:28:00 +3000     <!-- All the posts appearing on the site are sorted by date. Don't use dates from future, otherwise your post won't appear on categories pages. -->
author: mvlabat                     <!-- This should be your nickname on github. -->
categories: [mainpage, workflow]    <!-- Array of the categories (projects) the post is related to. "mainpage" means that your post will be shown as a recent post on the main page. -->
---
{% endhighlight %}

Insert it inside your file and make sure to remove the comments and fill the fields with your data.

Then you can write about everything you're up to. :) Make sure to check markdown/kramdown/jekyll guides, you're welcome to suggest everything we can add in this post or make a [github contribution][git-workflow] by yourself.

Cheers!

[installing-git]: https://git-scm.com/book/en/v2/Getting-Started-Installing-Git
[installing-ruby]: https://www.ruby-lang.org/en/documentation/installation
[installing-jekyll]: https://jekyllrb.com/docs/windows/
[git-workflow]: /posts/workflow/git-workflow

