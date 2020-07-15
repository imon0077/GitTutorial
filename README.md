1. Setup instructions
You can download Git here: [https://git-scm.com/downloads](https://git-scm.com/downloads)
installing it ....

### Configuring Your Name & Email
In your terminal, run the following commands to identify yourself with Git:

git config --global user.name "Your Name"
git config --global user.email "your@email.com"

2. Repositories
Create a new repository  into github.com 

3. Initializing a repository
To do this, create a directory, add a file there & write something on that file.

you can do this from your terminal also.

In the terminal, type:
mkdir Demo

This command will create a directory (or folder) named Demo.

Change your terminal to the Demo directory with the command:
cd Demo

Then enter:
echo "#Demo" >> README.md

This creates a file named README.md and writes #Demo in it. To check that the file was created successfully, enter:

To see whats inside README.md file : 
cat README.md

Now we have a file into our working directory/folder.

Now main things for Initializing a repository with the following command:

git init

## 4.1. Checking the status

While located inside the project folder in our terminal, we can type the following command to check the status of our repository:
git status

## 4.2. Staging files

From the project folder, we can use the **git add** command to add our files to the staging area, which allows them to be tracked.

We can add a specific file to the staging area with the following command:

git add file.js

To add multiple files, we can do this:
git add file.js file2.js file3.js

Instead of having to add the files individually, we can also add all the files inside the project folder to the staging area:
git add .

## 4.3. Making commits

 A **commit** is a snapshot of our code at a particular time, which we are saving to the commit history of our repository. After adding all the files that we want to track to the staging area with the `**git add`** command, we are ready to make a commit.

To commit the files from the staging area, we use the following command:

git commit -m "Commit message"


5. Connect your GitHub repo with your computer

Now, it's time to connect your computer to GitHub with the command:

git remote add origin https://github.com/imon0077/GitTutorial.git


it will ask your github username/password in a separate window.


Now that we have added the remote, we can push our code (i.e., upload our README.md file) to GitHub.com.
use the following command:

git push -u origin master

Now, go to https://github.com/<your_username>/Demo you will see your changes there.







