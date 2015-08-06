# git-etc-add-package

For those running Gentoo Linux and keeping /etc in a git repo this script will
help to prepare one commit per updated package after updating your system.

## Usage

It assumes /etc is already under version control.

  git etc-add-package FILENAME
  git diff --cached
  git commit

The script will automatically find all other files belonging to the same package
and stage all for commit. Inspect the changes using `diff --cached` and then
`git commit` as usual.
