---
layout: post
---

## How to make a Tutorial Page
### 1. Make a copy of this page as a template
You will see that it starts with the following header
```
---
layout: post
---
```
This is the magic Jekyll part.  It grabs the HTML it needs to create the navigation bar at the top, the style sheets, etc from the `_layouts/post.html` file.


### 2. Write tutorial in Markdown
Markdown is a simple way of giving formatting to text.  Instead of having to write html like:
```
<html>
<head></head>
<h1>title</h1>
<p>This is html. it is <strong>ugly></strong><p>
</html>
```

you can simply write:
```
# Title
This is markdown. it is *not* ugly
```

You can read the [this link](https://help.github.com/articles/basic-writing-and-formatting-syntax/) for more formatting options.

### 3. save tutorial to `tutorials` folder

Even through you save it as a markdown document, it will be transformed to html

### 4. create a link in the `tutorials.html` page
1. open `tutorials.html`
2. add a line like the following (replacing (TITLE) with the name of your file)

```
<li><a href="./tutorials/TITLE.html">YOUR TUTORIAL</a> </li>
```

### 4. Render the site locally
Follow the instruction on the  readme for rendering the site locally to test out your page

### 5. Commit and push your changes
Once you push your changes, Github will automatically render the site live
