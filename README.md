# git-crypt-test

This repo will contain sample for use of git crypt


First we need to install git-crypt on system along with git.

in an new repo we need to init

git-crypt init


then we need a key 

git-crypt export-key /path/to/key

then we need to add a .gitattributes file which will contain all the filters which will define which file needs to be encrypted. eg 

* filter=git-crypt diff=git-crypt
.gitattributes !filter !diff


And we are done we just need to unlock our repo using 

git-crypt unlock /path/to/key


then we can add our files like .key files and git add ., git commit  and git push

And your files are encrypted.


