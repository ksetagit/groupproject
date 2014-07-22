# Git Group Project

This group project is part of the course "Version Control with Git" giving at
the KSETA Doktorandenworkshop 2014 in Freudenstadt.
Slides for this Workshop, including further links can be found at:
	https://github.com/ksetagit/kseta-dvcs-talk

## Idea of the project
Documentation of the KSETA Doktorandenworkshop, consisting mostly of Markdown
documents.

Contents:
- Groupname.md 
- Directions.md
- Hotel.md
- Workshops.md
- Activities.md
- People.md

## Common tasks for all groups

0. Clone the example repository.
		git clone https://github.com/ksetagit/groupproject.git

1. Understand the existing history.

		git log

	Maybe try more fancy methods to look at the history like

		git log --graph --abbrev-commit --decorate --date=relative --format=format:'%C(bold blue)%h%C(reset) - %C(bold green)(%ar)%C(reset) %C(white)%s%C(reset) %C(dim white)- %an%C(reset)%C(bold yellow)%d%C(reset)' --all
	or
		gitk --all

2. Create a new feature branch `addgroupname`. Think up a group name and add it
   to Groupname.md. 

2. Put your names in People.md.

2. Rename the branch created in the previous step to `group-$groupname` where
   you replace `$groupname` with your groupname.
   Hint: `git branch -m oldname newname`

4. While you worked on your tasks, another group was added to People.md. This
   change is available in the branch `group-gitmaster`. Merge this branch to
   your `group-*` branch and resolve possible merge conflicts.

### Group specific tasks
Each group has a specific task listed in the following. 

For your task:
- Create a feature branch with a descriptive name
- Commit your changes in this branch
- Push the branch to the central repository
- Merge your branch to the `develop` branch
- Push the new version of the `develop` branch

### Group 1: Directions

1. Add a sentence to Directions.md to describe how to get to the Workshop.

### Group 2: Hotel

1. Briefly describe the hotel in Hotel.md.

### Group 3: People

1. Add your favorite invited speaker to People.md.

### Group 4: Workshops

1. Add a short description to one of the workshops in Workshops.md

### Group 5: Activities

1. Add a sentence to Activities.md and describe one of the soft skill events at
   the workshop.

### Group 6: Benefits of KSETA

1. Name a benefit of KSETA and put it in Benefits.md.

### Group 7: KSETA Slogan

1. Put the KSETA Slogan in Slogan.md.

### Group 8: GitHub

1. Describe the GitHub Logo in GitHub.md.

### Group 9: Favorite Text Editor

1. Name your favorite text editor in Vim.md.

### Group 10: 42

1. Which question has the answer "42"? Put the question in 42.md.


## Provocing conflict

If your merge to the `develop` branch was successful without a conflict, choose
another exercise, which has already been merged, maybe exercise number (10 - Groupnumer).
Without looking at what the other group did, start your work again on the
original `starthere` commit and make changes. When merging to develop, these
changes should lead to a conflict, which has to be resolved manually.


# Advanced

## blame, bisect
When trying to fix a bug in a program, an important step is to find out which
change introduced the bug. There are different approaches and possibilities
to do so.

1. `git blame $filename`
Git blame annotates a file and for each line shows the last commit modifying
that line.

2. `git bisect`

A nice example to understand how git bisect works can be found at
	https://github.com/cayblood/git-bisect-example

## submodules
Submodules can be used to make a project consisting of several git repositories.
This is a common way to work around the issue that git can only checkout the
full repository (instead of svn, which can checkout subfolders).
For a tutorial on how to used submodules, see:
http://joncairns.com/2011/10/how-to-use-git-submodules/


<!--
# vim: set textwidth=80 wrap: 
-->
