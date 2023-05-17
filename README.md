# Git/Github Practice

Git and Github are the tools you will use most often throughout this course for sharing/backing up code. Git and Github are related but not the same, however you will generally use them together.

- **Git** is a cli tool you use on your local computer to create a 'history' of your files that can be added to or rolled back as necessary. This is called a git repository, or 'repo' for short.

- **Github** is a website that makes it easier to back up your local git repo in the cloud. Git is designed for backing up files to a remote repository, so Github is designed to give you a remote repository for free that you can sync with your local repo. This way, if your own computer suddenly dies the info you saved to github will be unaffected.

## Assignment

### Task
Create a local git repository and push it's contents to a remote repository on Github

### Instructions

#### Create a local Git repo
- Create a new folder on your file system and name it 'hello-world'
- navigate into this folder
- within the folder type `git init` to initialize the git repo. All future work in this folder will not be tracked.
- create a new file in this folder and name it 'hello-world.txt'
- Open this file in VSCode and add some content to it, then save it
- Within the hello-world folder type `git add .` to 'stage' any newly created files (alternatively you can just write `git add hello-world.txt` but you will use `git add .` more frequently)
- type `git status` to see what the status of your git repo is at this point
- type `git commit -m "my first commit"` to 'commit' the currently staged changes. The -m is a flag for adding a message.
- Type `git status` again to see what it looks like now.
- Type `git log` to see a record of all commits so far.

#### Create a remote Github repo
- Sign into Github or create an account if you haven't done so already
- Check the + icon to the left of your profile on the main page
- Choose 'new repository'
- Select yourself as the owner and give the repo the name 'hello-world'
- Make it public. Ignore the other options.
- Click 'Create Repository'
- You will now see a page with complicated instructions, ignore them but keep the page open for later.

#### Linking your local Git repo to your Github repo
- In the page you opened copy the repo url in the Quick Setup section. For me this looks like `https://github.com/AloofBuddha/hello-world.git`
- In your local github repo (hello-world) type:
`git remote add origin <github-url>`
for me this looks like:
`git remote add origin https://github.com/AloofBuddha/hello-world.git`
- Now our local git repo knows about a 'remote' server with the supplied url and names it 'origin' (standard name for your main remote repo)
- type `git push -u origin main` to push the branch main (default branch name) to the remote repo 'origin'. The -u is to set up this connection the first time, in the future you can just type `git push`.
- Go back to your Github repo and refresh the page. You should now see the contents you pushed.

### Bonus

Keep playing with this and pushing files. The only way to learn most things in programming is to play around with it and with Git/Github its good to learn in a consequence free environment, so use this repo for that purpose.

Some things to try out are:
- add a `README.md`. Github will display this file below the contents of the repo like a 'home page' explaining what the repo is for.

- Try creating a new branch locally and pushing it to Github. `main` is the default branch but multiple branches help you to try out different ideas without overlapping with the 'stable version'.

- If you got this far and pushed a new branch to Github you will see Github prompt you to 'Compare & Pull Request'. Follow the prompts to merge the changes you made in your new branch with the main branch. This is how collaboration works with multiple people, but it's an advanced topic you will only start to use in earnest during your group projects at the end of the course.
