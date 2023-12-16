#Git Tutorial

##Initialising
Make directory, cd into directory, and initialise it.

git init

##Adding files

git add filename
git add --all
git add .

Adding procedure is needed after each change.

##Commiting

git commit -m 'My message'

-m adds message in ' '

##Look history

git log

##Generate SSH key

ssh-keygen -t ed25519 -C github-account-email
or
ssh-keygen -t rsa -b 4096 -C github-account-email

##Add key to github
account - settings - SSH and GPG keys - New SSH key
copy key from ./ssh/id_ed25519.pub or ./ssh/id_rsa.pub

to check the key
ssh -T git@github.com

##Connect repository
Go to repository page ang copy ssh
git remote origin git@github.com:panvorotila/gitutorial.git
origin - standart pseudo

check connection
git remote -v

##Syncronise repository

git push