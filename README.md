gitguide
========

##### upgrade moodle from v2.6.6 to v2.7.2 ######

$ cd /c/xampp/htdocs/moodlecorelocal
$ git branch -va 

// add remote moodle core repository
$ git remote add moodlecore git://git.moodle.org/moodle.git

// list of remote repositories
$ git remote -v

// list local and remote branches
$ git branch -va

// fetch moodlecore repository
$ git fetch moodlecore

// fetch all tags associated with moodle core
$ git fetch moodlecore --tags

// considering you are on moodle_v2.6.6, checkout a new branch 
$ git checkout -b moodle_v2.7.2

// merge v2.7.2 tag with moodle_v2.7.2 branch
$ git merge v2.7.2

#################################################### 

