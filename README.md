# GIT

To assign a commit to an issue and closed use this keywords:
> close, closes, closed, fix, fixes, fixed, resolve, resolves, resolved
> git commit -m "closes #1, closes #2, closes #3; YOUR COMMIT MESSAGE"

> #### When there is a long terminal response, kill with q
> #### When editing a terminal response, star editing with a
> #### When editing a terminal response, stop editing with ESC key
> #### When editing a terminal response, write on command line with :
> #### When editing a terminal response, write with w
> #### When editing a terminal response, write and kill wq

Suggested aliases
> alias.s status --short\
> alias.lg log --graph --abbrev-commit --decorate --format=format:'%C(bold blue)%h%C(reset) - %C(bold green)(%ar)%C(reset) %C(white)%s%C(reset) %C(dim white)- %an%C(reset)%C(bold yellow)%d%C(reset)' --all

<details>
  <summary>
    init
  </summary>
  
  > ## git init
  > ### Create an empty Git repository or reinitialize an existing one
</details>

<details>
  <summary>
    version
  </summary>
  
  > ## git --version/version
  > ### Display version information about Git
</details>

<details>
  <summary>
    help
  </summary>
  
  > ## git --help/help
  > ### Display help information about Git
</details>

<details>
  <summary>
    config
  </summary>
  
  > ## git config
  > ### Get and set repository or global options
  >
  > `git config -l/--list`\
  > List all variables set in config file, along with their values
  >
  > `git config --global`\
  > Write and read only from global `~/.gitconfig`
  > - init.defaultBranch \<branchname> to set the default branch when initializing a repository
  > - user.name "\<name>" to set git username
  > - user.email "\<email>" to set git email
</details>

<details>
  <summary>
    status
  </summary>
  
  > ## git status
  > ### Show the working tree status
</details>

<details>
  <summary>
    restore
  </summary>
  
  > ## git restore
  > ### Restore working tree files
</details>

<details>
  <summary>
    add
  </summary>
  
  > ## git add
  > ### Add file contents to the index
  > `. for adding all files or write specific path`
  >
  > `git add *.c`\
  > Fileglobs can be given to add all matching files
  >
  > `git add dir`\
  > Update the index to match the current state of the directory as a whole
</details>

<details>
  <summary>
    reset
  </summary>
  
  > ## git reset
  > ### Reset current HEAD to the specified state
  > `Write specific path to remove file from staged changes`
  >
  > `git reset <mode> <commit>`\
  > This form resets the current branch head to said commit\
  > \<mode>
  > - --soft: This leaves all your changed files "Changes to be committed"
  > - --mixed: Changed files are preserved but not marked for commit
  > - --hard: Any changes to tracked files in the working tree since \<commit> are discarded. Any untracked files or directories in the way of writing any tracked files are simply deleted.
  >
  > \<commit>
  > - If not specified defaults to HEAD
  > - For one commit behind use HEAD^
  > - For more than one commit behind use HEAD~\<NUMBER>
  > - Use commit hash for specific commit
  
</details>

<details>
  <summary>
    commit
  </summary>
  
  > ## git commit
  > ### Record changes to the repository
  >
  > `git commit -m/--message "msg"`\
  > Use the given msg as the commit message
  >
  > `git commit -a/-all`\
  > Automatically stage files that have been modified and deleted, but new files you have not told Git about are not affected
  >
  > `git commit -am "msg"`\
  > Combination of `-m/--message` and `-a/-all`
  >
  > `git commit --amend -m "msg"`\
  > Rewrite the most recent commit message
</details>

<details>
  <summary>
    log
  </summary>
  
  > ## git log
  > ### Show commit logs
</details>

<details>
  <summary>
    checkout
  </summary>
  
  > ## git checkout
  > ### Switch branches or restore working tree files
  >
  > `git checkout -- .`\
  > Restore all files to current tree
  >
  > `git checkout <branch>`\
  > Switch to said branch
  >
  > `git checkout -b <new-branch>`\
  > Create a new branch named \<new-branch> and switch to it
</details>

<details>
  <summary>
    branch
  </summary>
  
> ## git branch
> ### List, create, or delete branches
>
> `git branch <branchname>`\
> Create branch
>
> `git branch -m/--move <oldbranch> <newbranch>`\
> Move/rename a branch, together with its config and reflog
>
> `git branch -l/--list`\
> List branches 
>
> `git branch -d/--delete <branchname>`\
> Delete a branch
</details>

<details>
  <summary>
    merge
  </summary>
  
  > ## git merge
  > ### Join two or more development histories together
  >
  > `git merge <branch>`\
  > Incorporates changes from the named commits into the current branch.
</details>

