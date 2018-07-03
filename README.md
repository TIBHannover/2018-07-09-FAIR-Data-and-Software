# FAIR Data and Software: A Carpentries-based workshop at TIB, Hannover

## See [tibhannover.github.io/2018-07-09-FAIR-Data-and-Software](https://tibhannover.github.io/2018-07-09-FAIR-Data-and-Software/) for the workshop website.

This repository is based on [Software Carpentry][swc-site] and [Data Carpentry][dc-site]'s
template for creating websites for workshops.
Imported from [swcarpentry/workshop-template](https://github.com/swcarpentry/workshop-template).

**Note:**
this template includes some files and directories that most workshops do not need,
but which provide a standard place to put extra content if desired.
See the [design notes][design] for more information about these.

Further instructions are available in [the customization instructions][customization].
This [FAQ][faq] includes a few extra tips (additions are always welcome)
and these notes on [the background and design][design] of this template may help as well.

## Checking Your Changes

If you want to preview your changes on your own machine before publishing them on GitHub,
you can do so as described below.

1.  Run the command

    ~~~
    make serve
    ~~~

    and go to <http://0.0.0.0:4000> to preview your site.
    You can also run this command by typing `make serve`
    (assuming you have Make installed).

3.  Run the command

    ~~~
    make workshop-check
    ~~~

    to check for a few common errors in your workshop's home page.
    (You must have Python 3 installed to do this.)

## Creating Extra Pages

In rare cases,
you may want to add extra pages to your workshop website.
You can do this by putting either Markdown or HTML pages in the website's root directory
and styling them according to the instructions give in
[the lesson template][lesson-example].

## Setting Up a Separate Repository for Learners

If you are teaching Git,
you should create a separate repository for learners to use in that lesson.
You should not have them use the workshop website repository because:

*   your workshop website repository contains many files
    that most learners don't need to see during the lesson,
    and

*   you probably don't want to accidentally merge
    a damaging pull request from a novice Git user
    into your workshop's website while you are using it to teach.

You can call this repository whatever you like,
and add whatever content you need to it.

## Getting and Giving Help

[customization]: https://swcarpentry.github.io/workshop-template/customization/
[design]: https://swcarpentry.github.io/workshop-template/design/
[faq]: https://swcarpentry.github.io/workshop-template/faq/
[lesson-example]: https://swcarpentry.github.io/lesson-example/
[dc-site]: http://datacarpentry.org
[swc-site]: http://software-carpentry.org
