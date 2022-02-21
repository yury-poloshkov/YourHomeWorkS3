# Work with GIT
*To check your knowledge and become highly proficient, follow the link https://learngitbranching.js.org/. This application (trainer) helps you to comprehend the huge capacity of branching as well as to practice Git work.*

__Initial Configuration__

The first thing you should do when you install Git is to set your user name and email. Run the following into the terminal:

*git config --global user.name "Your name"*

*git config --global user.email "Your email"*

## __Git Basics__
*Notes:*

*To clean your terminal, enter **clear**.*

_To call previously entered commands press ↑._

*To insert an image, save the image to your folder. Enter this [Photo](Beach.jpg)

**NB: Add file .gitignore and insert a name of your file with photo/picture to this file.** 

## File creation and initialization.

1) Open folder.
2) Create a file.
3) Enter *git init* in terminal.

__Your folder will be added as a repository.__

4) Enter *git add file name* in terminal. 

__Now your file will be tracked by Git.__

Hint: start to write two-three letters of your file name and then press the button tab, the program will find the right file.

To check the status, enter *git status* in terminal.

NB: Do not forget to save your file (ctrl+S) and make a commit. Tracked files may be in three states: unmodified, modified and indexed (ready to be committed).

## Commits

In order to make a commit:
* save your file **ctrl+S.**
* enter *git add file name* in terminal.
* enter *git commit -m "Your commit"* in terminal.

In order to change the last commit run *git commit -amend -m "New commit"* in terminal.

__Commit deleting:__

For local repository – run *git reset* – this command will delete everything to the previous commit.

For remote repository – run *git revert* – this command will create new commit. It contains inverse transformation.

## How to switch between commits

In order to switch between commits, enter _git checkout commit's hash_ in terminal.

Commit's hash you can find in terminal when you enter *git log*.

Hint: It does not need to write down full hash of needed commit, it is enough to copy and paste 4-6 symbols.

To return to the latest commit, enter *git checkout master* in terminal.

## Change log

In order to see the history of your commits, enter *git log* in terminal.

There is a command to see short display (without author and date) of the commits. You need to enter _git log --oneline_ in terminal.

To see __all commits from all existing branches__ run *git log --oneline --all* in terminal.

## Difference between files

In order to see the difference between files, enter *git diff* in terminal. To quit, press Q.

NB: You can see this difference before you add changings in Git. (_git add_)

## Branching

In order to create a new branch, enter *git branch branch name* in terminal.

Enter *git branch* in terminal to see all branches you have.

To switch between branches, enter *git checkout branch name*.

In order to add a branch to master, switch to master and enter *git merge branch name* in terminal.

To delete your branch run *git branch -d branch_name* in terminal.

To make your branch the main/master run *git branch -M branch_name* in terminal.

## Work with Git Remote Repository. 

NB: 
1) GIT is a local program. All your repositories are located on your local machine.
2) GitHub is a remote service.  Your repository pushed to GitHub is available for viewing worldwide.

**How to get (to clone) a remote repository to your local machine**

1)	Follow the link https://github.com/.
2)	In the search box, enter the key words. You will find the lists of repositories (it does not need to create an account on GitHub). Find the desired repository and open it. You will see a CODE green button. Copy URL.
3)	Open Git (VS Code). Create a folder. Make an initialization. Enter git clone URL in terminal. 

Result: the program will copy the remote repository from GitHub. 

*Notes: 
Git command - *mkdir folder name* to create a new folder.
Git command - *cd folder name* to move to the selected folder (cd means change directory).
Git command - *cd ..* to go up a level.*

**How to push your local repository to GitHub**

1) Create an account on GitHub (Sign in).
2) Create a local folder. Make an initialization. Create a file. Add and commit it.
3) Create a new repository in your account on GitHub. In the upper right corner, press button +, new repository, repository name, create repository (chose to involve your local repository).
4) In local terminal enter the following commands:
-	*git remote add origin [url from GitHub]*
-	*git branch -M main*
-	*git push -u origin main* (on your first push you need to make friends your local repository with GitHub, follow the instruction).

__Changing in file pushed to GibHub__  

If you have already pushed your repository to GitHub and would like to make any changes, enter these commands in your local terminal:

-	*git add*
-	*git commit*
-	*git push*

Result: You will find all your changes on GitHub.

In case you make changes from other PC or right in GitHub, you should save your changes and pull it to your local machine. 

__Fork and Pull request__ 

If you want to contribute to somebody’s project (repository) and you do not have the rights to do it, you can make a Fork, do your changes in new branch and then make a Pull Request. The Fork is the replica. Make the following:

-	Find the needed repository on GitHub and the button Fork.
-	Clone the repository to your local machine (*git clone url*).
-	Make a new branch (*git branch name*)
-	Make some changes (*git add, git commit*)
-	Push your changed repository to GitHub (*git push*)
-	Make a new Pull request on GitHub.