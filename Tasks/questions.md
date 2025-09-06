### Answer the following questions in you own words.

> It's not necessary that you havee to know and answer all the questions. Just answer the ones
> you know and write in your own words.

1. Give the difference between the remotes - upstream and origin - with an example.
You answer:
Upstream is simply the original repository that you have created a fork from.
Origin - It points to the fork of your repository, simply origin is the name that git gives to the remote repository when you first clone it.

ex-
git fetch upstream - if your original repo has any new commits,we fetch them to local repo , you can merge/rebase later.

git push origin main- you made some changes locally and you want to push them into the remote repository on the github.


2. You have two branches A and B and you have currently made some changes in branch A.
You want to move into branch B but do not want to commit the current changes in branch A.
What will you do?

You answer:
we can use the feature of stashing in git
1st do git stash
       git checkout B
this will temporarily store your changes in branch A and then after your work is completed just do
       git stash pop
this command we can run from any branch(not only on the branch we stashed the changes,so we should be careful).

3. You were assigned a work to implement a feature and create a PR to your organization's remote repository.
For this you made a branch (say A) and made some changes and commited them. Now you moved to some other branch 
(say B) to do some other assigned work. But later you realisd that have to complete the task assigned earlier 
first and commited some changes in branch B which are meant for branch A. How will you use git to bring the 
changes from branch B to branch A?

You answer:
My opinion is to just merge the both branches(only if the commits are related we can follow this method) by using git rebase.

3. What is the difference between fetching changes and pulling changes?

Your answer:
Pull and fetch both bring the updated code to the remote rpository but there is a difference, fetch allows you to see whats new in the remote repo befor we bring to our local repo,
and git pull origin main does the work of bringing those changes into your work and merge with your working repo.
a git pull is equal to git fetch +git merge

4. What does -i flag stand for? What is it's significance in git?

You answer:

5. You are working in an organization that follows very strict guidelines for PRs and commits.
You made three commits in your PR and the maintainer says you were supposed to make a single commit.
What will you do in this case?

You answer:

6. Explain `git merge` and `git rebase` with example(s).

You answer:
Git merge - helps us to combine one branch into another, both branches' commit history will be safe.
-- git checkout main
-- git merge feature

Git rebase - this makes two branches merge on top of one another, only a single line history (linear type) for whole commits.
--git checkout feature
--git rebase main
 also we should also remember not to run this rebase command from the master/main branch because this would make a whole lot of mess.
 There is a reason for people to use this rebase, when we do a git merge there will be a commit made for this merging also , even if that commit didnt make any contribution to the project, and when we use rebase commits like those wont be visible on the linear line(only the real effective ones will be).

7. Write the flow how you create a repository and push changes to it. Also mention the commands used at each step.

You answer: 
First create a folder and follow these steps,
-- git init - this initialises the git into your repository i.e git will start to monitor your files, after doing this there will be a .git folder be created.
-- git add README.md - this file is very crucial because when you so any project this file solely tries to explain your project
-- git commit -m "First commit" -we commit our first addition of readme file
-- git branch -M main - in olden days the main branch was called to be master branch, there were many contraversies that arised, we simply rename the branch master to main(forces to rename).
-- git remote add origin <the link to your forked repo> -
-- git push -u origin main - it means to push the changes in my main branch into the origin(my forked repo), first time while running this command we do this but later on we just do git push
 similarly we can follow this for other files as well

8. How would you prevent a file or folder from getting tracked by git?

Your answer:
There are certain things like API keys and node modules that are not meant to be pushed into github so we use .gitignore file , we mention the file names that git should not track in the .gitignore . Those files contain secret information.

9. You did not implement the step you mentioned in question 8 and now you have committed and pushed your database's
secret key to the github. How will you remove the key from your git's commit history to avoid any misuse?

You answer:
I faced this problem while we were contributing to the google soluttion challenge, by mistake all our api keys were pushed into github, we even were notified through mail. We immediately revoked those keys and deleted those old keys, then we had to clear then evn from the commit history.
we used the following commands:-
git filter-repo --path secret.env --invert-paths
git push origin --force


---