---
title: "quartz notes v3"
draft: false
tags:
--- 

### Prerequisites
- node.js v18.14+
- npm v9.3.1+
- git
- obsidian (duh!)
### 1. Download/install Quartz
- git clone https://github.com/jackyzha0/quartz.git \[MY-REPO-NAME]
### 2. Install Quartz dependencies
- cd \[MY-REPO-NAME]
- npm i
### 3. Initialize Quartz
- npx quartz create
	1. Choose how to initialize content in ...
	   Select: "Empty Quartz"
	2. Choose how Quartz should resolve links ...
	   Select "Treat links as shortest path" (this is how Obsidian does it)
### 4. Create a GitHub repo
- create a new repo on github called \[MY-REPO-NAME]
- For "Initialize this repository with:" make sure that "Add a README file" is **not** selected
- Click "Create repository" at the end
### 5. Change the origin remote
1. `git remote -v`
2. `git remote rm origin`
3. `git remote add origin https://github.com/[GITHUB-USER-NAME]/[MY-REPO-NAME].git`
4. `git remote -v`
### 6. Sync your changes
- `npx quartz sync --no-pull`
### 7. Create an Obsidian vault
- Start Obsidian and when asked which vault to open, click on `Open` next to `Open folder as vault`. A Finder dialog window pops up. Navigate to the folder you created (`MY-REPO-NAME`) and then click `Open`.
- Install & enable "Templater" community plugin
- Create a "templates" folder in Obsidian
- In that folder create a template named `note` with front matter like the following:
```
---
title: "How to publish Obsidian notes with Quartz on GitHub Pages"
draft: false
tags:
--- 
```
- Go to `Settings > Templater`. In `Template folder location`, type `templates`
### Link local files to GitHub
- Build site locally:
	- `npx quartz build --serve`
- Then you can open a browser to `https://localhost:8080`

