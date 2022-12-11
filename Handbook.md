# handbook
This handbook is a summary of solutions to the problems I encoutered. It includes my understanding on specific knowledge, the way to make your code much neater and useful resources etc.

## Git Version Control Commands
Code Version Control is a great approach to organize your and team's code.

### Create Repository
- git init
- git clone ***

### Submit
- git add FILE1 FILE2 FILE3
- git commit -m 'NAME'

### Branch
- List all branches: git branch
- Create Branch: git branch ***
- Switch Branch: git checkout ***
- Create and switch to a new branch: git checkout -b ***

### Merge Branches
初始状态(位于iss53)分支。
![image](https://user-images.githubusercontent.com/95418272/206886659-cf656fa8-b8e5-4c8b-b08b-7ca1b9ae5df6.png)
提交完所有的修改，切换回主分支，并创建新分支。
git checkout master
git checkout -b hotfix
![image](https://user-images.githubusercontent.com/95418272/206886701-462cb903-46c8-419d-aef1-ecdf69e1c2d0.png)
新分支上做了一些修改，**先切换回主分支，然后和主分支合并。**
git checkout master
git merge hotfix
![image](https://user-images.githubusercontent.com/95418272/206886717-891ab47a-f09a-493c-8dff-731a01d3b010.png)
删除已经和主分支合并的分支，切换回原来的工作分支。
git branch -d hotfix
git checkout iss53

### Check Status
- git status
- See submitting history: git log

### Delete File
- Delete undesired files in cache: git rm --cached ***
- 删除log目录下以.log结尾的文件(\+文件名或*+.后缀): git rm log/\*.log
