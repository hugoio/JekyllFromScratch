---
layout: base
title: index
---

## JekyllFromScratch

## Table of content

- [Prerequisites](#1)
- [Instructions](#2)

### <a name="1"></a>Prerequisites

This guide requires the following:
* A github account
* An empty public github project
* Jekyll installed on your workstation

### <a name="2"></a>Instructions

1. Clone the empty public github project you made from `yourAccount` reffered as `projectName`:

	>>	```bash
	>>	git clone https://github.com/yourAccount/projectName.git
	>>	```

2. Change working directory:

	>>	```bash
	>>	cd projectName
	>>	```

3. Initialize a new site:

	>>	```bash
	>> bundle init;
	>> echo "gem \"jekyll\"" >> Gemfile;
	>> bundle;
	>>	```

4. Write an empty config file:

	>>	```bash
	>> touch _config.yml
	>>	```

5. Make a `_layouts` folder for site's layouts:

	>>	```bash
	>> mkdir _layouts;
	>>	```

6. Write `_layouts/base.html`:

	>> ```html
	>> <!DOCTYPE html>
	>> <html>
	>>   <head>
	>>     <meta charset="utf-8">
	>>     <title>{{ page.title }}</title>
	>>   </head>
	>>   <body>{{ content }}</body>
	>> </html>
	>> ```

7. Write `index.md`:

	>> ```yaml
	>> ---
	>> layout: base
	>> title: index
	>> ---
	>> Hello World!
	>> ```
