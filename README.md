How to use a git?

-------------------GIT-COMMANDS--------------------
After Setting Up the Git:
Few steps to follow: 
1.) Open a Folder(Ex: App) in Desktop or anywhere
2.) Open it from Git Bash here

Also, go to your editor either notepad++, brackets, atom or VsCode.
I'm using VSCode. In Vs code I will open a folder created. And add some 
basic text in index.html file

In Windows:

1 Check Version: git --version
2 Create a file in the folder: touch index.html
3 Initialize the folder as a git-repository: git init


---------Finding .GitFolder------------
-Go to the folder
-Go to view icons
-Go to options on the right hand side
-Go to view Inside
-Click the show hidden files, folders, and drives
-Scroll little bit down
-Uncheck the hide extensions for the known files types system
-Click Apply and Click Okay
-You should see a .git folder in your App Folder(or the folder you 
created in Desktop before)
-You don't need to know any of the files and folders inside the.git
-That's all

4 In order to use remote git repository, you have to enter your username
and email
- Username: git config --global user.name 'Scanner77'
- Email: git config --email user.email 'bista@gmail.com'

5 Add File: Let's add our index.html to our git-repository
	  :  touch index.html or,
	  :  git add index.html


6 Important: In order to check what's there in staging area we can use
           To check status: git status
	Inside there, you can see something like this:
	Important: Staging Area: The working area where files are not
				 handled by git. These files are also
				 Known as untracked files. The files in
				 Staging area are going to be the part
				 of the next commit, which lets git know
				 what changes in the file are going to
				 occur for the next commit. 

--------------------------
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   index.html

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        app.js
----------------------------

This tells us that index.html has to be committed and should be added to 
staging area. 

7  Delete files: In order to know more about staging.Let's delete a
	index.html file using
	Command: git rm --cached index.html
-----------------------------------------------------
	From the above result, you can see there is 
use "git rm --cached <file>..." to unstage)
        new file:   index.html
	This is the index.html in unstage ready for commit.
--------------------------------------------------------
	After deletion you can check the status of staging. There you
can see we don't have the same output as above. Here, we don't have index
.html
 ----------------------------------------------------------
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        app.js
        index.html

nothing added to commit but untracked files present (use "git add"
 to track)

-----------------------------------------------------

8. ADDING MULTIPLE FILES
	For example: You want to add all the .html files
	Command: git add *.html
	Now,
	Command: git status //you will see index.html
	---------------------------
No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   index.html

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        app.js
-------------------------------------
9. ADD EVERY FILE
	Command: git add .
This command will add every files from the folder
You can : git status to check the status

10. COMMIT: git commit
	It will take you to the new window. In order to start typing
		1.) Press ESC and after that press i from the keyboard
		2.) Remove # in front of the initial commit. Press down 
			to reach there
		3.) Now press ESC and i again and type ':wq'

11. Final Step: Check your status with 'git status' 
	You will have
	----------------
	On branch master
	nothing to commit, working tree clean
	-----------------------------------------



---------------GIT-BRANCHES-------------------

	
After every changes in files.
Do,
- git add .
- git commit -m 'login form'

1.) Git Ignore: This helps us not to add unwanted files even if we did
		'git add .' 
    COMMAND: touch .gitignore
	      Also, create a file you don't want to include

	Here,	
	Open a gitignore in VsCode
	- In .gitignore: type 'log.txt'
	- In log.txt: type 'error logs'
	- In order to ignore the whole directory 'dir' use /dirname 
	in .gitignore
	- *.txt to ignore all the txt files
	
	When you 'git add .' and 'git status'
	You will only see the changes made in .gitignore because
	we have ignored the 'log.txt'

	

-----https://youtu.be/SWYqp7iY_Tc-------

------------------BRANCHES----------------
Suppose your project is like a tree. Also lets suppose you are given 
a task to complete the login of a project. So, the small portion of work
given to you is a branch.

2.) Create a new branch: 
Step 1: git branch branchname(suppose 'login')
Step 2: git commit -m 'another change'
Step 3: git checkout login (now we are in login branch)

You will be redirected to 
bista@Laxyman MINGW64 ~/OneDrive/Desktop/My App (login)


3.) Let's create a new file while we are in this branch
 	1. touch login.html(WRITE something like 'Hi')
	2. git add .
	3. git commit -m 'login form'
	
4.) Switch the Branches: git checkout master
	You will see there won't be the previous 'login.html' in the Folder

5.) Merge: When we finish the project and want to merge branches. Then,
	   COMMAND: git merge login
	It will open up a editor where you can see

-----------------------------------------
Merge branch 'login'
//Added login (You will be entering this line without backslashes)
# Please enter a commit message to explain why this merge is necessary,
# especially if it merges an updated upstream into a topic branch.
#
# Lines starting with '#' will be ignored, and an empty message aborts
# the commit.
---------------------------------------------------
Here, even though you are in the master branch, you can see the login 
branch inside.
If you are working on your own. Then there wont be a need of branches 
because you will be working on all branches as a master



----------------------GIT-LINK-REMOTELY-------------

Adding you local repository to the remote github
1. Create a new repository in Github and do not add a readme File.
2. On the top of a page, you will see a CODE link where you can find
	a link like this : https://github.com/scanner77/FirstCommit.git
3.) Copy it and paste it with
 	git remote add origin https://github.com/scanner77/FirstCommit.git
4.)Check 'git remote'
	: You should have a 'origin'
5.) git push --set-upstream origin master
	This will ask you to login to your remote github
	- Login and authorize
	- Inside the remote github you can see your files

Again,
- git remote
- git remote add origin https://github.com/scanner77/FirstCommit
- git push --set-upstream origin master
That's all you will see the local repo in remote repo



------------IMP LINKS-----------
https://docs.github.com/en/free-pro-team@latest/github/importing-your-projects
-to-github/adding-an-existing-project-to-github-using-the-command-line	
--------------------------------


https://www.theserverside.com/video/How-to-use-the-git-remote-add-
origin-command-to-push-remotely


---------------MAKE-A-README-FILE-----------
- touch README.md to make a read me file
- add your content
- In bash, add the files using git add .
- Commit by using (git commit -m 'Added readme')
- And git push to push it to remote repo
	
