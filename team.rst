==============
Team
==============

The simplest way to collaborate among 5-10 members
==================================================


Centralized workflow
---------------------

Clone remote repo to local drive
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

git clone https://github.com/spm2020spring/TeamCollaborationTutorial.git

Everyone pushes his upates directly to the central repo.

- cd TeamCollaborationTutorial

- git status

- git checkout -b castle1  # make a copy of the original castle

- Edit files, stage and commit.  Everything happens inside the copy, the orignal castle won't be affected.

- git checkout master  # go back to master branch

- git pull origin master  # update with the central repo's content.  Why? Because someone else might have updated the central repo while you were playing inside castle1.

- git merge castle1  # merge castle1's stuff to master

- git push origin master # push local changes to the central repo.


Hui

