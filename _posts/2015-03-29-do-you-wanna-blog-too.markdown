---
layout: post
title:  "Do you wanna technical blog too?"
date:   2015-03-29 20:00:20
categories: Common Beginners
comments: true
---

Look at [this interesting article](http://blog.vjeux.com/2011/analysis/start-a-technical-blog-its-worth-it.html), IMHO it's a good summary why you should consider to create your own blog.

So let me explain what you need to create a blog. Most of you are experienced engineers, so this post is not for you, but for beginners.

You can use existing platforms like [blogspot](http://blogspot.com) or [wordpress](http://wordpress.com).

I decided to go with simple static site and external systems for comments etc. So it can be placed on [GitHub Pages][pages-gh] or any hosting. I've used [Jekyll][jekyll] as the template processor with [Kasper theme][kasper]. A bit more themes are available [here](http://jekyllthemes.org/)

This blog is available in my [GitHub](https://github.com/sotnikdv/sotnikdv.github.io) repository, feel free to fork and change to start your own blog. 

**Don't forget to:**

- delete my posts from `_posts` directory
- change `_config.yml` (use `_config.yml.sample`)
- change `about.md` (use `about.md.sample`)
- change Disqus section in `_layouts/post.html` to your own block, line 52


### How to write posts

See instructions how to write posts and list of available plugins on [Writing Posts on Jekyll](http://jekyllrb.com/docs/posts/)

**Take a look** at the [Markdown Reference Manual](http://daringfireball.net/projects/markdown/syntax#link) which is a simple text markup language used in this blog. Also you may use simple [Markdown Cheatsheet](http://assemble.io/docs/Cheatsheet-Markdown.html)  

If you need more markup - I can recommend you [Textile](https://github.com/jekyll/jekyll-textile-converter) with this [beautiful manual](http://redcloth.org/textile)

### Local development and deploy to any server

To run local development and to deploy build result to any server you need [Jekyll][jekyll]. It's Ruby based, so you need Ruby 2.0 or later AFAIK. 

Then you have to install few gems (Linux example).
{% highlight bash %}
apt-get install ruby-dev libz-dev git
gem install jekyll
gem install bundler
gem install execjs
gem install therubyracer
{% endhighlight %}

So now you can create your own project from scratch by `jekyll new myblogfolder` or clone my with `git clone https://github.com/sotnikdv/sotnikdv.github.io`

To run build - use `jekyll build` inside a folder, if you want to ask Jekyll to stay in background and rebuild changes files automatically - use `jekyll build -w`. This is useful to view your changes immediately
{% highlight bash %}
sdv@sdv-dev:~/code/sotnikdv.github.io$ jekyll build -w
Configuration file: /home/sdv/code/sotnikdv.github.io/_config.yml
            Source: /home/sdv/code/sotnikdv.github.io
       Destination: /home/sdv/code/sotnikdv.github.io/_site
      Generating... 
                    done.
 Auto-regeneration: enabled for '/home/sdv/code/sotnikdv.github.io'
      Regenerating: 2 file(s) changed at 2015-03-29 01:49:01 ...done in 0.04097498 seconds.
      Regenerating: 2 file(s) changed at 2015-03-29 01:49:16 ...done in 0.058890892 seconds.
      Regenerating: 2 file(s) changed at 2015-03-29 01:51:35 ...done in 0.042440558 seconds.
      Regenerating: 1 file(s) changed at 2015-03-29 01:57:30 ...done in 0.066120995 seconds.
      Regenerating: 2 file(s) changed at 2015-03-29 01:57:35 ...done in 0.04388916 seconds.
{% endhighlight %}

To start local server, use `jekyll serve` inside a folder, server will be started by default on `http://127.0.0.1:4000/`

So now you can upload `_site` folder  content (after build) to any server.

### OMG! I wanna write posts and not scripts!

No worries, now let's talk about [GitHub Pages][pages-gh]. I've used [Jekyll Now README](https://github.com/barryclark/jekyll-now/blob/master/README.md) as a basis for this section.

#### Step 1) Fork my blog repository to your User Repository

Fork `github.com/sotnikdv/sotnikdv.github.io`, then rename the repository to [yourgithubusername].github.io.

Your blog will often be viewable immediately at <http://[yourgithubusername].github.io> (if it's not, you can often force it to build by completing step 2)

#### Step 2) Customize and view your site

Change your site name, description, avatar and many other options by editing the _config.yml file.

Making a change to _config.yml (or any file in your repository) will force GitHub Pages to rebuild your site with jekyll. Your rebuilt site will be viewable a few seconds later at <http://[yourgithubusername.github.io]> - if not, give it ten minutes as GitHub suggests and it'll appear soon

> There are 3 different ways that you can make changes to your blog's files:

> 1. Edit files within your new username.github.io repository in the browser at GitHub.com (shown below).
> 2. Use a third party GitHub content editor, like [Prose by Development Seed](http://prose.io). It's optimized for use with Jekyll making markdown editing, writing drafts, and uploading images really easy.
> 3. Clone down your repository and make updates locally, then push them to your GitHub repository.

#### Step 3) Publish your first blog post

Use any existing file in `/_posts/` as a template for your new post.

> You can add additional posts in the browser on GitHub.com too! Just hit the + icon in `/_posts/` to create new content. Just make sure to include the [front-matter](http://jekyllrb.com/docs/frontmatter/) block at the top of each new blog post and make sure the post's filename is in this format: year-month-day-title.md

[pages-gh]: http://pages.github.com
[jekyll]: http://jekyllrb.com
[kasper]: https://github.com/rosario/kasper
