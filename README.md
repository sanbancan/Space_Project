Git Diff vs Git Diff --staged
Simple notes with an easy example
Why do we use these commands?
When we make changes in a file, Git lets us review those changes before we save them in a commit. The two commands, git diff and git diff --staged, help us check what has changed. The main difference is whether we have added the changes to the staging area or not.
1. git diff
The git diff command shows the changes we have made in our files but have not staged yet. In simple words, it shows the changes that are still waiting for git add.
Example:
•	Open space.txt.
•	Add a new line: Saturn has beautiful rings.
•	Save the file, but do not run git add yet.
•	Run the command below:
git diff
Git will show the line you added because the change is in your working directory, but it has not been moved to the staging area.
2. git diff --staged
The git diff --staged command shows the changes that we have already added to the staging area using git add, but have not committed yet. It helps us review exactly what we are about to save in the next commit.
Example:
•	Stage the file using git add space.txt.
•	Now run the command below:
git diff --staged
Git will show the changes that are currently staged and ready to be committed.
3. What is the difference?
Command	What it shows	When to use it
git diff	Changes that have not been staged yet.	Before git add.
git diff --staged	Changes that have been staged but not committed.	After git add and before git commit.
4. See how they fit into the Git workflow
1.	1. Make changes — Edit a file, for example space.txt.
2.	2. Check unstaged changes — Run git diff to see what you changed before staging.
3.	3. Stage the changes — Run git add space.txt.
4.	4. Check staged changes — Run git diff --staged to review what is ready for the commit.
5.	5. Commit the changes — Run git commit -m "Update space information".
5. Commands to practise
git status
git diff
git add space.txt
git diff --staged
git commit -m "Update space information"
Remember this simple difference
git diff: What have I changed but not staged yet?
git diff --staged: What have I staged and am about to commit?
Extra tip: git diff --staged and git diff --cached are two names for the same command. They show the same staged changes.
