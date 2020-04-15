# Project Reproducibility


![Iris doggie](IMG_5578)


The goal of this repository is to serve as an example on how to set up any type of data analysis in a reproducible way.

Developing reproducible analysis should be considered a best practice in the sciences. Unfortunately, it is not yet a very widespread practice.
Let me tell you why it is at least good for you as a scientist to strive for reproducibility in your projects:

- You keep all the files to run an analysis organized and contained on the same place.
- You save time for yourself when you need to rerun the analysis further down the road: changed a small variable, fix a database, plot figures again, put them on a report, etc.
- It is easier to share code with other people that might need it, saving you time on explanations and increasing your academic presence.
- Saves you time if you stopped working on the project, even if it's only for a short while, you can easily take over were you left off.
- Save time and resources for others that might take over your project later.
- Get proper credit for the work that you have done, even if it is not published on a journal or book. A reproducible project sets a good precedent of work that someone can build upon and not just start over, supporting proper credit to your own work.

So, what are the main parts of a reproducible project?

## The README file

<img align="right" width="200" src="http://experimentalmath.info/blog/wp-content/uploads/2013/01/miracle-264x300.gif">
<!-- ![Then a miracle occurs...](http://experimentalmath.info/blog/wp-content/uploads/2013/01/miracle-264x300.gif) -->

As you can see, the README file should contain at least a description of your project.
You should also explain the steps to take in order to run the analysis for the first time on a new computer: where to start, do you need to contact someone for more information, etc.

Generally, explain the how and why of each step of the analysis.
If you are are reading this on Github, you can see that its prefered format for a README file is `.md`, for `markdown`. This means that the file has been written using the markdown syntax to format the document in the nice way it is presented on the web. There are quite a few markup languages, and all of them allow us to give properties to plain text, such as formatting, highlights, hyperlinks, and other interactive features. Go to the pencil logo on the upper right corner of the document to look at the syntax of this .md file. It is not hard to interpret, so you can probably figure out how to write your own markdown README file in no time.  Go here for more details on [basic](https://www.markdownguide.org/basic-syntax/ "basic syntax markdown guide") and advanced syntax of a markdown document.

## The data-raw folder

Here goes your original data, before cleaning up.

Take into account a size limit of 50Mb. Any file larger than that that will have a hard time going through git.
If it is available to you, try hosting your data on an online data repository


## The code folder

This contains all code needed for data retrieveing and cleaning, analysis, and figure generation.
Try to automatize tasks by transforming into a function any code entailing a repetitive task, for example:

- code to load the raw data, either from an online database, other repository, or from the `data-raw folder`
- code to clean the raw data and save the clean data in the `data folder`.

Make sure to explain what your code does (document your code) and also provide an example on how to use your functions if any.

## The data folder

Contains your cleaned up data. Data files should be names with something that makes sense, and preferably also display the date those files were first generated.

## A figures or fig folder

This contains all files for your figures.

## A docs folder

This contains your reports.
You can of course write your reports in any format you'd like.
I suggest using a markup language for this, since it aligns with a reproducible workflow.
Among available markup languages, `rmarkdown` is one of the most versatile and fit options for writing scientific reports.   It allows embedding all types of code and run it within the report, to generate a figure, for example.
It allows adding citations and a list of references in any format.

Go here for a quick introduction to the rmarkdown format.

## Some extras

### A license file

As I recently learned, without a license, the contents of a repository are technically closed.
A nice licensing example for a reproducible project that requires proper crediting to the author is given by the Carpentries [here](https://github.com/LunaSare/tutorial-blogdown/blob/gh-pages/LICENSE.md).

For more types of licensing for scientific and reproducible projects:
https://usethis.r-lib.org/reference/licenses.html
https://r-pkgs.org/description.html#license
