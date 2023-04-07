# Task 1 - Creating a Local Repository

The purpose of this section of the documentation is to help users set up their git hub locally using the command line. This section goes on to show you the step by step process
of the commands needed to set up your repository. The git repository can  be used to saved code that you have worked on, as well as collaborate with other using shared code.

## Task 1.1 - Initialize a Git Repository

1\. To begin with make sure you have VSCode's integrated terminal open on the directory system you are storing in your local repository.

2\. The first step in creating a local repository is to initialize it using the Git scripting language. To do this, input the following command into the command line interface.

```git
git init
```

3\. Run the following command to create a README file:

```git
git add README.md
```

## Task 1.2 - Add Your Changes to The Local Respository

1\. Run the following command in the command line interface to ensure that the Git scripting language can see all the files in the directory.

```git
git status
```

2\. Add any changes or progress made in git repository.

```git
git add .
```

3\. Run the command from step 1 once more to ensure that the Git scripting language is now tracking changes in all the files in the directory.

```git
git status
```

??? success
    If the files show as green in the terminal, that means they're being
    tracked if the files show as red you need to run git add . again.

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
