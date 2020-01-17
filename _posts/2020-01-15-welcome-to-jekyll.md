---
title: I built and hosted a Jekyll website in 15 hours so you don't have to!
date: 2020-01-15 21:17:00 -05:00
categories:
- blogging
- web
tags:
- git
- github
- jekyll
- web development
layout: post
---

Let me start off by saying that for those who are still learning web development, programming, or still feel like a fresh young new baby when it comes to the world of CS and web dev: It's okay to have 20 tabs open full of command cheatsheets and tutorials because you're often forgetful. It's okay to have those 20+ tabs take up the majority of your RAM and heat up whatever surface you're on. Don't listen to those pish posh people saying those bunches of open tabs out in the wild give them anxiety (I love you Insom, whatever your name is in real life). We are all still learning, and prone to mistakes and forgetfulness, so take pride in that, y'all. 

Hopefully whoever is reading this will never have to slave to the 15 hour-long addiction that is discovering how to put together a static website using Jekyll and Github pages (and nearly fail their Japanese quiz from neglecting to study). 

First things first, you'll want to download [a Git BASH client](https://git-scm.com/downloads) to use, because it's the hard way, or no way in this (the irony...). 

![codercat-34fa8c.png](/uploads/codercat-34fa8c.png)

Be sure you also have a Github pages initialized in your Github with the repository's title formatted as yourgithubusername.github.io. But don't initialize Github Pages just yet (with its markdown pages and other tricks and such)! Leave it as a repo with just a README.md and license for now (if necessary). That way there won't be any overwriting or clutter present when we initialize Jekyll to build the site's skeleton for us. 

