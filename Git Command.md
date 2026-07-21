$ git config --global user.name "Hassan Ibrahim"
$ git config --global user.email "hassansafita97@gmail.com"
$ git config --list               (to see the configuration that I have made)

..........................................................

$ git init                                       (to initialize a repo file, mandatory)
$ git status                                     (to see the status of the file I have, whether it is tracked or not)
$ git ls-files -s                                (show me all the files that exist in the index or to see the staging area)
$ find .git/objects/ -type f                     (to see if there is anything in the repo area)
$ git add file.txt                               (transform the file from untracked to tracked: indexing)
$ git cat-file -t (SHA)                          (to see the type of the file using SHA-->this command is used after running $git ls-file -s)
$ git cat-file -s (SHA)                          (to see the size of the file using SHA--> this command is used after running $git ls-file -s)
$ git cat-file -p (SHA)                          (to see the content of the file using SHA--> this command is used after running $git ls-file -s)
$ git commit -m "initial commit"                 (first version of the project)
$ git log                                        (to see the history that I have)
$git commit -am  "description"                   (to make the add and commit in one command)

* **Note: Every commit will create 3 objects (blob, tree, rapper)**
* **HEAD: represents where you are in WT now**
..............................................................

$ git diff (filename)                                 (to see the difference between WT \& Index)
$ git diff --staged                                   (to see the difference between index \& Repo)
$ git config --global core.editor "vim"               (to specify an editor to read files: here, if I typed ($git commit) I can type what I want)
$ git log --online                                    (to see the history that I have in brief)
$ git show (SHA)                                      (to see what I did in this commit and what I had updated)
$ git diff (SHA1)..(SHA2)                             (to see the difference between two commits)

.............................................................

$ git rm --cashed <filename>                                  (to untrack a specific file)
$ git restore <filename>                                      (to undo the file modification and ignore the updates from index removal)
$ git restore --staged <file>                                 (to make the file from staged to untagged but keep the updates)
$ git commit --amend                                          (to update the last commit message)
$ git reset HEAD~(number)                                     (to go backward [as the number] to the staging area)
$ git reset --hard HEAD~(number)                              (to go backward [as the number] to the WT area)
$ git reflog                                                  (to see what happened to SHA & what I removed)
$git reset --hard HEAD@{number}                               (to go forward to what I had before remove)

................................................................

$ git tag  -a  v2.0   -m   "version 2.0 of the file"           (now I can show/display as per the version: $git show v2.0)
$ git branch <branch name>                                     (create new branch)
$ git branch                                                   (to list the branches)
$ git switch testing                                           (to switch to another branch)
$ git merge testing                                            (to merge testing into master)
$ git branch  --merged                                         (show me the branch that merged into master)
$ git branch -d  testing                                       (delete the testing branch)

..................................................................

$ git clone <remote_repo> <local_repo>            (to clone the repo from one location to another location and rename it)
$ git remote                                      (show me all the remotes that I have)
$ git remote -v                                   (show me all the remotes that I have with more information)
$ git branch -r                                   (show me the remote branch and where I am on any branch)
$ git remote add <shortname> <URL>                (to add another remote)
$ git fetch <remote_name>                         (to get all the updates, references, objects from the remote but will not merge that)
$ git push -u origin feature                      (create branch feature in remote and sync with it in remote the update I made in local)
$ git branch -v                                   (to see the branches that I have)
$ git pull origin                                 (fetch and merge in one command)
....................................................................
