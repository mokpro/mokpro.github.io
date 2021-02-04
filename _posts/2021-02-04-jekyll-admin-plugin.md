---
title: Rich Text Editor via jekyll-admin
layout: post
date: '2021-02-04 00:30:00 -0600'
categories:
- tech
tags:
- jekyll
- text-editor
---

Being a developer, one can get accostomed to writing in markdown or using HTML tags. However, I feel that markdown is not needed when one has a rich text editor. Let's see how [jekyll-admin](https://github.com/jekyll/jekyll-admin) can help with that.

Below is a screenshot of Rich Text Editor I used to write this post

![jekyll admin rich text editor]({{ 'images/jekyll-admin.png' | relative_url }})

# Setup up jekyll-admin
This setup need not be commit to git, because this plugin is only needed for only for writing posts locally.

1. Install gem

```
$ bundle add jekyll-admin
```

2. Add plugin  to  `_config.yml`

```
plugins:
  - jekyll-admin
```

3. Run jekyll server and visit [localhost:4000/admin](http://localhost:4000/admin)

```
bundle exec jekyll serve
```

# Write a post

1. Write your post to your heart's content
2. Ensure that you add `layout` metadata field, otherwise blog page will not render correctly. Additionally, add `date`, `categories`, `tags` metadata fields as needed
3. Hit Save
4. Click on View to see the rendered blog post

![metadata fields]({{ 'images/metadata_fields.png' | relative_url }})




Now, go and write new posts!
