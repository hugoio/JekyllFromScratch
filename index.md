---
layout: base
title: index
---

&nbsp;  

## Description

This file should explain how to write a simple jekyll-helloworld site and how to host it on GithubPages.

&nbsp;  

### Prerequisites

Your workstation must have:

* [Ruby](https://www.ruby-lang.org/en/)
* [Bundler](https://bundler.io/)
* [Jekyll](https://jekyllrb.com/)

You also need:

* A [Github](https://github.com/) account
* An empty public github [repository](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-new-repository)

&nbsp;  

The Github account username will be reffered as __userName__  
The empty public github repository name will be reffered as __repoName__  

&nbsp;  

### From scratch  

1. Clone the empty public github project you made from __userName__ named __repoName__ and change working directory:

	``` git clone https://github.com/userName/repoName.git ```  
	``` cd repoName ```

2. Initialize a new Jekyll site using __bundle__:

	```bundle init;```  
	```echo "gem \"jekyll\"" >> Gemfile;```  
	```bundle;```  

3. Write an empty ___config.yml__ file:

	```touch _config.yml```

4. Make a ___layouts/__ folder for site's layouts:

	```mkdir _layouts;```

5. Write ___layouts/base.html__:

	```html
	<!DOCTYPE html>
	<html>
  	<head>
    	<meta charset="utf-8">
    	<title>{% raw %}{{ page.title }}{% endraw %}</title>
		<style>
			body {
				margin: 0px; padding: 0px;
				background: #222; color: #eee;
				display: flex;
				justify-content: center;
				text-align: center;
				font-size: 2em;
			}
		</style>
  	</head>
  	<body>{% raw %}{{ content }}{% endraw %}</body>
	</html>
	```

6. Write __index.md__:

	```yaml
	---
	layout: base
	title: index
	---
	Hello World!
	```

7. Push the files to the main branch:

	```git add .```  
	```git commit -m "new commit";```  
	```git push```

8. Enable Github Pages:

	- Go to the repository settings page on Github
	- In the "Code and automation" section of the sidebar, click Pages.
	- Under "Build and deployment", under "Branch", use the None or Branch drop-down menu and select "main" branch as a publishing source.
	- Click Save

	Official [documentation](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)

9. Voilà !
