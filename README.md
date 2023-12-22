# Git Tutorial

## Initialising
Make directory, cd into directory, and initialise it.

git init

## Adding files

git add filename<br>
git add --all<br>
git add .

Adding procedure is needed after each change.

## Commiting

git commit -m 'My message'

-m adds message in ' '

## Look history

git log

Short version<br>
git log --oneline

## Generate SSH key

ssh-keygen -t ed25519 -C github-account-email<br>
or<br>
ssh-keygen -t rsa -b 4096 -C github-account-email

## Add key to github
account - settings - SSH and GPG keys - New SSH key<br>
copy key from ./ssh/id_ed25519.pub or ./ssh/id_rsa.pub

to check the key<br>
ssh -T git@github.com

## Connect repository
Go to repository page ang copy ssh<br>
git remote add origin git@github.com:panvorotila/gitutorial.git<br>
origin - standart pseudo

check connection<br>
git remote -v

## Syncronise repository

git push -u origin master(or main)   for the first time

the other times<br>
git push

## Correct commit

Add file to commit<br>
git commit --amend --no-edit

Change message
git commit --amend -m 'Corrected message'<br>
Do the same in editor<br>
git commit --amend

## Restore files and commits

Delete last commit(s) and restore choosen<br>
git reset --hard 'commit hash to restore'

To unstage file(s)<br>
git restore --staged 'filename or . '

To restore unstaged file<br>
git restore 'filename'

## Look changes

For modified files<br>
git diff (if needed use previous hash (space) later hash or HEAD)

For staged files<br>
git diff --staged