<details>
  <summary>
    diff
  </summary>
  
  > ## git diff
  > ### Show changes between commits, commit and working tree, etc
  >
  > `git checkout --cached`\
  > To view the changes you staged for the next commit\
  > --staged is a synonym of --cached
</details>

<details>
  <summary>
    reflog
  </summary>
  
  > ## git reflog
  > ### Manage reflog information
  >
  > Reference logs, or "reflogs", record when the tips of branches and other references were updated in the local repository.
</details>

<details>
  <summary>
    mv
  </summary>
  
  > ## git mv
  > ### Move or rename a file, a directory, or a symlink
  >
  > `git mv <source> <destination>`
</details>

<details>
  <summary>
    rm
  </summary>
  
  > ## git rm
  > ### Remove files from the working tree and from the index
  >
  > `git rm <pathspec>`
</details>

<details>
  <summary>
    tag
  </summary>
  
  > ## git tag
  > ### Create, list, delete or verify a tag object signed with GPG
  >
  > `git tag <tagname>`\
  > Create the tag
  >
  > `git tag -l/--list`\
  > List tags\
  > Running "git tag" without arguments also lists all tags
  >
  > `git tag -a/--annotate <tagname>`\
  > Make an unsigned, annotated tag object
  >
  > `git tag <tagname> <commit>`\
  > The object that the new tag will refer to, usually a commit. Defaults to HEAD.
  >
  > `git tag <tagname> -m/--message <msg>`\
  > Use the given tag message
  >
  > `git tag -d/--delete <tagname>`\
  > Delete existing tags with the given names
</details>

<details>
  <summary>
    show
  </summary>
  
  > ## git show
  > ### Show various types of objects
  >
  > `git show <object>`\
  > The names of objects to show (defaults to HEAD)
</details>

<details>
  <summary>
    stash
  </summary>
  
  > ## git stash
  > ### Stash the changes in a dirty working directory away
  >
  > `git stash list`\
  > List the stash entries that you currently have
  >
  > `git stash push -m/--message "<message>" <pathspec>`\
  >  Save your local modifications to a new stash entry
  >
  > `git stash save "<message>"`\
  >  It differs from "stash push" in that it cannot take pathspec. Instead, all non-option arguments are concatenated to form the stash message
  >
  > `git stash pop`\
  > Remove a single stashed state from the stash list and apply it on top of the current working tree state
  >
  > `git stash show "<stash>"`\
  > Show the changes recorded in the stash entry as a diff between the stashed contents and the commit back when the stash entry was first created
  >
  > `git stash apply "<stash>"`\
  > Like `pop`, but do not remove the state from the stash list
  >
  > `git stash drop "<stash>"`\
  > Remove a single stash entry from the list of stash entries
  >
  > `git stash clear`\
  > Remove all the stash entries
</details>

<details>
  <summary>
    rebase
  </summary>
  
  > ## git rebase
  > ### Reapply commits on top of another base tip
  >
  > `git rebase <branch>`\
  > Reapply commits of current branch to \<branch>
  >
  > `git rebase -i <upstream>`\
  > Reapply commits from HEAD to \<upstream>
  > - If not specified defaults to HEAD
  > - For one commit behind use HEAD^ (keep adding '^' for more commits behind, recommended to use the one below)
  > - For more than one commit behind use HEAD~\<NUMBER>
  > - Use commit hash for specific commit
  >
  > The options in interactive rebase are:
  > (The commits are from top to bottom, oldest to newest respectively)
  > - r, reword: use commit, but edit the commit message
  > - e, edit: use the commit, but stop for amending
  >   - git commit --amend: for update the commit message
  >   - git rebase --continue: when you finish with your changes (you have to add and commit your new changes before continue)
  > - s, squash: use commit, but meld into previous commit (the one in the line before)
  > - s, squash: like “squash”, but discards this commit’s message
</details>

<details>
  <summary>
    clone
  </summary>
  
  > ## git clone
  > ### Clone a repository into a new directory
  >
  > `git clone <repository>`\
  > The (possibly remote) repository to clone from
</details>

<details>
  <summary>
    pull
  </summary>
  
  > ## git pull
  > ### Fetch from and integrate with another repository or a local branch
</details>

<details>
  <summary>
    push
  </summary>
  
  > ## git push
  > ### Update remote refs along with associated objects
  >
  > `git push <tag_name>`\
  > To push a single tag
  >
  > `git push --tags`\
  > To push all tags
</details>

<details>
  <summary>
    remote
  </summary>
  
  > ## git remote
  > ### Manage set of tracked repositories
  > `git remote add <name> <URL>`  
  > Add a remote named \<name> for the repository at \<URL>
  >
  > `git remote prune <name>`  
  > Deletes stale references associated with \<name>. By default, stale remote-tracking branches under \<name> are deleted, but depending on global configuration and the configuration of the remote we might even prune local tags that haven’t been pushed there
</details>
