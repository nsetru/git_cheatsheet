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

#################################################### 

###### set local repository to tract remote repository ######

$git branch 

########################

###### git merging #####

$ git merge tag_name/branch_name

$ git merge --abort

delete branch locally <br /> 
$ git branch -d branch_name

delete remote branch <br />
$ git push origin :remote_branch_name


####git commit####
commit to git with no message <br />
$ git commit --allow-empty-message -m ''

amend commit message

