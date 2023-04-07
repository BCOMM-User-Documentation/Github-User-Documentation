## Task 3 - Creating a Remote Repository

A **remote repository** allows a developer or organization to store the current version(s) of a project where others can access it. In this section we will go through how to

* create a **remote repository**

* link a **remote repository** to a local repository

### Task 3.1 - Creating a New Remote Repository

1\. Log into [Github](www.github.com) using your **Github** account credentials. After logging in you should see a page displaying a list of repositories on the left.

???+ success
    A successful login should take you to the page displayed below

    <img src='/github-new.png'>

2\. Click on the [New] button in the section listing repositories on the left tab of the homepage in order to navigate to the page for creating a new **remote repository**.

??? warning "Missing [New] button"
    If you can't see the [New] button it might be due to the size of your web browser. Try resizing the browser to fill the screen if it isn't already full screen.

??? tip "Redirect to the new repository form using the URL"
    In the future you can load directly into [www.github.com/new](www.github.com/new) once logged in and skip right to step 3 of this task.

???+ success
    Clicking the [New] button should take you to the page displayed below

    <img src='/new-repo.png'>

3\. Fill in the repository name and description inputs with a meaningful name and a summary for your project goal.

??? tip "Name and describe repositories the way employers want"
    The **repository** name is an opportunity to describe the project's functionality in two to three words. The description is an opportunity for a project summary in two to three sentences. Try keep this mind when making new repositories!

???+ success
    After you have filled these inputs the top section of your form should look something like this.

    <img src='/repo-inputs.png'>

4\. Decide whether you would like for the repository to be [Public] or [Private]. Public repositories are visible to the internet, whereas private repositories are shared only to those you choose.

??? tip "Default to private, change to public"
    If a **repository** is being made for learning purposes it is usually best to start it off as private. From there, if you want to make it visible for employment of business purposes, the **repository** visibility can be changed to public through its settings. To learn how [click here](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/managing-repository-settings/setting-repository-visibility).

???+ success
    After you have selected your choice the middle section of the form should look like this.

    <img src='/private-repo.png'>

5\. If you haven't already, include a README file and select the project's main language in the drop down list for .gitignore templates

??? info "What is a .gitignore file?"
    The .gitignore file is used by Github to identify any files on your local repository that shouldn't be saved on its cloud service. By selecting your main project language Github produces an intelligent template of file types that would be unnecessary or dangerous to store. To learn more [click here](https://git-scm.com/docs/gitignore).

??? warning "I can't find Javascript in the drop down list"
    Javascript uses a **runtime environment** called **Node** when it is used outside of the browser. If your file uses Javascript, find **Node** from the drop down list.

