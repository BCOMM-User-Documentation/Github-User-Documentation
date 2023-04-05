# Introduction

This document aims to help you explore **Git** and **Github**'s **version control** capabilities. The core idea behind using **Git** and **Github** is to have full control over the stability and evolution of a project. This guide will direct you on the basic initialization steps you will need to gain these benefits in your project development.

To learn more about **Git**, **Github** and **version control** [take a look at Github's introductory documentation](https://docs.github.com/en/get-started/using-git/about-git).

## Is This Guide for You?

This guide has been created for beginner level developers with no prior experience in **version control**, Git or Github. Using our detailed instructions, explanations and visual cues you will learn the basic workflow around **version control** in development.

By the end of this guide, you will be able to

* Create a **local repository** using Git's **version control** commands on the **command line interface**

* Link your **local repository** to a **remote repository** hosted on Github

* Create branches on your **local respository** to safely make additions to an existing project

## Software Versions

This guide has been produced for the 2.40.0 version of Git for the Windows 10 OS. If you are using an older version of Git we recommend you use documentation relevant to that version.

There are also separate instruction guides available for macOS and Linux.

## Prerequisites

* Have access to a computer with a functioning Windows 10 OS

* Have access to a keyboard and mousepad connected to your computer

* Have access to an internet connection

* Install a web browser on your computer

* [Install VSCode on your computer](https://code.visualstudio.com/docs/setup/windows)

* [Have a basic understanding of VSCode](https://code.visualstudio.com/docs/introvideos/basics)

* [Install Git and Git Bash on your computer](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)

* [Have a basic understanding of Git Bash commands](https://mally.stanford.edu/~sr/computing/basic-unix.html)

* [Create a Github account](https://docs.github.com/en/get-started/signing-up-for-github/signing-up-for-a-new-github-account)

## Typographical Conventions

This guide uses the typographical conventions specified below to make the content easier to follow and use.

### Commands

Commands expected to be written in a **command line interface** will be wrapped in a code block. E.g.

```git
// git command goes here
```

The icon to the right of the code block allows you to copy the contents inside it, so that you can simply paste it on your own device.

When referencing a small portion of code written in the **command line interface** inline content will have a black background and distinct font. For example `like this`.

### Glossary Terms

Glossary terms will be highlighted in bold. Further explanation on what they mean can be found in the glossary section of the document.

An example of this can be seen above with the term **command line interface**.

### Menu & Option Sequence

Menu and option names will be enclosed in square brackets. The > symbol indicates the sequence in which menu, option and button names should be clicked. E.g.

[Start] > [Power] > [Command Prompt]

### User Inputs

Occasionally the guide will require you input information unique to your personal progress through the process. A description of what this information is will be wrapped between a less than and greater than sign. E.g.

https://&lt;url_to_a_website&gt;

### Keyboard Shortcuts

Any keyboard shortcuts referenced in this guide will be wrapped in curly braces. If multiple keys need to be pressed together they will be separated by a plus sign. E.g.

{ Ctrl + C }

### Admonitions

This guide uses information and warnings blocks to provide additional context around specific actions. These elements look as follows

???+ info
    Provides additional information surrounding a step in the instructions. It is always wrapped in a blue content box, with an i icon on the far left.

???+ tip
    Provides non critical but useful information surrounding a step in the instructions. It is always wrapped in a cyan content box, with a flame icon on the far left.

???+ warning
    Provides information surrounding a step in the instructions that can cause errors or create a permanent change. It is always wrapped in an orange content box, with a danger icon on the far left.

All admonitions can be minimized and expanded by clicking on the colored header bar.

# Instructions

## Task 1 - Creating a Local Repository

## Task 2 - Creating and Merging a Branch on a Local Repository

Creating a **branch** allows a developer to create a duplicate of their workspace to create changes on. This means any changes that damage the project structure are easily reversible by simply switching back to the original **branch**. In this section we will go through how to

* create a **branch** in your **local repository**

* add changes to a **branch**

* merge changes from one **branch** to another

### Task 2.1 - Creating a New Branch

1\. In VSCode open up the integrated terminal and ensure the terminal path matches the location of your local repository.

??? tip "Hotkey for opening the integrated terminal"
    Pressing { Ctrl + J } with VSCode open will automatically open the integrated terminal.

2\. Input the following command in the terminal to create a new branch with a suitable name

```git
git checkout -b <branch_name>
```

??? info "What is git checkout?"
    `git checkout` is an opening phrase which tells the Git scripting language that the user is attempting to view the data in a different branch. In normal circumstances the command is immediately followed by the branch name of the branch you are trying to view.

??? info "What does the -b flag do?"
    Flags in Git are an additional modifier included when the action being taken needs to be modified due to a unique circumstance. In this case `-b` informs the Git scripting language that we are both creating a new branch and changing branches to view it at the same time.

??? tip "Best practices for naming a branch"
    In the tech industry branches are generally distinguished by the type of change you are trying to create. This is usually either a bug-fix, feature or development. The naming convention is `<type_of_change>/<change_description>`. For example `bug-fix/fix-image-routes`.

3\. Input the following command in the terminal to verify that your new branch has been made. You should see the new branch's name highlighted in the list produced by the command.

```git
git branch
```

??? info "Why is my new branch highlighted in the command output?"
    Since the `git branch` command retrieves a list of all branches, as a convenience feature the Git scripting language uses color and the `*` character to highlight the branch you are currently on.

### Task 2.2 - Add Changes to a Branch

1\. Create your desired modifications on your new branch.

2\. Input the following command in the terminal to make the Git scripting language aware of the changes you want to add.

```git
git add .
```

??? info "What does git add . do?"
    `git add` informs the Git scripting language of what files you want it to update on its copy of your project. The `.` that follows it a shorthand that tells the Git scripting language that we want it to update changes on all the files that have been modified. If you wanted to add a specific set of files, you would run the `git add <file_name>` command for each one.

3\. Input the following command in the terminal to make the Git scripting language update its version of your project with the highlighted changes.

```git
git commit -m "<description_of_the_changes_made>"
```

??? info "What is git commit?"
    `git commit` informs the Git scripting language to transfer any changes added with the `git add` command onto its copy of your project. After this command is run with the ` git add .` command there are no changes between the project in your OS memory and the version being stored by Git.

??? info "What does the -m flag do?"
    Flags in Git are an additional modifier included when the action being taken needs to be modified due to a unique circumstance. In this case `-m` informs the Git scripting language that we are both creating a new commit and creating a message to describe it at the same time.

??? tip "Always make sure your commits have a meaningful message"
    Work that has been committed is viewed by colleagues and potentially even yourself down the line. Having a meaningful description of each incremental change makes it clear from the outside in as to what your thought process and approach was.

### Task 2.3 - Merge Changes From One Branch to Another

1\. Input the following command in the terminal to swap back to your original branch.

```git
git checkout <original_branch_name>
```

??? info "What is git checkout?"
    `git checkout` is an opening phrase which tells the Git scripting language that the user is attempting to view the data in a different branch. In normal circumstances the command is immediately followed by the branch name of the branch you are trying to view.

??? tip "Can't remember the name for your original branch?"
    The `git branch` command will present you with a list of branches in your local repository. Find the name of the branch in the list and then use it with the `git checkout` command.

2\. Input the command below in the terminal to verify that you are now in the correct branch. You should see the original branch's name highlighted in the list produced by the command.

```git
git branch
```

??? info "Why is the original branch highlighted in the command output?"
    Since the `git branch` command retrieves a list of all branches, as a convenience feature the Git scripting language uses color and the `*` character to highlight the branch you are currently on.

3\. Now that you are on the original branch, input the command below in the terminal to merge your new branch into it. If the merge is successful you should see all the changes made in the new branch now visible in the original branch.

```git
git merge <new_branch_name>
```

??? info "What is git merge?"
    `git merge` informs the Git scripting language to merge the changes on the branch name written at the end of the command with the branch the developer is currently on.

??? info "What happens to my new branch after I merge?"
    Nothing! Your new branch still exists. Though any further changes you make outside the branch will not be stored in the branch's version of your project.

## Task 3 - Creating a Remote Repository and Linking it to The Local Repository

A **remote repository** allows a developer or organization to store the current version(s) of a project where others can access it. In this section we will go through how to

* create a **remote repository**

* link a **remote repository** to a local repository

### Task 3.1 - Creating a New Remote Repository

1\. Log into [Github](www.github.com) using your Github account credentials. After logging in you should see a page displaying a list of repositories on the left.

2\. Click on the [New] button in the section listing repositories to navigate to the page for creating a new **remote repository**

??? warning "Missing [New] button"
    If you can't see the [New] button it might be due to the size of your web browser. Try resizing the browser to fill the screen if it isn't already full screen.

??? tip "Redirect to the new repository form using the URL"
    In the future you can load directly into [www.github.com/new](www.github.com/new) once logged in and skip right to step 3 of this task.

3\. Fill in the repository name and description inputs with a meaningful name and a summary for your project goal.

??? tip "Name and describe repositories the way employers want"
    The repository name is an opportunity to describe the projects functionality in two to three words. The description is an opportunity for a project summary n two to three sentences. Try keep this mind when making new repositories!

4\. Decide whether you would like for the repository to be [Public] or [Private]. Public repositories are visible to the internet, whereas private repositories are shared only to those you choose.

??? tip "Default to private, change to public"
    If a repository is being made for learning purposes it is usually best to start it off as private. From there, if you want to make it visible for employment of business purposes, the repository visibility can be changed to public through its settings. To learn how [click here](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/managing-repository-settings/setting-repository-visibility).

5\. Include a README file and select the project's main language in the dropdown list for .gitignore templates

??? info "What is a .gitignore file?"
    The .gitignore file is used by Github to identify any files on your local repository that shouldn't be saved on its cloud service. By selecting your main project language Github produces an intelligent template of file types that would be unnecessary or dangerous to store. To learn more [click here](https://git-scm.com/docs/gitignore).

??? info "Why include a README?"
    For any project it is recommended to include a README.md file. README files serve as a space where you can make a more detailed summary of the technology, functionality and structure of a project. At the very least this is very useful when returning to old work after a while. To learn more [click here](https://www.freecodecamp.org/news/how-to-write-a-good-readme-file/).

6\. If your repository is public, choose a license for your work that defines the regulations around your code being used by others.

??? tip "The MIT license is your best friend"
    The MIT license is simple, easy to understand and quite fair, making it my personal recommendation for learning projects. Important points are that it allows for free distribution of the work with no liability on the original author. To learn more [click here](https://snyk.io/learn/what-is-mit-license/).

7\. Select the [Create repository] button on the bottom of the page to create your Github repository.

### Task 3.2 - Linking The Remote Repository to The Local Repository

1\. On the main page for your newly created remote repository, make sure the [HTTPS] button is selected in the Quick Setup header bar.

??? info "How do I know if [HTTPS] is selected?"
    It can be difficult to tell whether you have selected [HTTPS] or [SSH] due to Github's design. Selected buttons are a shade darker than their unselected counterparts

2\. Copy the url provided in the input field beside the [HTTPS] button.

??? info "What is the url for?"
    The url provided by Github serves as a path for the Git scripting language to locate the internet based storage space they are providing.

3\. In VSCode open up the integrated terminal and ensure the terminal path matches the location of your local repository.

??? tip "Hotkey for opening the integrated terminal"
    Pressing { Ctrl + J } with VSCode open will automatically open the integrated terminal.

4\. Run the following command to link your local and remote repositories.

```git
git remote add origin <paste_link_here>
```

??? info "What is git remote?"
    `git remote` is an opening phrase which informs the Git scripting language that the actions that follow are in relation to a remote or internet hosted repository.

??? info "What is add origin?"
    `add origin` asks the Git scripting language to create a link to a remote repository called origin that follows the path of the url placed after it.

5\. Run the following command to upload all of your added and committed changes onto Github's remote repository.

```git
git push -u origin master
```

??? info "What is git push?"
    `git push` is used to update a remote repository with the changes that have been made on the local file system. It can be thought of as the command for saving a backup of your committed work on the internet.

??? info "What does the -u flag do?"
    Flags in Git are an additional modifier included when the action being taken needs to be modified due to a unique circumstance. In this case `-u` informs the Git scripting language that we are also configuring the location for where changes are supposed to be sent to. The `-u` flag only needs to be used when you are pushing to a remote repository for the first time.

??? info "What does origin master do?"
    The `-u` flag has informed Git we are configuring what remote repository to send our data to with `git push`. The `origin master` clause now tells Git what remote repository and what branch to send the data to.

6\. Refresh the page on your Github repository in the browser and ensure that all the changes you pushed have made their way across.

# Glossary

# Troubleshooting
