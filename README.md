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

Rebase takes all commits on the current branch and replays the commits onto the latest
commit of the branch that is being called. When on 'feature2' branch, if I call 'git rebase dev',
commits on feature2 will be temporarily removed and feature2 will be updated to point to dev's
last commit. All feature2 commits will then be replayed sequentially after dev. Dev branch will
remain the same before rebase was executed, but feature2 will now include all the code
that was in the dev branch with the added commits from feature2. In this example, dev and feature2
are no longer diverged. Until if and only if dev has a new commit that is not in feature2 and feature2
also has a new commit that is not in dev.

Squash allows you to combine multiple commits into one commit by rebasing a predetermined amount
of commits prior to 'HEAD'. It allows for messy commits to be consolidated into one commit with
one helpful descriptive commit message.

Cherry-picking allows you to incorporate hot fixes or critical fixes into the current branch you're on.
Cherry-picking enables users to choose specific commits to incorporate by including the hash code.
Hash codes could be found by executing 'git log --oneline' and finding the hot fix branch commit hash
code. Cherry-picking a commit incorporates those changes into the current branch and creates a new commit.
The proper workflow after a cherry-pick into a main branch would be to update the dev branch to ensure it's
up-to-date.

### What I observed in the git history for feature1 vs feature2 vs feature3
