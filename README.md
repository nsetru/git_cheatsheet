gitguide
========

##### upgrade moodle from v2.6.6 to v2.7.2 ######

$ cd /c/xampp/htdocs/moodlecorelocal
$ git branch -va 

add remote moodle core repository <br />
$ git remote add moodlecore git://git.moodle.org/moodle.git

list of remote repositories <br />
$ git remote -v

list local and remote branches <br />
$ git branch -va

fetch moodlecore repository <br />
$ git fetch moodlecore

fetch all tags associated with moodle core  <br />
$ git fetch moodlecore --tags

considering you are on moodle_v2.6.6, checkout a new branch  <br />
$ git checkout -b moodle_v2.7.2

merge v2.7.2 tag with moodle_v2.7.2 branch  <br /> 
$ git merge v2.7.2

###########################

####git branching####
set local repository to track remote repository <br />
$git branch --set-upstream-to origin/< branch_name >

delete branch locally <br /> 
$ git branch -d branch_name

delete remote branch <br />
$ git push origin :remote_branch_name

########################

####git merging####

$ git merge tag_name/branch_name

abort merge <br />
$ git merge --abort

resolve merge conflicts <br />
$ git mergetool

########################

####git commit####

commit to git with no message <br />
$ git commit --allow-empty-message -m ''

amend commit message <br />
$ git commit --amend -m "New commit message"

revert commit <br />
$ git revert < commit_id >

list of files committed <br />
$ git diff-tree --no-commit-id --name-only -r <commit_id>

list of local and remote branches <br />
$ git branch -va

revert back changes staged/unstaged <br />
$ git checkout < filename >
 --OR--
revert all changed files <br />
$ git  checkout .

checkout branch while tracking remote repo <br />
$ git checkout -b < branch_name > origin/< remote_branch_name >

cherry pick single commit <br />
$ git cherry-pick < commit-id >

#########################

####upgrade a test_moodle plugin and moodle to 2.x.x####

----upgrade moodle to 2.x.x----- <br />

checkout master from current repository <br />
$ git checkout master

pull all changes from remote master (in case current repo is out-of-date) <br />
$ git pull origin master

$ git checkout -b upgrade_moodle_2.x.x origin/master

add remote moodle repository <br />
$ git remote add moodle git://git.moodle.org/moodle.git

$ git fetch moodle

$ git fetch moodle --tags

$ git merge v2.x.x

----upgrade complete---

----After upgrading moodle, its time to upgrade test_moodle plugin-----

checkout a new feature branch off the < upgrade_moodle_2.x.x > <br />
$ git checkout -b feature_test_moodle_plugin

add remote test_moodle plugin repository <br />
$ git remote add test_moodle git@samnishsoftwares.com:test_moodle.git

$ git fetch test_moodle

$ git pull test_moodle

$ git merge test_moodle/feature_test_moodle_2

--------------------------------------------------------------------


