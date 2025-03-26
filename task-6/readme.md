# TAsk 6
## **Stashing Changes for Context Switching**
    
**Objective:**
    
    - Learn how to use Git stash to save uncommitted work temporarily.
    
**Requirements:**
    
    - Make changes in your working directory without committing.
    - Use `git stash` to save these changes.
    - Switch branches, perform some work, then return and reapply your stashed changes with `git stash pop`.
    - Optionally, demonstrate how to view and manage multiple stashes using `git stash list` and `git stash drop`.

# Steps Followed:

## 1. Created Hello.js file

### Hello.js
![alt text](./images/image.png)

### Add and Commit to Git
``` git
git add .
git commit -m 'Task-6 init'
```

## 2. Create new branch and make some changes and stash it

``` git 
git checkout -b stash-branch
```

### Modify Hello.js file
![alt text](./images/image-1.png)

### Without commit, stash the changes
``` git
git stash
```
![alt text](./images/image-2.png)

### After stash, Hello.js file
![alt text](./images/image-3.png)


## 3. Switch to Main branch and modify Hello.js

``` git
git checkout main
```

### Modified Hello.js file
![alt text](./images/image-4.png)

### Add and commit to git

``` git
git add .
git commit -m 'Task-6 initial commit'
```

## 4. Switch to stash branch and reapply stashed changes

``` git 
git checkout stash-branch
```
### Stash history
``` git
git stash list
```
![alt text](./images/image-5.png)

### Reapply stashed changes using `git stash pop` in stash-branch
``` git
git stash pop
git diff
```
![alt text](./images/image-7.png)
![alt text](./images/image-8.png)

### Add and Commit to Git
``` git
git add .
git commit -m 'Task-6 Stashed commit'
```

### Now, Two different branched have two different statements in Hello.js

#### main branch
![alt text](./images/image-10.png)


#### stash branch
![alt text](./images/image-9.png)


With the help of stashing, changes made in one branch is maintained without commit and can be reapplied after making changes to another branch.