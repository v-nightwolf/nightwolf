## Top 50 GIT Interview Questions and Answers for DevOps Roles - Solved

 We have consolidated a list of frequently asked GIT interview questions for Freshers and Experienced DevOps Engineer.
 You will find these questions very helpful in your interviews for DevOps Engineer. Prepare well and All the very best.
<br>

  All the [feedbacks and suggestions](https://nightwolf.in/contribute/) are most welocome.

 {!inpage-ads.md!}

---
       
   Q1) What is a version control system (VCS)?

        Version control systems are software tools that help a team manage changes to source code/documents over time.

   Q2) Why are version control systems (VCS) necessary?

       They allow you to
       1. Keep track of code changes.
       2. Can help team memembers to synchronize the code to the latest version easily.
       3. It helps teams to develop products faster.
       4. Helps teams to collaborate with each other easily.
       5. It acts as a backup for your code base.

   Q3) What are distributed version control systems (DVCS)?

       Distributed revision control synchronizes repositories by transferring patches from peer to peer.
       There is no single central version of the codebase instead, each user can download a working copy and full
       change history.  Hence not requiring to be connected to the server all the time.
       Example : GIT

   Q4) What are centralized version control systems (CVCS)?

       It is a version control where there is a single central repository hosted on a server. This server is expected
       to have the latest code and expects all its clients to contribute by being connected to the server always.

   Q5) How does git maintain the data internally.

       Git mainly uses three different types of objects to hold information about a repository
       BLOB  binary form of the actual data
       TREE  It contains pointers to the objects
       COMMIT  Commit object contains information about the author, date, ha

   Q6) Can git be used locally without using GIT server or any SAAS providers like

       git, bitbucket &etc
       Yes, if a person is willing to work on the project alone he can use git to maintain the state of the project.
       However the full potential of git is unutilized.

   Q7) How do you find a list of files impacted with a particular commit hash?

       git diff-tree -r {hash}

   Q8) What is a conflict in git. Is it necessary?

       A conflict in git arises when branches are merged with new commits which has changes on same file(s). In cases
       like this git cannot take precendence of changes hen

   Q9) What is the difference between git pull and git fetch

       Git fetch will download new commits from a remote repository to a local repository
       git pull does the same as git fetch and also merges the same into your local working files

   Q10) How are conflicts solved?

       The files in conflict must be edited and fixed. Then add the resolved files by running
       1. git add .
       2. git commit

   Q11) What is the command that defines the author email to be used for all the commits performed by the current user?

        # git config global user.email <email>

   Q12) GIT belongs to which generation of version control tools

       3rd

   Q13) What is GIT stash?

       When changes are made to the working directory but you don t want to comattempting to recreate a clean
       working directory. GIT stash is used where all changes in working directory and Index are are pushed into
       a stack.

   Q14) How do you create a new branches

        # git branch <branch name>

   Q15) How do you checkout to a particular branch

        # git checkout 

   Q17) What languages were used to build the git?

        C was the major language althought few parts were also written using shell, perl, tcl and python

   Q18) What is git config?

       git config allows you to configure git installation.
       example includes setting user name , password, email etc

   Q19) What is git clone?

       Git clone lets users to copy an exising git repository that resides in the server.
       It is the easiest way that a new developer can start using and contributing to the project

   Q20) What is branching?

       Branching is analogus to a storyline on which changes are made. The changes can resides in different 
       branches so that each branch can make changes independent of each other.

   Q21) What is the command line environment used to perform git operations?

        # git bash

   Q22) What is git cherry pick?

       cherry pick allows you to pick a particular commit from a branch and insert to another branch. This is
       different from git merge in that, git merge will bring in all commits from branches while cherry pick 
       picks a specific commit only.

   Q23) How to return a commit that has been pushed and made open?

       # git revert HEAD~2.HEAD

   Q24) What is gitflow workflow?

       It is a workflow that can be used to maintain large projects and it mainly consists of
       The master branch is always ready for live release with everything production-ready.
       The Hotflix branches help in quick patching of production releases.
       The Develop branch helps in merging of all feature branches and also performs all the tests.
       The Feature branch implies a unique branch for every new feature. The feature branch could be pushed to
       the development branch just like their parent branch.

 {!inpage-ads.md!}

   Q25) What is the syntax for rebasing ?

        # git rebase [new-commit]

   Q26) What are git webhooks?

       When plannning to cascade/notify new activities on git server to a different tool like jenkins,
       git webhook is used. the webhook contains information about the activity (ex: push on the server).

   Q27) What is git instaweb

        Its a command that helps in directing a web browser and running a web server with an interface to the
        local repository.

   Q28) What hash is used in git ?

        sha1

   Q29) sha1 is now considered unsecured. does that mean git is under threat.

        No. since git uses sha1 to only hash data to compare files/maintain state agit

   Q30) What is the max number of heads can be used in git?

        unlimited

   Q31) How many characters are used in sha1 name

        40 chars

   Q32)What is a commit message.

       It is the message assigned to a commit made. When a commit is made a hash is assigned automatically but for
       humans it becomes difficult to make anything out of this hash at later point of time. Hence a commit message
       is assigned along for his future reference

   Q33)Name few graphical git clients

       git cola, git gui

   Q34)What is git diff?

       Git diff represents the changes between the commits and changes between working tree and commits.

   Q35)What is git pull origin?

       The command git pull origin master tells git to perform a pull operation (download a copy of repository) where
       the origin represents the server url (alias) and master is the name of the branch

   Q36) What is gitlog?

       It is basically a command that can be executed when it comes to finding the history of a project according to
       the date, changes made, the developer who handled it and usefulness of the same.

   Q37) How can a developer update his changes to the git server.

       Perform git push from the branch he is currently checked out to.

   Q38) How do you make git not to consider few files/directories track changes.

        need to add them in .gitignore file
 
   Q39)What is the difference between git add . git add -all

       They are same

   Q40) What is git bisect?

       Its the command that uses a binary search algorithm to find which commit þÿa bug.Before the bug is 
       introduced into the commit, the commit is referred

   Q41) What is git stash drop?

       Its the command that helps you remove the last entry made to the stash list or it can also help to eliminate
       any stash entry.

   Q42) How do you delete a branch locally?

        git branch -d <branch name>
 
   Q43) What is git clean?

        It cleans a repository by removing the files that are not currently tracked by git recursively.

   Q44) What is git pop?
 
        It is the command that helps you retrieve the changes pushed on the stack.

   Q45) What is git fork?

       A fork is a copy of a repository. Forking a repository allows you to freely experiment with changes without
       affecting the original project. Generally open source projects follow fork workflow to allow users to 
       contribute to the project.
       
---

[<h3 style="text-align: center;font-family: cursive;"> GIT Cheat Sheet </h3>](git_cheatsheet.md)

---
<br>
{!footer.md!}
