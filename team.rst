==============
Team
==============

The simplest way to collaborate among 5-10 members
==================================================


Centralized workflow
---------------------

Everyone pushes his upates directly to the central repo.  One has to have write permission to be able to do this.


Clone remote repo to local drive
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

git clone https://github.com/spm2020spring/TeamCollaborationTutorial.git

**This should be done only once.**


Go to the local project folder
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

cd TeamCollaborationTutorial

Which branch I am in now?
~~~~~~~~~~~~~~~~~~~~~~~~~~

git branch


Copy the whole castle to make castle1
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

git checkout -b castle1

**Now castle1 contains everything from the master branch.**


Which branch I am in now?
~~~~~~~~~~~~~~~~~~~~~~~~~~

git branch

**I am in castle1.**



Edit files, stage and commit
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

**Edit files.**

**Test my edit does not break the program!**

git add .

git commit -m "some thoughtful messages"

**Everything happens inside castle1, the orignal castle won't be affected.  Now castle1 is ahead of the original castle.**


Switch back to the master branch
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

git checkout master


Which branch I am in now?
~~~~~~~~~~~~~~~~~~~~~~~~~~

git branch

**I am in the original castle, master.**


What has happened in the central repo
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

**Someone else in my team might have updated the central repo while I was working hard inside castle1. Sync with that updates first.**

git pull origin master

**Now merge change I made in castle1 to master.**

git merge castle1

**Now push my changes to the central repo so my teammates can see them and incorporate them.**

git push origin master



-Hui

