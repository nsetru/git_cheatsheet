gitguide
========
http://yakiloo.com/getting-started-git-flow/

##### upgrade moodle from v2.6.6 to v2.7.2 ######

$ cd /c/xampp/htdocs/moodlecorelocal

$ git branch -va 

<i>add remote moodle core repository</i> <br />
$ git remote add moodlecore git://git.moodle.org/moodle.git

<i>list of remote repositories</i> <br />
$ git remote -v

<i>list local and remote branches</i> <br />
$ git branch -va

<i>fetch moodlecore repository</i> <br />
$ git fetch moodlecore

<i>fetch all tags associated with moodle core</i>  <br />
$ git fetch moodlecore --tags

<i>considering you are on moodle_v2.6.6, checkout a new branch</i>  <br />
$ git checkout -b moodle_v2.7.2

<i>merge v2.7.2 tag with moodle_v2.7.2 branch</i>  <br /> 
$ git merge v2.7.2

<i> check all modified files</i> <br />
$ git status

<i> add/stage all modified file/files </i><br/>
$ git add < file_name >
--OR--
$ git add .

<i> commit all staged files to git </i> <br />
$ git commit -m "commit message"

<i> check commit-ids with commit messages </i> <br />
$ git log -n

<i> push all commit to remote </i> <br />
$ git push origin HEAD

###########################

####git branching####
<i>set local repository to track remote repository</i> <br />
$ git branch --set-upstream-to origin/< branch_name >
<br />
$ git branch --set-upstream-to=origin/<branch> moodle_v2.6.7

<i>delete branch locally</i> <br /> 
$ git branch -d branch_name

<i>delete remote branch</i> <br />
$ git push origin :remote_branch_name

<i>Rename current branch locally</i><br />
$ git branch -m < newname >

<i> Rename different branch </i> <br />
$ git branch -m < old_branch_name > < new_branch_name >


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

<i>Abort cherry-pick </i><br />
$ git cherry-pick --abort

<i> Amend latest commit </i> <br />
$ git add < modified_file_name >
$ git commit --amend
save :wq 

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

####git tag####

<i>list available tags</i> <br />
$ git tag -l

<i> checkout a new branch from tag</i> <br />
$ git checkout -b < new_branch_name > < remote_tag_name >

-- -- --- --- --- ---


