# Task 1 - Creating a Local Repository

The purpose of this section of the documentation is to help new developers use **Git** on the **command line interface** to create a local backup of their work. In this section we will go through how to

* Initialize a Git repository

* Add your changes to the **local repository**

## Task 1.1 - Initialize a Git Repository

1\. To begin with make sure you have VSCode's integrated **terminal** open on the directory you want to store in your **local repository**.

??? tip "Hotkey for opening the integrated terminal"
    Pressing ++control+j++ with VSCode open will automatically open the integrated terminal.

2\. On the right side tab of the **terminal**, check to see if your current **terminal** is `bash`. If not click the [&#709;] arrow beside the [+] button on the top right menu in the terminal. From the drop down list select `Git Bash`.

???+ success
    The terminal should open a new window labelled `bash`.

    <img src='/terminal-success.png'>

??? danger "I can't find **Git Bash** in the drop down list"
    Check to ensure that you have installed **Git** and **Git Bash** correctly. In your current terminal input the following code

    ```git
    git --version
    ```

    If a version is not returned then your installation was most likely not successful.

3\. The first step in creating a **local repository** is to initialize it using the **Git** scripting language. To do this, input the following command into the **command line interface**.

```git
git init
```

??? info "What is git init?"
    `git init` informs the **Git** scripting language to create a .git directory at your current location in the terminal. The **.git directory** is where your local repository is stored.

???+ success
    When opening file explorer and navigating to the filepath your project is in, you should see a **.git directory**.

    <img src='/git-init-success.png'>

??? danger "I can't see the .git folder in my project directory"
    It is possible that you cannot see the folder even though it exists due to your system settings. Folders beginning with `.` are hidden folders and by default are not visible in File Explorer. To learn how to change these settings, [click here](https://support.microsoft.com/en-us/windows/view-hidden-files-and-folders-in-windows-97fbc472-c603-9d90-91d0-1166d1d9f4b5).

4\. Run the following command to create a README file:

```git
>> README.md
```

??? info "What does >> do?"
    `>>` is a snippet of the **Bash** scripting language used by the **Git Bash** terminal. The shorthand asks **Bash** to create a file in the current directory with whatever name and extension follows it.

??? info "Why include a README?"
    For any project it is recommended to include a README.md file. README files serve as a space where you can make a more detailed summary of the technology, functionality and structure of a project. At the very least this is very useful when returning to old work after a while. To learn more [click here](https://www.freecodecamp.org/news/how-to-write-a-good-readme-file/).

???+ success
    In the [Explorer] tab in VSCode you should see a file called `README.md` added to the list of files inside the project directory.

    <img src='/add-readme-success.png'>

## Task 1.2 - Add Your Changes to The Local Respository

1\. Run the following command in the **command line interface** to ensure that the **Git** scripting language can see all the files in the directory.

```git
git status
```

??? info "What does git status do?"
    `git status` displays a list of paths inside the project which are different from the information that is stored in the **local repository**. When you first start a repository every file in the project should appear marked in red after the command is run.

???+ success
    A list of filepaths marked in red. The list should include every file in the project.

    <img src='/init-status-success.png'>

2\. Input the following command in the **terminal** to make the **Git** scripting language aware of the changes you want to add.

```git
git add .
```

??? info "What does git add . do?"
    `git add` informs the **Git** scripting language of what files you want it to update on its copy of your project. The `.` that follows it a shorthand that tells the **Git** scripting language that we want it to update changes on all the files that have been modified. If you wanted to add a specific set of files, you would run the `git add <file_name>` command for each one.

3\. Run the command from step 1 once more to ensure that the **Git** scripting language is now tracking changes in all the files in the directory.

```git
git status
```

???+ success
    A list of filepaths prefixed with `new file:` and marked in green. The list should include every file in the project.

    <img src='/post-add-status-success.png'>

4\. Finalize those changes by adding the following command into the **command line interface**. This so that the **Git** scripting language knows that these changes are authorized to save in the repository

```git
git commit -m "<description_of_the_changes_made>"
```

??? info "What is git commit?"
    `git commit` informs the **Git** scripting language to transfer any changes added with the `git add` command onto its copy of your project. After this command is run with the ` git add .` command there are no changes between the project in your OS memory and the version being stored by **Git**.

??? info "What does the -m flag do?"
    Flags in **Git** are an additional modifier included when the action being taken needs to be modified due to a unique circumstance. In this case `-m` informs the **Git** scripting language that we are both creating a new commit and creating a message to describe it at the same time.

??? tip "Always make sure your commits have a meaningful message"
    Work that has been committed is viewed by colleagues and potentially even yourself down the line. Having a meaningful description of each incremental change makes it clear from the outside in as to what your thought process and approach was.

???+ success
    For every file in the project an output should be generated containing the file name prefixed by `create mode` and a string of numbers.

    <img src='/commit-success.png'>

5\. Run the `git status` command from step 1 and 3 to confirm that the changes have been moved over to your **local repository**.

```git
git status
```

???+ success
    The returned message should end with `nothing to commit, working tree clean`. This means that your local repository and the project on your OS are now in sync.

    <img src='/post-commit-success.png'>

## Conclusion

After having completed this section of the instructions, you should be able to

[&#10004; Run **Git** scripting language commands in order to create a new **local repository**](/docs/localRepo.md#task-11---initialize-a-git-repository)

[&#10004; Run **Git** scripting language commands in order to update a **local repository** with new changes](/docs/localRepo.md#task-12---add-your-changes-to-the-local-respository)

If you would like to explore some of the more advanced features the **Git** scripting language has to offer in terms of creating **local repositories**, [click here](https://git-scm.com/docs/git-init).
