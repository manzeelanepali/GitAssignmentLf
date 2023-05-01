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


 Git Assignment 2 (part1)
 1. write the difference between the fetch and pull command?

 => Both fetch and pull are Git commands that allow you to update your local repository with changes from a remote repository. However, they have some differences in how they work:

fetch downloads new commits from a remote repository but does not integrate them into your local branch. It updates the "remote-tracking branches", which are references to the state of the remote branches, but it does not modify your local working directory. This means that after a fetch, you need to manually merge or rebase the changes into your local branch to incorporate them.

pull is a combination of fetch and merge. It downloads new commits from the remote repository and automatically integrates them into your local branch by merging them. This means that a pull will update both the remote-tracking branch and the local working directory with the latest changes from the remote repository.

In summary, fetch is a safe operation that downloads changes from the remote repository without modifying your local working directory, while pull is a more aggressive operation that updates your local working directory with the latest changes from the remote repository.


2. how to handle the merge conflict?

=>
A merge conflict happens when Git is unable to automatically merge changes from two different branches. This usually occurs when two different branches have modified the same lines of code, or when one branch has deleted a file that another branch has modified.

To handle a merge conflict, follow these steps:

First, ensure that your local repository is up to date by fetching the latest changes from the remote repository: git fetch origin.

Next, switch to the branch that you want to merge into: git checkout branch-to-merge-into.

Start the merge process: git merge branch-to-merge-from.

If Git encounters a merge conflict, it will mark the conflicting files in your working directory. Open these files in your code editor and search for the conflict markers, which will look something like this: <<<<<<< HEAD and >>>>>>> branch-to-merge-from.

Edit the conflicting code to resolve the conflict, keeping the changes that you want to keep and removing any unnecessary code. Save the file.

After resolving all conflicts, stage the changes by using git add for each modified file.

Once all conflicts are resolved and changes are staged, commit the changes with a commit message explaining the resolution of the conflict: git commit -m "Resolved merge conflict."

Finally, push the changes to the remote repository: git push origin branch-to-merge-into.

By following these steps, you can successfully resolve any merge conflicts that occur in your Git workflow