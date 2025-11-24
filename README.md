# invest-schisto-manual
InVEST Schistosomiasis User Manual

## website stuff  
Everything is published from the main branch. We make a drafts branch if needed.  

**Before working on anything: Fetch origin, pull if needed.**  

To update existing pages:  

1. Open the *.qmd file you want to work on
2. Edit
3. Render to see what it looks like as you go (can open in browser!)
4. Render final version.
5. Commit and push
6. Wait ~20sec then check the website https://deleo-lab.github.io/invest-schisto-manual/

To work on a tutorial:

1. Open the `index.qmd` file in the tutorial's folder
2. Edit (note: root is the tutorial folder not the project folder)
3. Render to see what it looks like as you go
4. When you want to post change draft: false in the yaml header
5. Render final version and render `tutorial.qmd`
6. Commit and push
7. Wait ~20sec then check the post on the website

*tutorial are currently ordered based on date, we probably want to update this.*

To add a new page: 

1. Make a new quarto doc as usual, save it to the root directory
2. Edit etc as above
3. In the `_quarto.yml` file add the page (see other pages for formatting)
4. Save that
5. Render all the `*.qmd` pages files (I don't remember having to do this before but was an issue when setting up the website)
6. Commit, push, wait, check

For more info:  
https://ucsb-meds.github.io/creating-quarto-websites/  
https://samanthacsik.github.io/posts/2022-10-24-quarto-blogs/
