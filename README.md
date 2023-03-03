# notion-deploy-action
This repository is for deploying notion pages into static site on github.  

The workflow is as follow:
1. Use [loconotion](https://github.com/leoncvlt/loconotion#advanced-usage) to parse notion page 
2. Place the output html files into gh-pages branch
3. Setup github pages through settings
 
The workflow is packed into a github action yaml file (Originally created by [artxia](https://github.com/artxia/Action-NotionSite)).  
It is modified to accept a toml file in the repository instead of using github secrets.

## How to use
1. Copy all the files into the target repository. (Or use template)
2. Modify the .toml file to suit custom need ([Full file setting](https://github.com/leoncvlt/loconotion#advanced-usage))
3. Go to **Settings/Actions/General** and choose **Workflow permissions** to `Read and Write permissions`
4. Run workflow `Deploy to Pages` on the left side in **Actions** to start generating the htmls
5. After the htmls are generated in the gh-pages branch, go to **Settings/Pages**, set **Source** to `Deploy from a branch`, and choose `gh-pages /root` as the **Branch**
6. The github site url should appears on the top of **Settings/Pages**

## Credits
Credits to these awesome works
- [loconotion](https://github.com/leoncvlt/loconotion#advanced-usage) : Notion static site parser
- [Action-NotionSite](https://github.com/artxia/Action-NotionSite) : Notion deploy action template    
