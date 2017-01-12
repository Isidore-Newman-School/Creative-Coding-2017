# Git 3. Submitting Assignments

If you have installed Git, cloned your repository, and made changes to files in your repo, you are now ready to submit assignments to GitHub using the command line.

## Navigate to Git Directory
Back in Git Bash, begin by changing into the directory where you cloned your GitHub repo (should be where you've saved your work). In my case, that's the "Coding" folder:

```bash
cd ~/Documents/Coding
```

## add
####(i.e. which files to track changes)
To let Git know that you want to track changes of a particular file, we use the "add" command. In this case we want to track changes of all of our files, so we add a "." to signify git should track all files in our working directory:

```bash
git add .
```

## commit
####(i.e. record changes)
Now that we've told Git which files to track, we need to record these changes with the "commit" command. Commits need messages describing what it is that we're committing. Try using descriptive language describing what parts of the code you changed.
```bash
git commit -m "your message goes here"
```

## push
####(i.e. sending files online)
And finally, we need to push these changes from our computer to GitHub so that Ms. deBB can see them. We'll decompose what the "origin master" means in a later tutorial. For now, type:
```bash
git push origin master
```

If everything worked as planned, the online GitHub page should be updated to reflect the changes that you made locally on your computer.


---
* [<- Git 2. Cloning Your Repo](2_cloning.md)
