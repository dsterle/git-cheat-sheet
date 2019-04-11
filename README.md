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