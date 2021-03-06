# MultiPost
MultiPost is a [Jekyll](https://github.com/mojombo/jekyll) plugin that enables the generation of multiple posts, each utilizing a different layout, from a single post (or page) entry.

## Installation
Simply download this repo and place the `multipost.rb` file in your `_plugins` directory.

## Usage
This plugin enables you to list more than one layout in the YAML front matter of your posts and pages.

```yaml
---
layout: [layout_a, layout_b]
title:  "My Awesome Post"
---
```

The post will then be rendered in each of the given layouts.

To ensure unique urls, each rendering of the post will have the name of the layout appended to it by default. For example:

- `/my-awesome-post/` becomes `/my-awesome-post/layout_a/`, or
- `/my-awesome-post.html` becomes `/my-awesome-post/layout_a.html`


However, you can customize this behavior by using a `:layout` variable in your permalink templates.

```yaml
---
layout: [layout_a, layout_b]
permalink: ":layout/:title/"
title:  "My Awesome Post"
---
```

## Why Would I Want This?
This is useful for any situation where you have a single content base that you wish to display in different views (e.g. prototyping designs, A/B testing, tailoring content presentation for different audiences).
