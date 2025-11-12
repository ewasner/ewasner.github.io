# This Github Repository

This Github repository is the basis on which the personal website of Evan Wasner is generated. Github has a feature called "Github Pages" which uses software called Jekyll to automatically generate a website from the content of the repository. I'm using the "academicpages" template (https://github.com/academicpages/academicpages.github.io) to generate this website.

# Personal notes

These are just some notes to myself to help me understand (and remind myself in the future) how to edit the contents of this repository to generate the website that I want.

## Publications

There is a tsv file "markdown_generator/publivations.tsv". This is what needs to be edited. Then run "publications.py" from the "markdown_generator/ directory" (the ".ipynb" file is just a Jupyter notebook file written by the creators of the academicpages template to explain what to do, it's not necessary).

The "publications.py" script takes the content of the tsv file and converts it into separate markdown files (.md) in the "_publications/" directory. The publications are part of a "Jekyll collection" (declared in the "_config.yml" file) that is used to generate the publications page. So, whereas there are actual "about.md" and (unused) "cv.md" markdown files that are used to generate the About and (unused) CV pages, there is no "publications.md", because the page is just a list of the entries in the Jekyll collection.

## Automatic scripts from Github

In ".github/workflows/", there was a file "scrape_talks.yml". This script would tell Github to automatically run the "talkmap.ipynb" script on any push to main. To prevent this from happening, first I commented out the whole file, but I would still get emails from Github saying that it had tried to run the script, but nothing was happening (because it was empty). So I removed the ".yml" extension. If I ever want to enable this again, I should re-add the .yml extension and un-comment the script.