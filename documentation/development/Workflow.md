# Development Environment

Development is best done in a Ubuntu environment. Follow the instructions at https://jekyllrb.com/docs/ to install the required tools.

# GitHub Pages Workflow

The website will be deployed to GitHub pages, requiring a modified development workflow.

- https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/creating-a-github-pages-site-with-jekyll?platform=linux gives additional information about required jekyll configuration
- https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/testing-your-github-pages-site-locally-with-jekyll explains testing methods

# Updating the Website

1. The Jekyll project is in the `/docs` folder
2. Make the changes locally.
3. Build the modified website with `bundle exec jekyll build --verbose`
4. Test the modifications with `bundle exec jekyll serve`. This launches a local web server at http://localhost:4000
5. Push the modifications to GitHub

# Testing with Firefox

To reload a page in Firefox without using the cache, you can perform a hard refresh by:

- Holding down Ctrl and Shift and pressing R 
- Holding down Ctrl and pressing F5 
- Holding down Shift and clicking the Reload button