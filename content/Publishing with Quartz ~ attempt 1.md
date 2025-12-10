---
title: "quartz notes v1"
draft: false
tags:
--- 

<u>Note</u>: started with xda-developers.com reference
## Pre-req dependencies
- node.js**: Version 20 or higher. Check with **_node -v_**.
	- My system is at v23.11.0
- **npm**: Version 9.3.1 or higher. Check with **_npm -v_**.
	- My system is at v10.9.2
## Clone and set up Quartz
From the directory that contains the Obsidian vault directory I want to publish...
1. git clone https://github.com/jackyzha0/quartz.git Quartz
2. cd Quartz
3. npm install
4. npx quartz create
	1. Choose how to initialize content in ...
	   Select: "Empty Quartz"
	2. Choose how Quartz should resolve links ...
	   Select "Treat links as shortest path" (this is how Obsidian does it)
## To preview Quartz repo locally
- npx quartz build --serve
- CTRL-C in terminal window to force quit local web server
## To integrate a vault into the Quartz repo
- copy entire contents of vault direct to the "Content" folder inside the Quartz repo
## Configure GitHub repo
from the Quartz repo directory...
1. git init
2. git remote add origin https://github.com/olli-shamlin/Quartz.git
   may need to "git remote remove origin" before the "git remote add..." above
3. git add .
4. git commit -m "first commit"
## Set up github actions for deployment
1. Create a file named "deploy.yml" inside Quartz/.github/workflows populated with the content on the xda-developers.com reference page
## Push to GitHub
After creating a new repo in GitHub named "Quartz"
- git push -u origin v4
## Configure GitHub Pages
From github dashboard in browser...
1. Navigate to Settings: open the Quartz repo on GitHub and click Settings
2. Click on "Pages" in the sidebar
3. Source: Under "Build and deployment", ensure that "GitHub Actions" is selected as the source
## References
- https://github.com/A-wels/obsidian-quartz-publish
- using Vercel to host --> https://charleszw.com/posts/quartz-obsidian
- using Netify to host --> https://oliverfalvai.com/evergreen/my-quartz-+-obsidian-note-publishing-setup
- https://www.xda-developers.com/turned-obsidian-vault-into-website/
- https://nicolevanderhoeven.com/blog/20240126-how-to-publish-your-notes-for-free-with-quartz/
- https://dwywdo.xyz/posts/Building-Your-Own-Obsidian-Publishing-Platform-with-Quartz
- https://blog.zloutek1.com/Main-Notes/Publishing-Obsidian-Notes-with-Quartz
- https://blog.isaiah-harvey.com/dev/2025-06-13-how-i-m-using-quartz-and-obsidian-to-power-my-blog
