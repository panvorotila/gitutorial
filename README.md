# Git Tutorial

## Initialising
Make directory, cd into directory, and initialise it.

git init

## Adding files

git add filename
git add --all
git add .

Adding procedure is needed after each change.

## Commiting

git commit -m 'My message'

-m adds message in ' '

## Look history

git log

## Generate SSH key

ssh-keygen -t ed25519 -C github-account-email
or
ssh-keygen -t rsa -b 4096 -C github-account-email

## Add key to github
account - settings - SSH and GPG keys - New SSH key
copy key from ./ssh/id_ed25519.pub or ./ssh/id_rsa.pub

to check the key
ssh -T git@github.com

## Connect repository
Go to repository page ang copy ssh
git remote add origin git@github.com:panvorotila/gitutorial.git
origin - standart pseudo

check connection
git remote -v

## Syncronise repository

git push -u origin master(or main)   for the first time

the other times
git push

## Correct commit

Add file to commit
git commit --amend --no-edit

Change message
git commit --amend -m 'Corrected message'
Same in editor
git commit --amend

## Restore files and commits

Delete last commit(s) and restore choosen
git reset --hard 'commit hash to restore'

To unstage file(s)
git restore --staged 'filename or . '

To restore unstaged file
git restore 'filename'

## Look changes

For modified files
git diff

For staged files
git diff --staged
