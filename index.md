---
layout: base
title: Jekyll notebook
---

&nbsp;  

### <a name="1"></a>Prerequisites

&nbsp;  

This guide requires the following:  

* [Jekyll](https://jekyllrb.com/docs/) installed on your workstation
* An empty public github [project](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-new-repository)

&nbsp;  

### <a name="2"></a>From scratch  

&nbsp;  

1. Clone the empty public github project you made from __yourAccount__ named __projectName__ and change working directory:

	```git clone https://github.com/yourAccount/projectName.git;```  
	```cd projectName;```

3. Initialize a new site using __bundle__:

	```bundle init;```  
	```echo "gem \"jekyll\"" >> Gemfile;```  
	```bundle;```  

4. Write an empty ___config.yml__ file:

	```touch _config.yml```

5. Make a ___layouts/__ folder for site's layouts:

	```mkdir _layouts;```

6. Write ___layouts/base.html__:

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

7. Write __index.md__:

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

10. Update Github project settings:

	[Official documentation](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)
