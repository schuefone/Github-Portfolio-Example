# Creating a GitHub Page

# Introduction

We show how to create a repository on github, fill it with files from a project that you’d like to post on your public repository  and share it as a web page. We’ll go through the steps of creating a github repository, configuring it as a web page, constructing the content and importing figures from plotly. We will demonstrate this by putting this document on github as a web page.

# Methods & Results

## Creating the Repository

This section assumes that you have already created a github account and that you have created your default github page of the form \[userid\].github.io.

Visit your github account and create a new repository. For this demonstration, we create a repository called “Github Portfolio Example”. Accept the defaults when creating this repository.

Immediately upon creating your repository, you will see a link “creating a new file”. Click on that link and create a file called “README.md”. Add some trivial content to the file, e.g. \#\#\# Test \#\#\# and click “Commit changes…” Once you’ve committed the changes, you should see the new file in the repository.

Next, go to the Settings for the repository which can be found at the right end of the menu across the top of the page. On the left sidebar, choose “Pages”. Under the “Branch” section, choose “main” from the dropdown menu and click “Save”. Wait a minute or two and reload the page. Once the page has been activated, you should see a notification at the top saying “Your site is live at…” The url that follows is the web page for this new repository. In the case of this example, it is: [https://schuefone.github.io/Github-Portfolio-Example/](https://schuefone.github.io/Github-Portfolio-Example/)

Visiting your new site, you should see a simple page with “Test” at the top. Visiting *my* site, you should see this report.

## Adding Content

The contents of this webpage are controlled by the README.md file. This is a markdown file. Markdown is a way of formatting text. Here’s an overview of the [markdown syntax](https://github.com/adam-p/markdown-here/wiki/markdown-cheatsheet). To modify the contents of README.md, click on it and then click on the pencil icon in the upper right corner.

To see the contents of the markdown file for *this* web page, visit the [github repository for this web page](https://github.com/schuefone/Github-Portfolio-Example), click on the README.md file and click on the “raw” button.

## Adding Plotly Figures

In data analysis with python, plotly visualizations are often interactive. To embed one of these live visualizations in your github page it’s necessary to do the following:

1. In addition to your other plotly import statements, add: `import plotly.io as pio`  
2. Generate your figure (assuming it’s name “fig”) as you normally would and immediately call `fig.write_html(“filename.html”)`  
3. Locate the file (download it to your computer if necessary).  
4. Visit your github repository. Choose “Add file” from the drop down menu near the top. Choose “Upload files”. Navigate to the html file and upload it to the repository. (make sure you click the “commit” button before navigating away)  
5. In your README.md file, where you want the figure to appear, insert the following: `{% include_relative filename.html %}` where you replace the filename with the name of your file.
