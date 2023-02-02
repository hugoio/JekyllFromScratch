---
layout: base
title: index
---

## My Jekyll Guide

## Table of content

- [Jekyll from scratch](#1)
	- [Quickstart](#1a)
	- [Index page and base layout](#1b)
- [CLI commands](#2)
	- [Jekyll](#2a)
	- [Bundle](#2b)

### <a name="1"></a>Jekyll from scratch

#### <a name="1a"></a>Quickstart

This post assume you previously installed ruby and Jekyll on your machine.

1. Initialize a new site:

	>> ```bash
	>> mkdir newP;
	>> cd newP;
	>> bundle init;
	>> echo "gem \"jekyll\"" >> Gemfile;
	>> bundle;
	>> ```

	You can prefix all jekyll commands listed in this tutorial with ```bundle exec```, to use the project configuration.

	You can run the jekyll local web server with ```jekyll serve```, options:

	* ```--livereload```: force the browser to refresh with every change

	* ```--host``` and ```--port```

	You can build the site with ```jekyll build```.

	This post assume you run the local web server will developing with the following command:

2. Run the local web server:

	>> ```bash
	>> bundle exec jekyll serve --livereload;
	>> ```

#### <a name="1b"></a>Index page and base layout

1. Write a file named `index.html` with the following code:

	>> ```html
	>> <!DOCTYPE html>
	>> <html>
	>>   <head>
	>>     <meta charset="utf-8">
	>>     <title>Home</title>
	>>   </head>
	>>   <body>
	>>     <h1>Hello World!</h1>
	>>   </body>
	>> </html>
	>> ```

	If you visit local server on a local browser, you should see this hello world index page.

	Let's wrap the index page content inside a layout.

2. Write a folder named `_layouts`:

	>> ```bash
	>> mkdir _layouts;
	>> ```

3. Write a file named `_layouts/base.html` with the following code:

	>> ```html
	>> <!doctype html>
	>> <html>
	>>   <head>
	>>     <meta charset="utf-8">
	>>     <title>{{ page.title }}</title>
	>>   </head>
	>>   <body>
	>>     {{ content }}
	>>   </body>
	>> </html>
	>> ```

4. Rename `index.html`:

	>> ```bash
	>> mv index.html index.md;
	>> ```

5. Replace `index.md` content:

	>> ```yaml
	>> ---
	>> layout: base
	>> title: Home
	>> ---
	>> # Hello World
	>> ```

### <a name="2"></a>CLI commands

#### <a name="2a"></a>Jekyll

* Jekyll development server ```jekyll server```

	* ```--livereload```: force the browser to refresh with every change

	* ```--host``` and ```--port```: //

* Build static site ```jekyll build```

#### <a name="2b"></a>Bundle

* ```bundle```
