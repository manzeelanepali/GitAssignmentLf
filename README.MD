Git Assignment Part 1 

1. Can we have a global .gitignore?
  => yes, we can have global ".gitignore" file that applies to all Git repository on our local machines. when we create a global ".gitignore" file it is stored in our home directory and applies to all the Git repositories on our machines.




2. How can we find the differences between the two  commits?
  => The command "git diff" followed by the commits IDs or references  can be used when we  want to find out the difference between two commits.
  for an example: git diff firstCommit..secondCommit where, "firstCommit" and "secondCommit" are the commit IDs and the .. notation specifies that we want to compare the difference between two commits.




3. write differene between git add and git commit commands?
 =>  when certain changes are made to our file then the command "git add"  takes our code from working directory to the staging area for next commit  whereas " git commit" commands are used to create a new commit with the changes that we have staged using "git add".




4. how to unstage files?
=> The command "git reset" followed by the file name  can be used if we want to unstage  specific file that has already been staged changed using "git add". Its always wiser to check the status using the command "git status" before unstaging.

The command "git reset" can be used to unstage all the changes that we have staged and move back to the working directory.

Incase we have already committed the changes, we can unstage back so we should use the command "git revert" to undo the changes in a new commit.



5. how to revert a commit?
=>the command "git revert" can be used inacase we want ro revert a commit.
We can follow the foloowing steps to revert a command .
  1. use "git log" command to view the commit history.
  2.use "git revert" followed by the id to create a new commit that undoes the changes introduced by the previous commit.

  

6.Difference between revert and reset?
 => Both of the commands are used in the git to undo changes, however both of them works in different ways. 

 "git revert" craetes a new commit that undoes the changes introduced by a previous commit which is to say the original commit remains in the commit history but a new commit is added to undo the changes. Its useful when we want to undo changes but still keep a record of the original commits and its changes. 

 "git reset " on the other hands removes the commits from the commit history entirely.