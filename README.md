# Project Summary
---
Get familiar using git and GitHub

We'll go through three short exercises to get you comfortable with the workflow you'll be using
with git in throughout this course.

Our first exercise will show you the steps you'll take when you first start a project using git.
  - Creating a repository
  - Linking a remote `repository` to the `repository` on your local computer
  - Pushing changes to GitHub

The second exercise will show you the steps you'll take with most of the projects in this course.
You'll ...
  - `fork` the BoomCamp repository
  - Link your local repository to your `fork`
  - Push your changes up to GitHub

The third exercise will have you mimicking the workflow that you would typically encounter working
on a software development team. You'll...
  - Create a repository
  - Create a `branch` off of the `master` `branch`
  - Make changes to the newly created `branch`
  - Create a `pull request` from your new `branch` to the `master` `branch`

### Exercise 1:
---
#### Step 1:
**Summary** - We will create a repository on GitHub

**Instructions**
  - Go to [GitHub](https://github.com)
  - Sign in to GitHub
  - Create a new `repository`
    > ![New Repo Example](images/github_new_repo.png)

  - Give the `repository` any name you like, make the `repository` public
  - Do **NOT** initialize the `repository` with a README
---

#### Step 2:

**Summary** - We will connect a **local** `repository` to the **remote** `repository` we just created
on GitHub.

**Instructions**
  - Create a folder named `myFirstRepo`.
  - Go into that folder.
  - Inside the folder create a file called `bands.txt`.
  - Add a name of a band to the `bands.txt` file.
  - Save your `bands.txt` file.
  - Open a terminal window.
  - `cd` into your project folder.
    > ```bash
    > cd ~/myFirstRepo
    >
    > # your repository may be in a different location
    > # than this example
    > ```

  - Run the following commands inside the `myFirstRepo` directory
    > ```bash
    > git init
    > ```
    > The `init` command creates a hidden folder and files that enable git to start tracking changes
    > within your project directory. many `git` commands will not work if they are not run within a
    > directory that git has been initialized within.

    > See the official documentation for more info: https://git-scm.com/docs/git-init

  - Run
    > ```bash
    > git remote add origin $YOUR_REPOSITORY_URL
    >
    > # Replace $YOUR_REPOSITORY_URL with the actual URL your repository is located at.
    > # You can find your repository URL by navigating to
    > # the repository you made earlier on GitHub and copying the address.
    > ```
    > ![Repository URL example](images/repository_url.png)
    >
    > The `remote add` command takes two arguments a **$REMOTE_NAME**, in this case it is named `origin`
    > this is by convention in git. We are telling our local repository that it _originates_ from the
    > remote repository url we specified as the second argument.
    >
    > Doing this we are linking the repository on our computer to the repository located on GitHub,
    > this will allow us to _push_ changes to the remote repository when we are ready.
    >
    > See the official documentation for more info: https://git-scm.com/docs/git-remote

#### Step 3:

**Summary** - We push some code from our local repository to our remote repository on GitHub.

**Instructions**

  - Open a terminal window and navigate into the `myFirstRepo` directory
  - Run
    > ```bash
    > git status
    > ```
    > This will show what files have been changed. This is how we determine what we've changed and
    > what we want to **add** to a **commit**.
    >
    > See the official documentation for more information: https://git-scm.com/docs/git-status

  - Run
    > ```bash
    > git diff
    > ```
    > This will show the code line-by-line that has changed. This is a good way to inspect changes
    > at a more granular level.
    >
    > See the official documentation for more information: https://git-scm.com/docs/git-diff

  - Run
    > ```bash
    > git add bands.txt
    > ```
    > This adds the `bands.txt` file and all of the changes made to it into the **staging** area. Files
    > added to the staging area are not yet **committed** but their state has been saved, this will
    > make more sense after the next command.
    >
    > See the official documentation for more information: https://git-scm.com/docs/git-add

  - Run
    > ```bash
    > git commit -m "This is a commit message"
    > ```
    > This takes all of the file(s) in the **staging** area and creates what is called a **commit**.
    > A commit is a _snapshot_ of your code. The `commit` command is what tells `git` to create that snapshot.

  - Run
    > ```bash
    > git push origin master
    > ```
    > This _syncs_ or _pushes_ the commits you've made to your local repository to your remote repository.
    > Be sure to include `origin master`, this tells `git` which _branch_ you want to push to, and it
    > will create the branch if it does not already exist in the remote repository.

  - Go to the repository on GitHub and see the updates made to your repository.









