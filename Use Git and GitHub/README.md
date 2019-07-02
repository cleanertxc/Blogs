# 1.Finding difference between files
-cd to the path of file
- windows: FC file1_name.xx file2_name.xx
- Mac or Linux: diff -u file1_name.xx file2_name.xx
# 2.Git
- commits: user-created checkpoint 
- `git clone +URL`: Cloning a Repository
- `git log`: show a list of the recent commits with information about them
- `git diff`: compare the two versions of the code in those commits
- `git checkout  + commit ID`:  checkout the commit
- `git init`: create a Git repository
- `git reset`: remove a file from staging area
- `git add`: add files to staging area (the area between the working directory and the repository)
- `git status`: check the status of staging area and working directory
- `git commit`: write a commit message
- `git branch`: create a new branch
- `git gc`: Git’s garbage collection runs
- `git show`: show the difference between commit and its parent
- `git branch -d`: delete the branch's label
- `git merge`: 在merge两个branch之前一定要看当前checkout的branch是不是在打算merge的两个branch中，如果不是的话需要checkout到需要merge的branch上面，否则会把当前checkout但是不打算merge的branch也merge到一起
# 3.GitHub
- `git remote add origin + URL`: create the origin remote
- `git push + remote's name + local branch`: push repository to remote location
- `git pull + remote's name + remote branch`: push repository from remote back to local computer
- `forking`: clone others' repository on your own GitHub account
- `git fetch origin`: 将远程的更新放到本地上
- `fast-forward merging`: 如果merge的两个commit是祖先和子孙的关系，那么可以执行fast-forward merging
