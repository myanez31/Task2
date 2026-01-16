# Read Me

## Branches

### main
Stable production branch
### dev
Integration branch for features
### feature1, feature2, feature3
Experimental branches with multiple commits
### hotfix
Branch with a commit ready for main

## Learning Summary
In this assignment I learned about the following operations:
merge, rebase, squash, and cherry-pick. 

Merge will merge two branches. More specifically it will merge another 
branch into your current branch. One example is if I'm currently on branch
'feature2' and I call 'git merge dev', the dev branch will get merged into 
feature2 branch. Conflicts are identified and displayed to the user to be manually
updated. Once conflicts are resolved, the user stages the updated files using 'git add 
<filename>' and finishes the merge process with 'git commit'. During the merge 
process history is preserved showing on the log  showing that the branches had 
diverged and subsequently merged.

