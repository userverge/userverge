# userverge
# Creating a New Article
Want to help contribute to the Help Center? Write or update an article!

## 🛡️ Requirements 
 - The communication must be clear and well explained for the user to understand
 - Fact check and make sure the information you're providing is accurate
 - Good grammar
 - Valid syntax
 - Proper metadata
 - Valid links and up to date

## ✍️ Creating an Article
By following the file structure, create a `.md` file under the correct category. As an example, if you were to create an article that explains on how to do something in Python, the file would be created like `_posts/python/2021-09-12-title-of-article.md`. You're required to add the date at the beginning of the file name, `YYYY-DD-MM`. These dates are used to show when the article was last updated, to allow users to know if the article is up to date.

 Then start writing the article in [Markdown](https://www.markdownguide.org/getting-started/). Writing in Markdown is very easy to do, if you need help understanding how to do certain task like creating a link, inserting an image, creating a list look [here](https://guides.github.com/features/mastering-markdown/).

## 📃️ Metadata
Make sure the metadata is setup properly, this is usually at the top of every article.
It should look like this:
```
---
layout: post
title:  "Title of Article"
categories: ReactNative
permalink: /reactnative/ios/headerBlurEffect​/
---
```

## Author
For author, just replace `octocat` with your GitHub username.
```
<div class="authors">
    <p>Author: <a href="#" target="_blank">{% avatar Octocat %} Octocat</a></p>
</div>
```
Make this is placed at the between the metadata and article.

The `{% avatar Octocat %}` variable will grab your GitHub avatar to use as your profile picture on userverge, thanks to the [jekyll-avatar](https://github.com/jekyll/jekyll-avatar/) plugin.


## 📢️ Publishing
Create a pull request on this repo and title it like this "New Post: Name of Article" or if you're editing an article to maybe improve or fix a typo, title it like "Edit: Name of Existing Article".

# Building
If you're interested in learning on how to build userverge locally, maybe to preview that your article does show up properly, just follow the instructions below.

Since userverge is powered by Jekyll, you'll need to install [Ruby](https://www.ruby-lang.org/en/) for your operating system.
 - [Download for Windows](https://rubyinstaller.org/)
 - [Download for macOS](https://www.ruby-lang.org/en/downloads/)

### Installing Ruby on Linux
Debian/Ubuntu:
```
sudo apt-get install ruby-full build-essential zlib1g-dev
gem install jekyll bundler
bundle install
```
Fedora/RedHat:
```
sudo dnf install make automake gcc gcc-c++ kernel-devel ruby-devel
gem install jekyll bundler
bundle install
```

## Building and Locally Hosting

To run a localhost server, run:
```
bundle exec jekyll serve
```

After using `bundle exec jekyll serve`, try going to http://localhost:4000/ in your preferred web browser.

If you're unable to get Ruby installed or the serve command working, you can always resort to building it on other platforms like GitHub Pages, Cloudflare Pages, or Netlify.
