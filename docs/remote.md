## Task 3 - Creating a Remote Repository

A **remote repository** allows a developer or organization to store the current version(s) of a project where others can access it. In this section we will go through how to

* create a **remote repository**

* link a **remote repository** to a local repository

### Task 3.1 - Creating a New Remote Repository

1\. Log into [Github](www.github.com) using your Github account credentials. After logging in you should see a page displaying a list of repositories on the left.

2\. Click on the [New] button in the section listing repositories to navigate to the page for creating a new **remote repository**.

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

5\. If you haven't already, include a README file and select the project's main language in the dropdown list for .gitignore templates

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

??? warning "I can't tell if [HTTPS] is selected"
    It can be difficult to tell whether you have selected [HTTPS] or [SSH] due to Github's design. Selected buttons are a shade darker than their unselected counterparts

2\. Copy the url provided in the input field beside the [HTTPS] button.

??? info "What is the url for?"
    The url provided by Github serves as a path for the Git scripting language to locate the internet based storage space they are providing.

3\. In VSCode open up the integrated terminal and ensure the terminal path matches the location of your local repository.

??? tip "Hotkey for opening the integrated terminal"
    Pressing ++control+j++ with VSCode open will automatically open the integrated terminal.

4\. Run the following command to link your local and remote repositories.

```git
git remote add origin <paste_link_here>
```

??? info "What is git remote?"
    `git remote` is an opening phrase which informs the Git scripting language that the actions that follow are in relation to a remote or internet hosted repository.

??? info "What is add origin?"
    `add origin` asks the Git scripting language to create a link to a remote repository called origin that follows the path of the url placed after it.

5\. If your current branch is master, run the following command in the command line interface to change its name to main

```git
git branch -M main
```

6\. Run the following command to upload all of your added and committed changes onto Github's remote repository.

```git
git push -u origin main
```

??? info "What is git push?"
    `git push` is used to update a remote repository with the changes that have been made on the local file system. It can be thought of as the command for saving a backup of your committed work on the internet.

??? info "What does the -u flag do?"
    Flags in Git are an additional modifier included when the action being taken needs to be modified due to a unique circumstance. In this case `-u` informs the Git scripting language that we are also configuring the location for where changes are supposed to be sent to. The `-u` flag only needs to be used when you are pushing to a remote repository for the first time.

??? info "What does origin main do?"
    The `-u` flag has informed Git we are configuring what remote repository to send our data to with `git push`. The `origin master` clause now tells Git what remote repository and what branch to send the data to.

7\. Refresh the page on your Github repository in the browser and ensure that all the changes you pushed have made their way across.

## Conclusion

After having completed this section of the instructions, you should be able to

[&#10004; Walk through Github's repository creation process in order to create a remote repository](/docs/remote.md#task-31---creating-a-new-remote-repository)

[&#10004; Run Git scripting language commands in order to link your remote and local repositories.](/docs/remote.md#task-32---linking-the-remote-repository-to-the-local-repository)

If you would like to explore some of the more advanced features **Github** has to offer in terms of managing **remote repositories**, [explore Github's documentation](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features)
