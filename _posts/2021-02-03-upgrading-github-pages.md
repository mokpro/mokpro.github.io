---
title: Upgrading Github Pages Site
layout: post
date: '2021-02-03 11:40:19 -0600'
categories:
- tech
tags:
- jekyll
- github-pages
---

On a whim, I created [this website](https://pranav.moktali.io) over 4 years ago.  I'm glad I did create it. In last 5 years, I've learnt so much on Ruby, Rails, JavaScript, Golang. I want to share what I have learnt. One might think that - how nice, Pranav's sharing. But this is for my own sake. The more I write, the more I can recollect and formalize the knowladge.

So, here it is, the first article after a long time! 

# A long time ago, not too far away ...

I built [this website](https://pranav.moktali.io) on github pages. You can build one too, it's pretty easy, follow [Github Pages](https://pages.github.com/). But it was outdated with dependency vulnerabilities (see below). So I started to upgrade it.

So, here it is, the first article after a long time! 

# How to upgrade github pages?

1. Clone [existing repo](https://github.com/mokpro/mokpro.github.io) on terminal 

    ```bash
    $ git clone git@github.com:mokpro/mokpro.github.io.git
    ```

1. Follow the [Jekyll Instructions](https://jekyllrb.com/docs/#instructions) to create a new blog
  
    - Install the jekyll and bundler gems
    
        ```bash
        $ gem install jekyll bundler
        ```
  
    - Create a new Jekyll site at `./mokpro.github.io`
    
        ```bash
        # `--force` to ensure outdated files are overwritten
        $ jekyll new mokpro.github.io --force

        ```
 
1. Review all the diffs

    ```bash
    $ git status
    
    Changes to be committed:
    (use "git restore --staged <file>..." to unstage)
      modified:   .gitignore
      new file:   404.html
      modified:   Gemfile
      modified:   Gemfile.lock
      modified:   _config.yml
      modified:   about.md
      deleted:    index.html
    ```

1. Commit changes and push to a new branch

    ```bash
    $ git commit -m 'upgrade jekyll'
    $ git push origin HEAD
    ```

1. Create a pull request and merge it [#6](https://github.com/mokpro/mokpro.github.io/pull/6), it's done!
