### GitDiary
My daily learnings of git.

This file is a lil rough. But comes in handy.

**Squash:**

```git rebase -i HEAD~3```  

Squash the last 3 commits.

**Rebase:**

* `git rebase master`

Rebase master into the branch you're checked into.

* ```git rebase --abort```

**Reset:**

* ```git reset <filepath>```

To delete a file that you just added.

* ```git reset --hard HEAD^```

resets branch to when it was last committed.

* `git reset HEAD~3`

This will undo the last 3 commits and take you to the staging area of the 3rd commit.

After that you can make the changes you want and then commit them. Now, it will be considered a single commit.

**Cherry-pick:**

If you've one commit out of sync, you can get it back into sync using cherry-pick. For example, you checked into a commit and then made some changes and committed. Now, this new commit will be out of sync. To get it into sync with the `HEAD`, use this.

```git cherry-pick <commit>```

**Reflog:**

This is a history that will get you back to where you want to be. Unless you haven't used `hard`

`git reflog`

Then to get back to the place in the history you want to be. For example:

 `git reset 'HEAD@{1}' `
 
 **Hooks:**
 
 `bash .git/hooks/pre-commit`
