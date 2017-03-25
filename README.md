# intro-to-git
Pomona WAC-M intro to git workshop Spring 2017

## Contributing to a Repository

### Forking a repository onto your GitHub
1. Log into account
2. Go to the [intro-to-git repo](https://github.com/madelinezug/intro-to-git)
3. Click "fork". After forking you should now have a intro-to-git repository on your account, with a URL `https://github.com/your-account-name/intro-to-git`

### Putting it onto your local machine
1. Click on "Clone or download" and copy the URL. It should have the format `https://github.com/your-account-name/intro-to-git.git`
2. In terminal, navigate to the directory that you want to put this project in, using the `cd` command
3. Clone the repository onto your machine: `$ git clone URL`, where you replace `URL` with the one you got from step 1

### Modifying the project and putting the changes onto GitHub
1. Navigate into the directory: `$ cd intro-to-git`
2. Enter `git status` to see how git interprets your directory before you make any modifications. It should say something like "nothing to commit, working directory clean"
3. Edit the `name.txt` file to include your name
4. Now we put the changes onto GitHub

	```
	$ git status                        # Shows that you've modified `name.txt`
	$ git pull                          # Fetches and merges any changes that has been made in the GitHub repository onto this local copy
	$ git add .                         # Adds all your modifications
	$ git status                        # Shows that you've added your modifications
	$ git commit -m "Modified name.txt" # Commits your modifications
	$ git status                        # Shows that you've committed your modifications
	$ git push origin master            # Pushes from your local (origin) to the master branch "GitHub repository"
	```

### Creating a pull request
1. Go to the original [intro-to-git repository](https://github.com/madelinezug/intro-to-git)
2. Click on "New pull request"
3. Add information as necesssary
4. Wait for Maddie to either accept or reject your request

## Starting a project from scratch

There are many different ways to do this, and this is just one of the ways!

### Create a new repository on GitHub 
1. Go to your GitHub
2. Click on the "Repositories" tab
3. Click on the "New" tab
4. Enter in a repository name. Don't initialize the repository with a README, don't add `.gitignore`, and don't add a license
5. Click "Create repository"

### Putting that repository onto your local computer
1. Get the URL of the repository. It should be of the format `https://github.com/your-account-name/your-project-name`
2. In terminal, navigate to the directory you want the project to be in
3. Make a directory with the same name as your GitHub repository: `$ mkdir your-project-name`
4. Go into that directory: `$ cd your-project-name`
5. Initialize git version control for this directory: `$ git init`
6. Establish a connection between this directory and your GitHub repository: `$ git remote add origin URL`, where `URL` is the one you copied in step 1
7. Verify the connection `$ git remote -v`. Both `fetch` and `push` should have the URL by it

If you make changes to this project, see the section [Modifying the project and putting the changes onto GitHub](###Modifying the project and putting the changes onto GitHub) on how to push these changes onto its corresponding GitHub repository.