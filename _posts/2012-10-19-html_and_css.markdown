---
layout: default
title: Rails Girls HTML and CSS Tutorial
permalink: html_and_css
---

# Rails Girls HTML and CSS Tutorial

*Created by [Piotr Szotkowski](http://chastell.net)*


## Step 0: Setting up

Get a computer with a browser and a text editor:

* browser: for best results use a recent version
of [Firefox](https://www.mozilla.org/firefox) or
[Chrome](https://www.google.com/chrome)

* editor: any **text** editor will do; use [Sublime
Text](http://www.sublimetext.com) if you don’t have a favourite


## Step 1: Content, or the brains

### Setup

Create a new directory (folder) and create a file named
`index.html` in it. Open that file in your editor and web browser.

**Coach:** Explain that browsers can open
local files, only the URL looks strange.

### HTML skeleton

Start by adding a general skeleton for your HTML
by writing the below into the `index.html` file:

{% highlight html %}
<!doctype html>
<html>
  <head>
  </head>
  <body>
  </body>
</html>
{% endhighlight %}

**Coach:** Explain the two main parts of HTML, `<head>` and `<body>`.

### Invisible head

Put the following lines between `<head>` and `</head>`:

{% highlight html %}
    <link rel='stylesheet' href='layout_and_style.css' />
    <meta charset='UTF-8' />
    <title>Rails Girls HTML and CSS Workshop</title>
{% endhighlight %}

**Coach:** Explain briefly `<title>`, `<meta>` and `<link>`.


### Header

Put the following lines between `<body>` and `</body>`:

{% highlight html %}
    <header>
      <h1>Rails Girls</h1>
      <ul>
        <li><a href='index.html'>welcome</a></li>
        <li><a href='events.html'>events</a></li>
        <li><a href='materials.html'>materials</a></li>
      </ul>
    </header>
{% endhighlight %}

Refresh the page in your browser: you should see
a plain, black-on-white (with blue links) list of items.

**Coach:** Explain the meaning of `<h1>`, `<ul>`, `<li>` and `<a>`.


### Side navigation

Put the following lines between `</header>` and `</body>`:

{% highlight html %}
    <nav>
      <h1>upcoming events</h1>
      <ul>
        <li>
          <a href='http://railsgirls.com/chengdu.html'>
            Chengdu, China
          </a>
        </li>
        <li>
          <a href='http://railsgirls.com/munich.html'>
            Munich, Germany
          </a>
        <li>
          <a href='http://railsgirls.com/turku.html'>
            Turku, Finland
          </a>
        </li>
        <li>
          <a href='http://railsgirls.com/zagreb.html'>
            Zagreb, Croatia
          </a>
        </li>
      </ul>
    </nav>
{% endhighlight %}

Refresh the page in your browser: you should see two lists now
that look quite similar, except the new links actually work.

**Coach:** Explain difference between
relative and absolute `href` attributes.


### Footer

Put the following lines between `</nav>` and `</body>`:

{% highlight html %}
    <footer>
      <p><a href='https://twitter.com/railsgirls'>follow us on Twitter</a></p>
      <p>get excited and make things!</p>
    </footer>
{% endhighlight %}

Refresh the page in your browser: two new lines should appear below the lists.



### Main content

Put the following lines between `</nav>` and `<footer>`:

{% highlight html %}
    <article>
      <h1>title</h1>
      <p>some content</p>
    </article>
    <article>
      <h1>title</h1>
      <p>some content</p>
    </article>
    <article>
      <h1>title</h1>
      <p>some content</p>
    </article>
{% endhighlight %}

Refresh the page in your browser: you
should see some content below the lists now.

**Coach:** Explain the header/nav/article/footer separation.


## Step 2: Layout, or the frame

### Getting the header and footer right

Now that we have all of the content of our page ready, let’s
move it around a bit. Create a `layout_and_style.css` file in
the same directory as `index.html` and open it in your editor.
Put the following lines in the `layout_and_style.css` file:

{% highlight css %}
header {
  text-align: center;
}

header ul {
  display: inline-block;
}

header li {
  float: left;
  margin: 1em;
}

footer {
  text-align: center;
}
{% endhighlight %}

Refresh your browser: your header and footer
should be centred and look differently now.

**Coach:** Explain the above CSS properties.


### Floating the navigation

Put the following lines in the CSS file:

{% highlight css %}
nav {
  float: right;
  width: 25%;
}

article {
  width: 70%;
}

footer {
  clear: both;
}
{% endhighlight %}

Refresh your browser: the navigation should be to the left now.

**Coach:** Explain the `float` and `clear` properties.


### Adjusting margins and padding

Put the following lines in the CSS file:

{% highlight css %}
body {
  margin: 0;
}

header h1 {
  margin: 0;
  padding-top: 1em;
}

header ul {
  padding: 0;
}

nav ul {
  padding: 0;
}

article, nav {
  margin: 1em;
}

footer {
  padding: 1em;
}
{% endhighlight %}

Refresh your browser: the positions of the elements should change slightly.

**Coach:** Explain margins and padding.


## Step 3: Style, or the looks

Now that we have the elements in roughtly the right places
comes the time to play with how things actually look.

### Fonts

Put the following lines in your CSS file:

{% highlight css %}
body {
  font-family: sans-serif;
}
{% endhighlight %}

Refresh your browser. Did the font change?

**Coach:** Explain fonts. Good luck.


### Colours

Put the following lines in your CSS file:

{% highlight css %}
a {
  color: inherit;
}

header {
  background-color: red;
  color: white;
}
nav li {
  color: red;
}

footer {
  background-color: silver;
}
{% endhighlight %}

Refresh your browser. Did the colours change?

**Coach:** Explain `color` and `background-color`.


### Finishing touches

Put the following lines in your CSS file:

{% highlight css %}
header a, nav a {
  text-decoration: none;
}

header li {
  list-style-type: none;
}

nav li {
  font-size: 1.5em;
  list-style-position: inside;
}

article, nav {
  border-top: 2px solid red;
}
{% endhighlight %}

Refresh your browser. Is it starting to look ok?

**Coach:** Explain what happened.


### Add some images

Download and save
[railsgirls.png](/examples/html_and_css/railsgirls.png)
and [railsgirls-logo.png](/examples/html_and_css/railsgirls-logo.png)
(warning: it’s white-on-transparent, so might be invisible
in your browser) in the same directory as your `index.html`
and `layout_and_style.css` files.

Open your `index.html` file and replace the
`<h1>Rails Girls</h1>` line with the below:

{% highlight html %}
      <h1><img src='railsgirls-logo.png' /></h1>
{% endhighlight %}

Open your `layout_and_style.css` file and add the below:

{% highlight css %}
nav li {
  list-style-image: url('railsgirls.png');
}
{% endhighlight %}

**Coach:** Explain images, list images and transparent backgrounds.



## What next?

* create more pages for your new site
* play with [colors](https://en.wikipedia.org/wiki/List_of_colors)
* play with [fonts](https://www.google.com/webfonts)
* add a [favicon](https://en.wikipedia.org/wiki/Favicon#How_to_use)
* add [Open Graph protocol](http://ogp.me)