Then, to save a lot of time, install [the Ruby DevKit Environment](https://rubyinstaller.org/downloads/) to manage and run functions with "Gems". Stick to the default settings during installation, run `ridk` at the last step of the installation wizard, download everything from 1 to 3 (includng the dev environment should take almost 1GB), and exit out. Make sure that the installation adds the PATH environment variables to run Ruby if you're on Windows. 

As soon as those are done, you'll want log onto git, login with your credentials with `git config` (link to git commands down below for reference), and `git clone` your github.io repository into whatever folder or workspace you prefer working on on your desktop. 

Now, using the Ruby dev environment we installed earlier, you're going to install the bundler package with `gem install bundler` and then `bundler install` after bundler is done installing. The bundler package is what's going to be building your website on a local server and committing all the changes to your blog live. Sounds scary, but neat!

![mmm.gif](/uploads/mmm.gif)

For installing necessary functions, you're going to have to run `gem install jekyll`, obviously the most important package we'll be using to build this baby. 

Finally, you can initialize your Jekyll blog by running `jekyll new .` in the remote repo that you cloned earlier, and there should now be at least the following files and directories which you can see by running the `ls` command (if you don't know how to already):

* `index.html`
* `_config.yml`
* `_layouts/`
* `_posts/`
* `_site/`
* `.gitignore`

Try writing something in `index.html`, which is the layout and essentially homepage of your blog. After that, push and commit your changes with `git add .`, `git push origin master`, and `git commit -m "your message here"` to publish to your repo. 

You will also want to configure your `_config.yml` file next since that will be the meat of how your blog is structured in Jekyll. For customizability's sake, I'll let you do the research on what plugins you want for your config file. But for reference, I will list a template of my `_config.yml` file and what I put (do not include brackets as indicated except for the exclude line): 

```
# Site settings
name: [Name of your website here]
title: null
description: [Something something]
url: [Not necessary unless you have a custom domain like me]
base-url: [/name.github.io]
relative_url: [same as your base-url]

# Social Media and Contact Info
twitter_username: nooduulz
github_username:  noodulz
email: jocelyndzuong@ufl.edu

# Build settings
timezone: America/New_York
markdown: kramdown
remote_theme: mattvh/solar-theme-jekyll
plugins:
  - jekyll-feed
  - jemoji
gems: [jekyll-paginate]
plugins: [jekyll-paginate]
permalink: /:year/:month/:day/:title/
paginate: 10
exclude: ['README.md', 'Gemfile.lock', 'Gemfile', 'Rakefile']
```

There should also be a Gemfile that allows for the Gem plugins to be enabled on your website. It should look something like this:
```
source "https://rubygems.org"
# Hello! This is where you manage which Jekyll version is used to run.
# When you want to use a different version, change it below, save the
# file and run `bundle install`. Run Jekyll with `bundle exec`, like so:
#
#     bundle exec jekyll serve
#
# This will help ensure the proper Jekyll version is running.
# Happy Jekylling!
# gem "jekyll", "~> 4.0.0"
gem "jekyll-paginate"
gem "jemoji"
# This is the default theme for new Jekyll sites. You may change this to anything you like.
# gem "minima", "~> 2.5"
# If you want to use GitHub Pages, remove the "gem "jekyll"" above and
# uncomment the line below. To upgrade, run `bundle update github-pages`.
# If you have any plugins, put them here!
group :jekyll_plugins do
  gem "jekyll-feed", "~> 0.12"
end

# Windows and JRuby does not include zoneinfo files, so bundle the tzinfo-data gem
# and associated library.
install_if -> { RUBY_PLATFORM =~ %r!mingw|mswin|java! } do
  gem "tzinfo", "~> 1.2"
  gem "tzinfo-data"
end

# Performance-booster for watching directories on Windows
gem "wdm", "~> 0.1.1", :install_if => Gem.win_platform?
```
Also, if your build didn't come with a `404.html` file to display when the user goes to a non-existent page on your website, you can either build that up in `.md` or `.html`. I have it in `.html` for reference as:
```
---
layout: default
permalink: /404.html
---

<style type="text/css" media="screen">
    .container {
        margin: 10px auto;
        max-width: 600px;
        text-align: center;
    }

    h1 {
        margin: 30px 0;
        font-size: 4em;
        line-height: 1;
        letter-spacing: -1px;
    }
</style>

<div class="container">
    <h1><b>4OWO4</b></h1>

    <p><strong>Page not found</strong></p>
    <p>The requested page could not be found. Womp Womp Womp...</p>
</div>
```
You can use this as reference in building one in `.html` if you don't have it already.

Finally, you can stage the files (`git add .`), push, and commit the changes to your repo! Be sure to do this before doing the next step. We're almost done!

Now, run `bundle exec jekyll serve --watch` (I believe that's how you force run the server should there be errors?) and it should run smoothly and show you that you can `ctrl + c` to stop the server from building the site (**do not do this yet!**).

Now the drawback of this is that git and generators like jekyll take quite some time to fully commit all the changes to your website. So it may take at most 10 minutes to see the difference and finished product. But keep refreshing your github.io page and eventually there should be a blank page with some text from your index.html file. 

From here on out, you can implement a [custom Jekyll theme](http://jekyllthemes.org) you prefer (which is what I did due to its ease). Be sure to replace any files in your repo as needed with the theme files and directories to fully implement the theme! 

To start adding additional pages, you can add a `.md` file with the page name in the home directory of the repo. Then edit the default.html or whatever layout file for your chosen theme and add an additional list at where the other pages are in `<li></li>` brackets or something like that, and link it to the `.md` file you made (i.e. yourname.github.io/something.md). Here's an outline of what a `.md` page should include before putting any content:
```
---
YAML front matter
layout: default
title: About
permalink: /about
---
blah blah blah your content here
```

And we're done! I think? Let me know or contact me if I'm missing anything or if a step went wrong. I'm open to criticisms left and right.

![happysolar-2285cd.gif](/uploads/happysolar-2285cd.gif)

I'd like to thank these sources for being truly resourceful and wholesomely time consuming in putting this site together: 
* [Smashing Magazine's Jekyll and Github Pages Blog Guide](https://www.smashingmagazine.com/2014/08/build-blog-jekyll-github-pages/)
* [Michelle Fullwood's Guide to Setting up a Jekyll Blog](https://michelleful.github.io/code-blog//2014/02/28/setting-up-a-jekyll-blog-on-github-pages/)
* [24 Ways to Get Started with Github Pages](https://24ways.org/2013/get-started-with-github-pages/)
* [GitLab's Start Using Git](https://docs.gitlab.com/ee/gitlab-basics/start-using-git.html)
* [Jekyll Documentation](https://jekyllrb.com/docs/)

You can refer to the documentation should there be any minor build errors. Good luck and have fun! Hope this saved you a chunk of time as I tried to make this as concise and simplistically short. If not, I'll be sure to improve in my clarity in the next post!

_Update: As per request, I've elaborated a little further on how to set up the Ruby DevKit Environment to run gem functions during build. Also fixed formatting in the code examples and demonstration._
