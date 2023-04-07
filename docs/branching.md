# Task 2 - Creating and Merging a Branch on a Local Repository

Creating a **branch** allows a developer to create a duplicate of their workspace to create changes on. This means any changes that damage the project structure are easily reversible by simply switching back to the original **branch**. In this section we will go through how to

* create a **branch** in your **local repository**

* add changes to a **branch**

* merge changes from one **branch** to another

## Task 2.1 - Creating a New Branch

1\. In VSCode open up the integrated terminal and ensure the terminal path matches the location of your local repository.

??? tip "Hotkey for opening the integrated terminal"
    Pressing ++control+j++ with VSCode open will automatically open the integrated terminal.

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

## Task 2.2 - Add Changes to a Branch

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

## Task 2.3 - Merge Changes From One Branch to Another

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

## Conclusion

After having completed this section of the instructions, you should be able to

[&#10004; Run Git scripting language commands in order to create a new branch of a local repository](/docs/branching.md#task-21---creating-a-new-branch)

[&#10004; Run Git scripting language commands in order to update the branch with changes you have made.](/docs/branching.md#task-22---add-changes-to-a-branch)

[&#10004; Run Git scripting language commands in order to merge your new branch with the original branch.](/docs/branching.md#task-23---merge-changes-from-one-branch-to-another)

If you would like to explore some of the more advanced features the Git scripting language has to offer in terms of branching and merging, [click here](https://git-scm.com/book/en/v2/Git-Branching-Basic-Branching-and-Merging).
