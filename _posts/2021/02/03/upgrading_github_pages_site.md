# Upgrading Github Pages Site

On a whim, I created this website over 4 years ago.  I'm glad I did create it. In last 5 years, I've learnt so much on Ruby, Rails, JavaScript, Golang. I want to share what I have learnt. One might think that - how nice, Pranav's sharing. But this is for my own sake. The more I write, the more I can recollect and formalize the knowladge.


So, here it is, the first article after a long time! 

## Long time ago, not too far away ...

I built [this website](https://pranav.moktali.io) on github pages. You can build one too, it's pretty easy, follow [pages.github.com/](https://pages.github.com/).
But it was outdated with dependency vulnerabilities (see below). So I started to upgrade it.

<PICTURE HERE>

## How to upgrade github pages?

1. Clone [existing repo](https://github.com/mokpro/mokpro.github.io) on terminal 

  ```bash
  $ git clone git@github.com:mokpro/mokpro.github.io.git
  ```

1. Follow the [Jakyll Instructions](https://jekyllrb.com/docs/#instructions) to create a new blog
  a. Install the jekyll and bundler gems
  
    ```bash
    $ gem install jekyll bundler

    ```
  
  b. Create a new Jekyll site at `./mokpro.github.io` (`--force` to ensure outdated files are overwritten)
  
    ```bash
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
$ git commit -m 'upgrade jakyll'
$ git push origin HEAD
```

1. Create a pull request and merge it, it's done!


