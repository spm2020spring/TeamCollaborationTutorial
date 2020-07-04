==============
Team
==============

The simplest way to collaborate among 5-10 members
==================================================


The Centralized workflow
-------------------------

Everyone pushes his updates directly to the central repo.  One has to have write permission to be able to do this.
With this approach, we do not need actions like Pull Request.
Therefore, you should be a **responsible** individual who **always** tests your code to make sure it does not break the program before you commit.


Clone remote repo to local drive
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

git clone https://github.com/spm2020spring/TeamCollaborationTutorial.git

**This should be done only once.**


Go to my local project folder
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

cd TeamCollaborationTutorial

Which branch am I in now?
~~~~~~~~~~~~~~~~~~~~~~~~~~

git branch


Copy the whole castle to make castle2
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

git checkout -b castle2

**Now castle2 contains everything from the master branch.  This command should be executed only once.  Later, when you wish to switch to castle2, using the above command without -b.**


Which branch am I in now?
~~~~~~~~~~~~~~~~~~~~~~~~~~

git branch

**I am now in castle2.**



Edit files, stage and commit
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

**Edit files.**

**Test my edit does not break the program!  This test is really IMPORTANT to make the centralized workflow work.**

git add .

git commit -m "file changed: specific messages (what & why)"

**Append your group information in each commit message.  Why?  If your name and student number are not included, you won't get credit for that commit.**

**Everything happens inside castle2, the original castle won't be affected.  Now castle2 is ahead of the original castle, master.**

**You may spend most of your time in this step.**


Switch back to the master branch
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

git checkout master


Which branch am I in now?
~~~~~~~~~~~~~~~~~~~~~~~~~~

git branch

**I am now in the original castle, master.**


Merge changes in castle2 to master
-----------------------------------

**Now merge the changes I have made in castle2 into master.**

git merge castle2


What has happened in the central repo?
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

**Someone else in my team might have updated the central repo while I was working hard inside castle2. Sync with that updates first.**

git pull origin master

DON'T BREAK THE BUILD.  Double check that your code does not break the program before you send it to the central repo.

**Everything seems good.  Push my changes to the central repo so that my teammates can see and incorporate them.**

git push origin master


I have finished today's work
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

I am happy.  Have a good rest.  Castle2, see you tomorrow (git checkout castle2).


The feature-branching workflow
-------------------------------

In contrast to the centralized workflow in which every developer writes the central repo's master directly, the idea of the feature-branching workflow is that each developer pushes 
their feature branch to the *central* repo, and creates a Pull Request for merging their feature into the master branch in the central repo. 

Of course, the Pull Request will undergo code review.

In this way, while interacting with the central repo, developers do not touch the central repo's master directly (even if they have write access), making master less vulnerable to bad pushes that may break the build.

Note: You should use this workflow in this course: http://lanlab.org/course/2020s/spm/.

Clone remote repo to local drive
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
git clone https://github.com/spm2020spring/TeamCollaborationTutorial.git

This should be done only once.

Go to my local project folder
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
cd TeamCollaborationTutorial

Copy the whole castle to make chinese-castle 
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
git checkout -b chinese-castle

Now chinese-castle contains everything from the master branch.
This command should be executed only once. 
Later, when you wish to switch back to chinese-castle, using the above command without -b.

Making a branch is a cheap operation.  
We should do this for each small feature or bugfix.
We can make a branch called chinese-castle-made-by-wood.  We can make a branch called chinese-castle-made-by-stone.


Work on the branch chinese-castle
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

All of your changes related to this feature (or bugfix) must happen in chinese-castle.

You edit files, and test that your editing does not break the program.

git add .

git commit -m "file changed: specific messages (what & why)"

Append your group information in each commit message. Why? If your name and student number are not included, you won't get credit for that commit.

Everything happens inside chinese-castle.

You may spend most of your time in this step.


Update the branch chinese-castle with the central repo's master branch
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

git pull origin master

Now I am still in chinese-castle.  I do this primarily to make sure I will be ahead of the central repo's master branch.


If there are no conflicts (in most cases), this command will finish silently.  Otherwise, you must resolve any conflicts before you push.
A conflict occurs when a line you changed in your local branch has already been changed by other people since your last sync with the central master repo.

IMPORTANT: You should execute the above command before you push your commits to the remote central repo, to make sure your branch is "clean".


Push chinese-branch to the central repo
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

git push origin chinese-castle


Initialize a Pull Request
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

I want other people see my changes and incorporate my changes (if they are satisfactory).

Initialize a Pull Request using the web interface on Github.


Another developer could work on a german-castle and pushes his german-castle to the central repo in a similar way.


References
----------------------

Michael Ernst. (2017).  How to create and review a GitHub pull request?  https://homes.cs.washington.edu/~mernst/advice/github-pull-request.html

Kedar Vijay Kulkarni. (2019).  How to create a pull request in GitHub?  https://opensource.com/article/19/7/create-pull-request-github
 

-Hui


Last modified on 22 March 2020

