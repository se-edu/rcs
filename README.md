# Getting Started With Revision Control Software

This GitHub repo is a resource for Software Engineering students to get started with Rivision Control Software, 
specifically, Git. We also cover some GitHub concepts.

#Learning Resources

Suggested Git learning sequence:

* [Git overview video](http://www.youtube.com/watch?v=v40b3ExbM0c): 
  First, watch this to get a quick overview of Git (for beginners and intermediate users)  
* [Git demo](http://www.youtube.com/watch?v=Y9XZQO1n_7c&feature=youtu.be&t=1m33s): Next, watch this short Git demo from 
  C0dePorn that shows some basic Git commands in action. If the video above was too abstract for you, 
  this view will show you some concrete Git commands in action. This video also describes how to install Git.
* [Try Git](https://try.github.io): Now, try this online Git simulation + tutorial to learn Git basics hands-on
* [Git commands tutorial](https://www.atlassian.com/git/tutorial/git-basics): 
  (from Atlassian) - If you didn’t like the simulation above, try this tutorial instead.
* [The Pro Git Book](http://git-scm.com/book): An online version of probably the
  most popular book on Git. Use this as a reference to learn Git usage in more detail.
* Once you know the basic terminology, try a web search to find how to perform and Git task.<br>
  e.g. [how to undo a Git commit](https://git-scm.com/book/en/v2/Git-Basics-Undoing-Things) 

# Learning Outcomes

### Create a Pull Request online `[LO-PrOnline]`

##### Ex : Do GitHub HelloWorld Tutorial

Complete the [GitHub HelloWorld tutorial](https://guides.github.com/activities/hello-world/). 

### Clone a repo `[LO-Clone]`

##### Ex : Clone HelloWorld repo

* Install [SourceTree](https://www.sourcetreeapp.com/) on your Computer. <br>

  > SourceTree comes with Git and a GUI for Git.
* Use SourceTee to clone the HelloWorld repo you created in the previous exercise.
* Do some Git stuff on your clone. e.g. 
  * Edit some files in the repo, `stage` the changes, and a `commit`.
  * Add a new file, stage it, and commit.  
  * `push` the new commits to your repo on GitHub.

### Create a PR from fork `[LO-PrFork]`

#### Ex: Create PR against this repo

* Fork this repo to your GitHub account.
* Clone the fork onto your Computer.
* Add a text file `{YourName}.txt` to the `users` folder e.g. `users/JayYong.txt`. Add some content to the file. 
  Commit the changes. Suggested commit message `Added {YourName}.txt`
* Push the commit to your fork.
* Create a PR from your fork to this repo. The PR name should be `Added YourFileName.txt` e.g. `Added JayYong.txt`.
* Wait for the PR to be merged by the repo owner.

### Create a PR using GitHub Flow `[LO-PrGitHubFlow]`

#### Ex: Create a PR using GitHub Flow

* Submit an issue in this repo's issue tracker. Issue name `Additions to {YourFileName.txt}` 
  e.g. `Additions to JayYong.txt`
* Create a branch in your local clone of this repo with the name `additions-to-{YourFileName-txt}` 
  e.g. `additions-to-JayYong-txt`
* Switch to the new branch.
* Do some modifications to your text file (in your local repo) and commit the changes in the new branch.
* Push the branch to your fork.
* Go to your fork on GitHub and create a PR for your new branch against the master branch of this repo.
  * PR name: Copy paste the name of the issue you created earlier, including the issue number. <br>
    e.g. `Additions to JayYong.txt (#123)`
  * In the PR description, include `Fixes #{issue_number}` e.g. `Fixes #123` 
    Reason for the above: It instructs GitHub to close the issue automatically whe your PR is merged.
  