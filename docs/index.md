# Introduction

This document aims to help you explore **Git** and **Github**'s **version control** capabilities. The core idea behind using **Git** and **Github** is to have full control over the stability and evolution of a project. This guide will direct you on the basic initialization steps you will need to gain these benefits in your project development.

To learn more about **Git**, **Github** and **version control** [take a look at Github's introductory documentation](https://docs.github.com/en/get-started/using-git/about-git).

## Is This Guide for You?

This guide has been created for beginner level developers with no prior experience in **version control**, **Git** or **Github**. Using our detailed instructions, explanations and visual cues you will learn the basic workflow around **version control** in development.

By the end of this guide, you will be able to

* Create a **local repository** using Git's **version control** commands on the **command line interface**

* Link your **local repository** to a **remote repository** hosted on Github

* Create branches on your **local respository** to safely make additions to an existing project

## Software Versions

This guide has been produced for the 2.40.0 version of **Git** for the Windows 10 OS. If you are using an older version of **Git** we recommend you use documentation relevant to that version.

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

[Start] > [Power] > [Restart]

### User Inputs

Occasionally the guide will require you input information unique to your personal progress through the process. A description of what this information is will be wrapped between a less than and greater than sign. E.g.

https://&lt;url_to_a_website&gt;

### Keyboard Shortcuts

Any keyboard shortcuts referenced in this guide will be wrapped in curly braces. If multiple keys need to be pressed together they will be separated by a plus sign. E.g.

++control+c++

### Admonitions

This guide uses information and warnings blocks to provide additional context around specific actions. These elements look as follows

???+ info
    Provides additional information surrounding a step in the instructions. It is always wrapped in a blue content box, with an i icon on the far left.

???+ tip
    Provides non critical but useful information surrounding a step in the instructions. It is always wrapped in a cyan content box, with a flame icon on the far left.

???+ warning
    Provides information surrounding a step in the instructions that can be difficult to achieve due to some misleading feature. It is always wrapped in an orange content box, with an exclamation mark on the far left.

???+ danger
    Provides context around common errors that can be encountered whilst following the instruction set. It is always wrapped in a red content box, with a lightning bolt icon on the far left.

???+ success
    Provides a description or explanation of the output that should be achieved if a task is successful. Sometimes it will include an embedded image to give a visual cue for what a successful action looks like. It is always wrapped in a green content box, with a tick icon on the far left.

All admonitions can be minimized and expanded by clicking on the colored header bar.
