<h2>1. Setup instructions</h2>
You can download Git here: [https://git-scm.com/downloads](https://git-scm.com/downloads)
<br/>install it ....

<h4>Configuring Your Name & Email</h4>
In your terminal, run the following commands to identify yourself with Git:

<br/>
<br/>
<code>
git config --global user.name "Your Name"<br/>

git config --global user.email "your@email.com"
</code>

<h2>2. Repositories</h2>
Create a new repository into github.com 

<h2>3. Initializing a repository</h2>
To do this, create a directory, add a file there & write something on that file.

you can do this from your terminal also.

In the terminal, type:

<code>
mkdir Demo
</code>
<br/>
This command will create a directory (or folder) named Demo.

Change your terminal to the Demo directory with the command:

<code>
cd Demo
</code>

Then enter:

<code>
echo "#Demo" >> README.md
</code>
<br/>

This creates a file named README.md and writes #Demo in it. To check that the file was created successfully, enter:

To see whats inside README.md file : 

<code>
cat README.md
</code>
<br/>
Now we have a file into our working directory/folder.

Now main things for Initializing a repository with the following command:

<code>
git init
</code>

<h2>4.1. Checking the status</h2>

While located inside the project folder in our terminal, we can type the following command to check the status of our repository:

<code>
git status
</code>

<h2>4.2. Staging files</h2>

From the project folder, we can use the **git add** command to add our files to the staging area, which allows them to be tracked.

We can add a specific file to the staging area with the following command:


<code>
git add file.js
</code>
<br/>
To add multiple files, we can do this:

<code>
git add file.js file2.js file3.js
</code>
<br/>
Instead of having to add the files individually, we can also add all the files inside the project folder to the staging area:
<br/>
<br/>
<code>
git add .
</code>


<h2>4.3. Making commits</h2>

 A **commit** is a snapshot of our code at a particular time, which we are saving to the commit history of our repository. After adding all the files that we want to track to the staging area with the `**git add`** command, we are ready to make a commit.

To commit the files from the staging area, we use the following command:
<br/>
<br/>
<code>
git commit -m "Commit message"
</code>


<h2>5. Connect your GitHub repo with your computer</h2>

Now, it's time to connect your computer to GitHub with the command:

<code>
git remote add origin https://github.com/imon0077/GitTutorial.git
</code>

it will ask your github username/password in a separate window.


Now that we have added the remote, we can push our code (i.e., upload our README.md file) to GitHub.com.
use the following command:


<code>
git push -u origin master
</code>

<br/>

Now, go to https://github.com/<your_username>/Demo you will see your changes there.


============================================
<h2>** Others Command **</h2>

## 4.4. Commit history

To see all the commits that were made for our project, you can use the following command:

```bash
git log
```

The logs will show details for each commit, like the author name, the generated hash for the commit, date and time of the commit, and the commit message that we provided.

To go back to a previous state of your project code that you committed, you can use the following command:

```bash
git checkout <commit-hash>
```

Replace `<commit-hash>` with the actual hash for the specific commit that you want to visit, which is listed with the `git log` command.

To go back to the latest commit (the newest version of our project code), you can type this command:

```bash
git checkout master
```

## 4.5. Ignoring files

To ignore files that you don't want to be tracked or added to the staging area, you can create a file called `.gitignore` in your main project folder.

Inside of that file, you can list all the file and folder names that you definitely do not want to track (each ignored file and folder should go to a new line inside the **.gitignore** file).

You can read an article about ignoring files [on this link](https://help.github.com/en/articles/ignoring-files).

# 5. Branches

A **branch** could be interpreted as an individual timeline of our project commits.

With Git, we can create many of these alternative environments (i.e. we can create different **branches**) so other versions of our project code can exist and be tracked in parallel.

That allows us to add new (experimental, unfinished, and potentially buggy) features in separate branches, without touching the '*official'* stable version of our project code (which is usually kept on the **master** branch).

When we initialize a repository and start making commits, they are saved to the **master** branch by default.

## 5.1. Creating a new branch

You can create a new branch using the following command:

```bash
git branch <new-branch-name>
```

The new branch that gets created will be the reference to the current state of your repository.

It's a good idea to create a **development** branch where you can work on improving your code, adding new experimental features, and similar. After development and testing these new features to make sure they don't have any bugs and that they can be used, you can merge them to the master branch.

## 5.2. Changing branches

To switch to a different branch, you use the **git checkout** command:

```bash
git checkout <branch-name>
```

With that, you switch to a different isolated timeline of your project by changing branches.

For example, you could be working on different features in your code and have a separate branch for each feature. When you switch to a branch, you can commit code changes which only affect that particular branch. Then, you can switch to another branch to work on a different feature, which won't be affected by the changes and commits made from the previous branch.

To create a new branch and change to it at the same time, you can use the **-b** flag:

```bash
git checkout -b <new-branch-name>
```

To list the branches for your project, use this command: `git branch`

To go back to the **master** branch, use this command:

```bash
git checkout master
```

## 5.3. Merging branches

You can merge branches in situations where you want to implement the code changes that you made in an individual branch to a different branch.

For example, after you fully implemented and tested a new feature in your code, you would want to merge those changes to the stable branch of your project (which is usually the default **master** branch).

To merge the changes from a different branch into your current branch, you can use this command:

```bash
git merge <branch-name>
```

You would replace `<branch-name>` with the branch that you want to integrate into your current branch.

## 5.4. Deleting a branch

To delete a branch, you can run the **git branch** command with the **-d** flag:

```bash
git branch -d <branch-name>
```





