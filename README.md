git init REPO_NAME
cd REPO_NAME

git commit --amend
--> überarbeitet letzten commit

git reset --hard
--> macht alle änderungen seit letztem commit rückgängig

**Note** Directories are not tracked, just add a '.keep' file

to ignore files add them to '.gitignore':
...
log/*.log
...

To just add parts to the index we can user 'git add -p' ('-p' as in "patch").

## Disaster Recovery

In case of deleted commits use 'git reflog' and 'git cherry-pick' to recover those commits:
...
git cherry-pick LOST_COMMIT_SHA1
...

**Note** Will be cleaned up once 'git gc' ran.

## Getting information out of history

Use 'git log --oneline --graph' to get condensed log view.

Use 'git blame' to see **last** change for each line.

Use 'git show COMMIT_SHA1' to get detailed information about commit (including diff).

Use 'git log -S' to search in contents of commits