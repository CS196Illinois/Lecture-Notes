# How to create your Homework Repo

Prerequisite: Create a github account, install git on your local machine.


1) Go to this link: http://tinyurl.com/zfjrygb
You will see the following:

![alt text](https://cloud.githubusercontent.com/assets/7456865/18331697/8d641386-7526-11e6-8c3b-f9700d87bdcb.png)

click "Accept this Assignment".

2) You should have gotten an email that redirects you to a homework repo that was automatically generated:
![alt text](https://cloud.githubusercontent.com/assets/7456865/18331824/6553c48a-7527-11e6-8c87-e7c4834bca47.png)

Go to the link reference at the bottom of the email.

3) You should now have access to the CS196Illinois filled with class-related repositories You should see a repo called "homework-<your github handle>". :
![alt text](https://cloud.githubusercontent.com/assets/7456865/18331875/ad3c0190-7527-11e6-8586-619ef3c36fc2.png)

The first thing you must do with this repo is rename it to "homework-your_netID"
Go to "settings", "options", and "rename" your repository. For example, I would rename my repository to "homework-achung13".

![alt text](https://cloud.githubusercontent.com/assets/7456865/18331699/91a915c2-7526-11e6-90a6-61dba896145e.png)

4) Go to your newly created repo. This is where you will be submitting your homework from now on. First, clone the repo using the command

```
$ git clone <your_repo_url_here>.

```
Your repo url will be inside the homework-<your_netid> repo, in place of mine (its highlighted).

![alt text](https://cloud.githubusercontent.com/assets/7456865/18332017/cf0f4330-7528-11e6-8781-633ab8ba4c96.png)

5) Once you clone, you should have an empty repository in your file system. cd into your homework file. Now pull or download your homework file (the one with the questions) and put it in this empty repository. You should now have your hw1 (or any other hw) file in your repo. Feel free to import any other files that you think might be relevant to your hw. When we activate the autograder, we will specifically look for a file called "hw1.py" (hw2.py, hw3.py, etc ,etc), and so you can even leave your old homeworks in the repo if you wish.

6) complete the homework.

7) When you are ready to submit, we have to go through all of the steps to push your homework file up to the cloud. 

First run the following command to add your new files to the staging environment this command will simply add all untracked files to the staging area:

```
$ git add .
```

Next, you must commit to save your changes to git. Run the following command to save the snapshot of your code to your local git. Your commit message can be anything, it does not matter.:

```
$ git commit -m "<your commit message here.>"
```

Finally, you're ready to push. Run the following command to "push" your new homework file to Github:
```
$ git push origin master
```
Your terminal should look something like this after finishing this process:
![alt text](https://cloud.githubusercontent.com/assets/7456865/18332274/e4bec8de-752a-11e6-88dd-530e7485586a.png)


8) You're done! If you want to make changes to your homework, re-commit and re-push, and your files on the cloud will be updated. Congratulations, you've just version controlled your homework submissions folder! From now on, add all of your finished homeworks to this folder and push to submit. We will take your last commit as your submission. You do not need to delete your old homeworks, but you will not lose points for doing so.





