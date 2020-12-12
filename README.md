# Intro to Git and GitHub
By: Eric Smith

This tutorial will help new incoming freshman in college become familar with GitHub. This is a very simple tutorial with only a few steps. It will help get freshman on their feet in a new environment of learning and coding.

# What is Git

Git is a version control system (VCS) for tracking changes in computer files and coordinating work on those files among multiple people. It is primarily used for source code management in software development, but it can be used to keep track of changes in any set of files. As a distributed revision control system it is aimed at speed, data integrity, and support for distributed, non-linear workflows.
…every Git directory on every computer is a full-fledged repository with complete history and full version tracking abilities, independent of network access or a central server. [Git(Wikipedia)](https://en.wikipedia.org/wiki/Git)

# Editing basics

The source code of the tutorial is [hosted on GitHub]. The GitHub [Fork & Pull workflow](https://help.github.com/articles/using-pull-requests) is used to accept and review changes.

The tutorial uses the [GitBook](https://legacy.gitbook.com/) service for publishing its documentation. [See more information about how GitBook works](https://help.gitbook.com/).

The tutorial is written in [Markdown mark up language](https://help.github.com/articles/markdown-basics).

You can find any discussions about the contents of the tutorial on the [GitHub issue tracker](https://github.com/DjangoGirls/tutorial/issues).

[Crowdin](https://crowdin.com/project/django-girls-tutorial) platform is used to manage translations. If you want to join an existing translation team or launch a new translation, send an email to the [translation managers](mailto:translations@djangogirls.org) or contact [support team](mailto:hello@djangogirls.org). If you want to propose some small changes or fix typos in existing translations, please create a Pull Request.

# Getting started and prerequisites

For contributing to the tutorial the following is needed to get started:

* a [GitHub account](https://github.com)
* in the case of complex edits familiarity with [Git command line basics](https://help.github.com/articles/set-up-git) or familiarity with an app ([Windows](https://windows.github.com/), [Mac](https://mac.github.com/)) to push your edits made on your computer to GitHub.

## Fork the repository

First fork the [GSKG7 Tutorial](https://github.com/gskg7/Final-Project.git) repository to your personal GitHub account:

![Fork button](contributing/images/fork.png)

# Editing chapter content

## Simple changes

For simple changes like typo corrections you can use the GitHub online editor:

* Open your local fork page on GitHub,
* go to *README.md* file in any chapter,
* press the *Edit* icon (pen)

and you can edit the chapter directly on github.com.

![Edit button](contributing/images/edit.png)

Markdown syntax is used to edit the individual pages of the tutorial.

![GitHub editor](contributing/images/github_editor.png)

Save your changes and create a pull request as explained below.

## New content and complex changes

For adding new chapters, writing longer snippets of text or adding images, you need to get a copy of the tutorial to your local computer.

Either use the GitHub app for your operating system (mentioned above) or `git` command line to get the repository locally. You get the repository address from the front page of your own GitHub repository fork:

    git clone git@github.com:yourgithubusername/tutorial.git

Then, create a branch for your new changes to sit in. It helps to call the branch something related to the changes you are going to make.

    git checkout -b contributing

Download the [GitBook Editor](https://legacy.gitbook.com/editor) app to your computer.

Then you can open the tutorial in GitBook Editor (*File* > *Open book*).

Make any changes in the tutorial using GitBook and then save changes (*Book* > *Save all*).

Then commit the changes using `git` and push the changes to your remote GitHub repository.

Example:

    $ git status
    On branch contributing
    Untracked files:
      (use "git add <file>..." to include in what will be committed)

        contributing_and_editing_this_book/images/gitbook.png

    $ git add contributing_and_editing_this_book/images/gitbook.png

    $ git commit -m "Added gitbook editor screenshot"
    [contributing fe36152] Added gitbook screenshot
     1 file changed, 0 insertions(+), 0 deletions(-)
     create mode 100644 contributing_and_editing_this_book/images/gitbook.png

    $ git push
    Counting objects: 11, done.
    Delta compression using up to 8 threads.
    Compressing objects: 100% (5/5), done.
    Writing objects: 100% (5/5), 266.37 KiB | 0 bytes/s, done.
    Total 5 (delta 1), reused 0 (delta 0)
    To git@github.com:miohtama/tutorial.git
       b37ca59..fe36152  contributing -> contributing

If you don't want to download the GitBook Editor app you can also go to the [GitBook website](https://legacy.gitbook.com/), sign up for free and work directly in your browser.

# Making a pull request

After you have finished your changes you need to create [a pull request](https://help.github.com/articles/using-pull-requests)  on GitHub. DjangoGirls will get notified about the pull request, review your changes, suggest any corrections if needed and then *pull* your changes to the master version.

In your own repository on GitHub press do *Compare & pull request*

![Compare & pull request](contributing/images/pull_request.png)

Fill in the information *why* this change is being made. The reviewer can see the details of the actual change, so you don't need repeat the content of the change.

Then press *Create pull request*.

GitHub emails will notify you for the follow up process.

# Further information and help

GitHub has an excellent [documentation](https://help.github.com/). Check it out if you need help!
