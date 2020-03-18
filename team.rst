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


Copy the whole castle to make castle1
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

git checkout -b castle1

**Now castle1 contains everything from the master branch.  This command should be executed only once.  Later, when you wish to switch to castle1, using the above command without -b.**


Which branch am I in now?
~~~~~~~~~~~~~~~~~~~~~~~~~~

git branch

**I am now in castle1.**



Edit files, stage and commit
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

**Edit files.**

**Test my edit does not break the program!  This test is really IMPORTANT to make the centralized workflow work.**

git add .

git commit -m "some thoughtful messages"

**Everything happens inside castle1, the original castle won't be affected.  Now castle1 is ahead of the original castle, master.**

**You may spend most of your time in this step.**


Switch back to the master branch
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

git checkout master


Which branch am I in now?
~~~~~~~~~~~~~~~~~~~~~~~~~~

git branch

**I am now in the original castle, master.**


Merge changes in castle1 to master
-----------------------------------

**Now merge the changes I have made in castle1 into master.**

git merge castle1


What has happened in the central repo?
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

**Someone else in my team might have updated the central repo while I was working hard inside castle1. Sync with that updates first.**

git pull origin master

**Push my changes to the central repo so that my teammates can see and incorporate them.**

git push origin master


I have finished today's work
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

I am happy.  Have a good rest.  Castle1, see you tomorrow (git checkout castle1).





-Hui


Last modified on 18 March 2020

