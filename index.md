---
layout: base
title: Jekyll notebook
---

### <a name="1"></a>Prerequisites

This guide requires the following:  

* [Jekyll](https://jekyllrb.com/docs/) installed on your workstation
* An empty public github [project](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-new-repository)


### <a name="2"></a>From scratch

1. Clone the empty public github project you made from `yourAccount` named `projectName` and change working directory:

	```git clone https://github.com/yourAccount/projectName.git;```  
	```cd projectName;```

3. Initialize a new site using `bundle`:

	```bundle init;```  
	```echo "gem \"jekyll\"" >> Gemfile;```  
	```bundle;```  

4. Write an empty `_config.yml` file:

	```touch _config.yml```

5. Make a `_layouts/` folder for site's layouts:

	```mkdir _layouts;```

6. Write `_layouts/base.html`:

	```html
	<!DOCTYPE html>
	<html>
  	<head>
    	<meta charset="utf-8">
    	<title>{{ page.title }}</title>
  	</head>
  	<body>{{ content }}</body>
	</html>
	```

7. Write `index.md`:

	```yaml
	---
	layout: base
	title: index
	---
	Hello World!
	```

8. Build site:

	```bundle exec jekyll build```

9. Push the files to the main branch:

	```git add .```  
	```git commit -m "new commit";```  
	```git push origin main;```

10. Update Github project settings ?

	[?](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-new-repository)
