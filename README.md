# Getting Started With Revision Control Software

This GitHub repo is a resource for Software Engineering students to get started with Revision Control Software,
specifically, Git. It also covers some GitHub concepts.

# Learning Resources

##### Suggested Git learning sequence

1. [Git overview video](http://www.youtube.com/watch?v=v40b3ExbM0c): 
   First, watch this to get a quick overview of Git.  
2. [Try Git](https://try.github.io): Now, try this online Git simulation + tutorial 
   to learn Git basics hands-on.
3. Install [SourceTree](https://www.sourcetreeapp.com/) on your Computer.

   > SourceTree comes with Git and a GUI for Git.
4. Follow [this tutorial](https://www.atlassian.com/git/tutorials/setting-up-a-repository) to try git commands
   for real.

   > Tip: [This](https://confluence.atlassian.com/sourcetreekb/using-terminal-in-sourcetree-781398580.html)
   is how you open a Git command line window from SourceTree
5. Now you should be ready to start using Git. Here are two more resources to keep in mind:
   * [The Pro Git Book](http://git-scm.com/book): An online version of probably the
     most popular book on Git.<br>
     Use it as a reference when you want to learn a Git feature in more detail.
   * Use web search to find how to perform a Git task.<br>
     e.g. [How to undo a Git commit](https://git-scm.com/book/en/v2/Git-Basics-Undoing-Things)

# Learning Outcomes

### Use Git on a local repo `[LO-GitLocal]`

* Learn some Git basics by following the [Git learning resources given above](#learning-resources).
* Create a local repo with some dummy content.
* Do some Git stuff on your repo. e.g. 
  * Edit some files in the repo, `stage` the changes, and a `commit`.
  * Add a new file, stage it, and commit.  


### Use Git with a remote repo `[LO-GitRemote]`

Prerequisite: `[LO-GitLocal]`

##### Ex : Clone HelloWorld repo

* Complete the [GitHub HelloWorld tutorial](https://guides.github.com/activities/hello-world/).
* Use SourceTree to clone the HelloWorld repo you created in the previous step.
* Clone the same remote repo to another location of your computer 
  (let's call the two clones `clone1` and `clone2`).
* Do some commits in the `clone1`.  
* `push` the new commits to your remote repo on GitHub.
* `pull` the new commits to your `clone2`.

### Create a PR from fork `[LO-PrFork]`

#### Ex: Create PR against this repo

* [Fork](https://help.github.com/articles/fork-a-repo/) this repo to your GitHub account.
* Clone the fork onto your Computer.
* Add a text file `{YourName}.txt` to the `users` folder e.g. `users/JayYong.txt`. Add some content to the file. 
  Commit the changes. Suggested commit message `Add {YourName}.txt` 
  
  >It's common practice to write commit message in imperative mood.<br>
  e.g. `Add abc.txt` rather than `Added abc.txt` or `Adding abc.txt`.
* Push the commit to your fork.
* Create a PR from your fork to this repo. The PR name should be `Added YourFileName.txt` e.g. `Added JayYong.txt`.
* Wait for the PR to be merged by the repo owner.

### Create a PR using GitHub Flow `[LO-PrGitHubFlow]`

#### Ex: Create a PR using GitHub Flow

* Submit an issue in this repo's issue tracker. Issue name `Add to {YourFileName.txt}` 
  e.g. `Add to JayYong.txt`
* Create a branch in your local clone of this repo with the name `add-to-{YourFileName-txt}` 
  e.g. `add-to-JayYong-txt`
* Switch to the new branch.
* Do some modifications to your text file (in your local repo) and commit the changes in the new branch.
* Push the branch to your fork.
* Go to your fork on GitHub and create a PR for your new branch against the master branch of this repo.
  * PR name: Copy paste the name of the issue you created earlier, including the issue number. <br>
    e.g. `Add to JayYong.txt #123`

    > ![exmaple PR](/images/PrGithubFlow.png)
  * In the PR description, include `Fixes #{issue_number}` e.g. `Fixes #123`<br>
    Reason for the above: It instructs GitHub to close the issue automatically when your PR is merged.
  