??? info "Why include a README?"
    For any project it is recommended to include a README.md file. README files serve as a space where you can make a more detailed summary of the technology, functionality and structure of a project. At the very least this is very useful when returning to old work after a while. To learn more [click here](https://www.freecodecamp.org/news/how-to-write-a-good-readme-file/).

6\. If your repository is public, choose a license for your work that defines the regulations around your code being used by others.

??? tip "The MIT license is your best friend"
    The MIT license is simple, easy to understand and quite fair, making it my personal recommendation for learning projects. Important points are that it allows for free distribution of the work with no liability on the original author. To learn more [click here](https://snyk.io/learn/what-is-mit-license/).

7\. Select the [Create repository] button on the bottom of the page to create your **remote repository**.

???+ success
    After creating your **repository** you should be redirected to the following page

    <img src='/new-repo-homepage.png'>

### Task 3.2 - Linking The Remote Repository to The Local Repository

1\. On the main page for your newly created **remote repository**, click on the big green [Code] button and make sure the [HTTPS] button is selected.

??? warning "I can't see the [Code] button"
    If you can't see the [Code] button it might be due to the size of your web browser. Try resizing the browser to fill the screen if it isn't already full screen.

??? warning "I can't tell if [HTTPS] is selected"
    It can be difficult to tell whether you have selected [HTTPS] or [SSH] due to **Github**'s design. Selected buttons are either a shade darker or underlined depending on the view.

???+ success
    If you have selected the [HTTPS] button it should be underlined and the input field below it should contain a url. An example of this can be seen below

    <img src='/copy-url.png'>

2\. Copy the url provided in the input field below the [HTTPS] button.

??? info "What is the url for?"
    The url provided by **Github** serves as a path for the **Git** scripting language to locate the internet based storage space they are providing.

3\. In VSCode open up the integrated **terminal** and ensure the terminal path matches the location of your **local repository**.

??? tip "Hotkey for opening the integrated terminal"
    Pressing ++control+j++ with VSCode open will automatically open the integrated **terminal**.

4\. On the right side tab of the **terminal**, check to see if your current **terminal** is `bash`. If not click the [&#709;] arrow beside the [+] button on the top right menu in the terminal. From the drop down list select `Git Bash`.

???+ success
    The **terminal** should open a new window labelled `bash`.

    <img src='/terminal-success.png'>

??? danger "I can't find **Git Bash** in the drop down list"
    Check to ensure that you have installed **Git** and **Git Bash** correctly. In your current terminal input the following code

    ```git
    git --version
    ```

    If a version is not returned then your installation was most likely not successful.

5\. Run the following command to link your local and remote repositories.

```git
git remote add origin <paste_link_here>
```

??? info "What is git remote?"
    `git remote` is an opening phrase which informs the **Git** scripting language that the actions that follow are in relation to a remote or internet hosted **repository**.

??? info "What is add origin?"
    `add origin` asks the **Git** scripting language to create a link to a **remote repository** called origin that follows the path of the url placed after it.

5\. If your current **branch** is master, run the following command in the **command line interface** to change its name to main

```git
git branch -M main
```

??? info "What does git branch do?"
    `git branch` is an opening phrase which informs the **Git** scripting language that the actions that follow are in relation to one or more **branch**es.

??? info "What does the -M flag do?"
    Flags in **Git** are an additional modifier included when the action being taken needs to be modified due to a unique circumstance. In this case `-M` informs the **Git** scripting language that we are renaming the original branch of this repository to whatever follows the flag.

??? info "Why am I changing the branch name to main?"
    **Github**'s main **branch** is called main. Having your main **branch**es on your local and remote **repository** called something different can cause complications, so it is recommended to make them match.

6\. Run the following command to retrieve your .gitignore file from the **remote repository**.

```git
git pull --set-upstream origin main --allow-unrelated-histories
```

??? info "What is git pull?"
    `git pull` retrieves updates from the **remote repository** and integrates it into your **local repository**.

??? info "What does the --set-upstream flag do?"
    Flags in **Git** are an additional modifier included when the action being taken needs to be modified due to a unique circumstance. In this case `--set-upstream` informs the **Git** scripting language that we are also configuring the location for where changes are supposed to be sent to. The `--set-upstream` flag only needs to be used when you are pulling from a **remote repository** for the first time.

??? info "What does origin main do?"
    The `--set-upstream` flag has informed **Git** we are configuring what **remote repository** to retrieve our data from with `git pull`. The `origin master` clause now tells **Git** what **remote repository** and what **branch** to retrieve the data from.

??? info "What does the --allow-unrelated-histories flag do?"
    Flags in **Git** are an additional modifier included when the action being taken needs to be modified due to a unique circumstance. In this case `--allow-unrelated-histories` informs the **Git** scripting language that we are merging two repositories which have separate files and commit in them. This flag needs to be used because behind the scenes **Github** created a commit on the **local repository** in order to create our .gitignore file

???+ success
    The **terminal** should return an address from which the data was pulled alongside the **branch**. After this it return a message listing out the number of files changed and the number of lines inserted and deleted. Followed by a line ending with the file name and beginning with `create mode` for every new file created.

    <img src='/successful-pull.png'>

7\. Run the following command to upload all of your added and committed changes onto **Github**'s **remote repository**.

```git
git push
```

??? info "What is git push?"
    `git push` is used to update a **remote repository** with the changes that have been made on the local file system. It can be thought of as the command for saving a backup of your committed work on the internet.

???+ success
    The **terminal** should return several lines outlining the procedure it took to perform the action. These lines will end with a link to the remote repository, an ID of letters and numbers. All alongside a small graphic showing which branch from your local repository the data was taken from and which branch in your remote repository it went to.

    <img src='/successful-push.png'>

8\. Refresh the page on your **Github repository** in the browser and ensure that all the changes you pushed have made their way across.

???+ success
    If the push was successful you should now see a list of all your project files on **Github**

    <img src='/linked-remote.png'>

## Conclusion

After having completed this section of the instructions, you should be able to

[&#10004; Walk through Github's repository creation process in order to create a remote repository](/docs/remote.md#task-31---creating-a-new-remote-repository)

[&#10004; Run Git scripting language commands in order to link your remote and local repositories.](/docs/remote.md#task-32---linking-the-remote-repository-to-the-local-repository)

If you would like to explore some of the more advanced features **Github** has to offer in terms of managing **remote repositories**, [explore Github's documentation](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features).
