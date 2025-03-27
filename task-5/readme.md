# Task 5

## **Interactive Rebasing for Clean Commit History**
    
**Objective:**
    
    - Use interactive rebase to tidy up your commit history.
    
**Requirements:**
    
    - Create a series of commits (some with minor changes or typos in commit messages).
    - Run `git rebase -i HEAD~n` (with `n` representing the number of commits) to squash, reorder, and edit commit messages.
    - Explain how squashing helps in cleaning up commit history before merging into a main branch.


# Steps Followed:

## 1. Creating series of commit

``` git
git add .
git commit -m 'Task-5 nth commit'
```

### Modifying Hello.js

First Commit
![alt text](image.png)

Second Commit
![alt text](image-1.png)

Third Commit
![alt text](image-2.png)

## 2. Seeing commit history

``` git
git log
```
![alt text](image-3.png)

## 3. Reordering commits

Initially,
``` git
git rebase -i HEAD~3
```
![alt text](image-4.png)

### Moving second commit ahead of third commit

Editing git-rebase-todo and saving it.
![alt text](image-6.png)

Merge conflict arised.
![alt text](image-7.png)

Merge Conflict resolved.
![alt text](image-8.png)

``` git
git add .
git rebase --continue
```
![alt text](image-9.png)

![alt text](image-10.png)

![alt text](image-11.png)

### Updated Commit History
``` git
git log
```
![alt text](image-12.png)

## 4. Squashing commits

``` 
git rebase -i HEAD~3
```
### Editing git-rebase-todo

Initally,
![alt text](image-14.png)

After Modifying,
![alt text](image-13.png)

Adding Commit message
![alt text](image-15.png)

Successfully squashed!
![alt text](image-16.png)

``` git
git log
```
![alt text](image-17.png)

## 5. Editing commit message

``` git
git rebase -i HEAD~1
```

Initially,
![alt text](image-18.png)

After Editing and saving it,
![alt text](image-19.png)

### Editing Commit Message

Initially,
![alt text](image-20.png)

After Editing,
![alt text](image-21.png)

Successfully, Completed Editing Commit Message
![alt text](image-22.png)


# Squashing Benefits
    - used to merge the multiple commits into single commit
    - used to maintain clean commit history with logical progression
    - Maintained Commit history helps in code review process
