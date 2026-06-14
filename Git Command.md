$ git config --global user.name "Hassan Ibrahim"
$ git config --global user.email "hassansafita97@gmail.com"
$ git config --list               (to see the configuration that I have made)

..........................................................

$ git init                                                             (to initial a repo file mandatory)
$ git status                                                        (to see the status of the file I have if it is tracked or not)
$ git ls-files -s                                                   (show me all the files that existed in Index or to see the staging area)
$ find .git/objects/ -type f                             (to see if there is any thing in the repo area)
$ git add file.txt                                               (transform the file from untracked to tracked: indexing)
$ git cat-file -t (SHA)                                       (to see the type of the file using SHA-->this command used after run $git ls-file -s)
$ git cat-file -s (SHA)                                       (to see the size of the file using SHA--> this command used after run $git ls-file -s)
$ git cat-file -p (SHA)                                      (to see the content of the file using SHA--> this command used after run $git ls-file -s)
$ git commit -m "initial commit"                 (first version of the project)
$ git log                                                             (to see the history that I have)
$git commit -am  "description"                   (to make the add and commit in one command)

* **Note: Every commit will create 3 object (blob, tree, rapper)**
* **HEAD: represent where you are in WT now**
..............................................................

$ git diff (filename)                                                 (to see the difference between WT \& Index)
$ git diff --staged                                                    (to see the difference between index \& Repo)
$ git config --global core.editor "vim"               (to specify an editor to read files: here if I typed ($git commit) I can type what I want)
$ git log --online                                                     (to see the history that I have in brief)
$ git show (SHA)                                                     (to see what I did in this commit and what i had updated)
$ git diff (SHA1)..(SHA2)                                        (to see the difference between two commit)

.............................................................

$ git rm --cashed <filename>                  (to untrack a specific file)
$ git restore <filename>                          (to undoing the file modifying and ignore the updates from Index remove)
$ git restore --staged <file>                    (to make the file from staged to untagged but keep the updates)
$ git commit --amend                              (to update the last commit message)
$ git reset HEAD~(number)                     (to go backward [as the number] to the stagging area)
$ git reset --hard HEAD~(number)         (to go backward [as the number] to the WT area)
$ git reflog                                                  (to see what happened to SHA & what I removed)
$git reset --hard HEAD@{number}        (to go forward to what I had before remove)

................................................................

$ git tag  -a  v2.0   -m   "version 2.0 of the file"                    (now I can show/display as per the version: $git show v2.0)
$ git branch <branch name>                                                     (create new branch)
$ git branch                                                                                  (to list the branches)
$ git switch testing                                                                     (to switch to another branch)
$ git merge testing                                                                     (to merge testing to master)
$ git branch  --merged                                                              (show me the branch that merged into master)
$ git branch -d  testing                                                              (delete the testing branch)

..................................................................

$ git clone <remote_repo> <local_repo>                            (to clone the repo from location to another location and rename it)
$ git remote                                                                               (show me all the remotes that I had)
$ git remote -v                                                                           (show me all the remotes that I had with more information)
$ git branch -r                                                                            (show me the remote branch and where I am any branch)
$ git remote add <shortname> <URL>                                 (to add another remote)
$ git fetch <remote_name>                                                   (to get all the update, reference, objects from the remote but will not merging that)
$ git push -u origin feature                                                     (create branch feature in remote and sync with it in remote the update I made in local)
$ git branch -v                                                                           (
$ git pull origin                                                                          (fetch and merge in one command)
....................................................................