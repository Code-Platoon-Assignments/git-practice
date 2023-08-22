# Git Practice

## Assignment

### Task

Create a local git repository and get familiar with some of the essential sub-commands

### Instructions

#### Create a local Git repo

#### Part 1: Make a repo and make some commits

1. Create a new folder on your file system and name it 'hello-world', then navigate inside

2. Within the 'hello-world' use the right `git` subcommand to initialize this folder as a git repo

3. Create a new file in this folder and name it 'hello-world.txt'. Open this file in VSCode and add some content to it, then save it.

4. Create another file 'my-poem.txt' and write an excepional poem (or not)

5. Use the appropriate `git` subcommand to 'stage' these newly created files (either individually or all at once)

> Remember, use `git status` between `git` commands to get a sense of what you just did and whether you and `git` are on the same page.

6. Use `git log` to confirm your commit was recorded

7. Create some more changes (any you want, new files or changing existing ones, `git` only cares that there are changes) and make another commit. Confirm again with `git log`

#### Part 2: Create a feature branch

1. Use the appropriate command to create (and checkout) a new branch off of main called `experiment`

2. Make some more changes in this branch and commit them. Try to make at least 2 new commits in this branch.

3. Use `git log` to confirm the history of this branch

#### Part 3: Merging a feature branch

1. Use the right command to checkout `main` again. Use `git log` to confirm it doesn't contain any of the work on the `experiment` branch

2. Use the right command to merge the changes from `experiment` into `main`. Remember, the `git merge <branch>` command merges the changes _from_ `<branch>` _into_ the branch you are currently on, so make sure you are on `main` first!

3. Use `git log` to confirm all the changes have been integrated into the current branch

4. **BONUS**: if you got this far, try using the below version of `git log` to see a commit history view that helps with visualizing branching:

```sh
git log --oneline --graph
```

Ultimately Github will be the preferable tool for tracking such changes visually, but it's good to know a primitive version of this exists right within `git`.

### Cheatsheet

Some important commands we learnt so far include:

- `git init` - make a new local repo

- `git status` - get feedback on the current state of your repo

- `git add <filename>` - add a specific file to git for staging

- `git add .` - add files to git for staging

- `git commit -m '<message>'` - commit staged files as a discrete unit of 'work' that git tracks

- `git log` - print the commit history

- `git checkout -b <branchname>` - create a new branch with the given name

- `git checkout <branchname>` - switch to the branch with the given name

- `git merge <branchname>` - merge the latest changes from the branch with the given name into the branch you are currently on
