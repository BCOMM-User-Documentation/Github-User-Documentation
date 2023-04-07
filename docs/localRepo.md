# Task 1 - Creating a Local Repository

The purpose of this section of the documentation is to help users set up their git hub locally using the command line. This section goes on to show you the step by step process
of the commands needed to set up your repository. The git repository can  be used to saved code that you have worked on, as well as collaborate with other using shared code.

## Task 1.1 - Initialize a Git Repository

1\. To begin with make sure you have VSCode's integrated terminal open on the directory system you are storing in your local repository.

2\. The first step in creating a local repository is to initialize it using the Git scripting language. To do this, input the following command into the command line interface.

```git
git init
```

??? info "What is git init?"
    `git init` informs the Git scripting language to create a .git directory at your current location in the terminal. The .git directory is where your local repository is stored.

3\. Run the following command to create a README file:

```git
git add README.md
```

??? info "Why include a README?"
    For any project it is recommended to include a README.md file. README files serve as a space where you can make a more detailed summary of the technology, functionality and structure of a project. At the very least this is very useful when returning to old work after a while. To learn more [click here](https://www.freecodecamp.org/news/how-to-write-a-good-readme-file/).

## Task 1.2 - Add Your Changes to The Local Respository

1\. Run the following command in the command line interface to ensure that the Git scripting language can see all the files in the directory.

```git
git status
```

??? info "What does git status do?"
    `git status` displays a list of paths inside the project which are different from the information that is stored in the local repository. When you first start a repository every file in the project should appear marked in red after the command is run.

??? success
    A list of filepaths prefixed with `modified:` and marked in red. The list should include every file in the project.

2\. Add any changes or progress made in git repository.

```git
git add .
```

??? info "What does git add . do?"
    `git add` informs the Git scripting language of what files you want it to update on its copy of your project. The `.` that follows it a shorthand that tells the Git scripting language that we want it to update changes on all the files that have been modified. If you wanted to add a specific set of files, you would run the `git add <file_name>` command for each one.

3\. Run the command from step 1 once more to ensure that the Git scripting language is now tracking changes in all the files in the directory.

```git
git status
```

??? success
    If the files listed display as green in the terminal, that means they're being tracked.

4\. Finalize those changes by adding the following command into you command line interface. This so that the Git scripting language knows that these changes are authorized to save in the repository

```git
git commit -m "<meaningful_commit_message>"
```

??? info
    After the git commit you should add -m followed by a short message describing the changes in quotation marks.

5\. Run the `git status` command from step 1 and 3 to confirm that the changes have been moved over to your local repository.

## Conclusion

After having completed this section of the instructions, you should be able to

[&#10004; Run Git scripting language commands in order to create a new local repository](/docs/localRepo.md#task-11---initialize-a-git-repository)

[&#10004; Run Git scripting language commands in order to update a local repository with new changes](/docs/localRepo.md#task-12---add-your-changes-to-the-local-respository)

If you would like to explore some of the more advanced features Github has to offer in terms of managing remote repositories, [explore Github's documentation](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features)
