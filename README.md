# Getting Started With Revision Control Software

This GitHub repo is a resource for Software Engineering students to get started with Revision Control Software,
specifically, Git. It also covers some GitHub concepts.

-----------------------------------------------------------------------------------------------------
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

-----------------------------------------------------------------------------------------------------
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
* Create a PR from your fork to this repo. The PR name should be `Add YourFileName` e.g. `Add JayYong.txt`.
* When the PR is ready, add a comment with the text `Ready for review`.

### Create a PR using GitHub Flow `[LO-PrGitHubFlow]`

#### Ex: Create a PR using GitHub Flow

* Submit an issue in this repo's issue tracker. Issue name `Add {YourFullName-Intro.md}` 
  e.g. `Add JayYong-Intro.md`
* Create a branch in your local clone of this repo with the name `add-{YourFullName-Intro-md}` 
  e.g. `add-JayYong-Intro-md`
* Switch to the new branch.
* Create a new file named `users/YourFullName-Intro.md` (e.g. `users/JayYong-Intro.md`) in your local repo.<br>
  Add some info about yourself to the file and commit the changes in the new branch.

  > When adding content to your file, you can use plain text or 
  [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/) format in your file.
  
* Push the branch to your fork.
* Go to your fork on GitHub and create a PR for your new branch against the master branch of this repo.
  * PR name: Copy paste the name of the issue you created earlier, including the issue number. <br>
    e.g. `Add JayYong-Intro.md #123`

    > ![exmaple PR](/images/PrGithubFlow.png)
    
  * In the PR description, include `Fixes #{issue_number}` e.g. `Fixes #123`<br>
    Reason for the above: It instructs GitHub to close the issue automatically when your PR is merged.
* When the PR is ready, add a comment with the text `Ready for review`.

### Follow the centralized workflow [`LO-CentralizedWorkflow`]

When working as a team, you need to be able to write code in parallel and merge the code later.
 There are different workflows you can adopt for this purpose.
 The [centralized workflow](https://www.atlassian.com/git/tutorials/comparing-workflows/centralized-workflow)
 is one of the simplest.

#### Exercise: merge commits using centralized workflow

This is a team exercise.

* These steps are to be done by only one member of the team.
  * Fork this repo to your account, if you haven't done that already. Let's call it the 'team fork'
  * [Give other team members push access to your fork](https://help.github.com/articles/inviting-collaborators-to-a-personal-repository/).

* These steps are to be done by all members.
  * Clone the *team fork* to your computer.
  * While staying in the `master`, add a new file to the repo with the name
  `/centralized/{YourName}.txt`. e.g. `centralized/JamesYong.txt`
  * Add some content into the file and commit it.

* Now follow the centralized workflow (see link given above) to push your changes to the
  team fork.
  * You can ignore references to SVN (in the workflow description). SVN is an older RCS tool.
    You can also ignore the bit about setting up the repo. As you are using a fork, there is no need to set it up.
  * As team member is editing a different file, there should not be any merge conflicts.

### Resolve merge conflicts [`LO-MergeConflicts`]

This is a team exercise.

Prerequisites: `LO-CentralizedWorkflow`

* [Only one member] While staying in the `master` branch,
  create a file `/centralized/{Team-ID}.txt`, commit, and push to the team fork.
* [All members] 
  * Pull the master branch to your clone, add your own name as the first line of the file,
    and commit. Wait for other members to finish this step.
  * Now try to push to the team fork. This is likely to create merge conflicts. Resolving them will give you an opportunity
    to learn how to resolve merge conflicts. More instructions about resolving conflicts
    can be found in the [centralized workflow](https://www.atlassian.com/git/tutorials/comparing-workflows/centralized-workflow)


### Follow the Feature Branch Workflow [`LO-FeatureBranchWorkflow`]

This is a team exercise.

[Step 1: Only one member]
  * Create a GitHub organization for your team.
  * Fork a repo to that org: you can fork this repo or any other repo that you team members were previously working in.
  * Add your team members as collaborators to that fork. Let's call it the *team repo*.

[Step 2: All members]
  * If you have a clone of the team repo on your computer (or a clone of any upstream version of the repo), add the
    team repo as a `remote` of that clone. Otherwise clone the team repo to your computer.

    > **Adding a remote using SourceTree**
    >  1. Choose `Repository > Repository Settings` from the menu.
    >  2. Click `Add`.
    >  3. Copy-paste the team repo URL into the `URL/Path` box. <br>
    >     e.g. `https://github.com/se-edu/rcs.git` (Note the `.git` at the end)
    >  4. Give a suitable name in the `Remote name` box. e.g. `teamrepo`
    >  4. Click `OK`.

  * Now, each member add a feature to the code base using the
   [feature branch workflow](https://www.atlassian.com/git/tutorials/comparing-workflows/feature-branch-workflow)
   also known as the [Github flow](https://guides.github.com/introduction/flow/).



-----------------------------------------------------------------------------------------------------
# Contributors

* [Damith C. Rajapakse](http://www.comp.nus.edu.sg/~damithch) : Project Advisor

-----------------------------------------------------------------------------------------------------
# Contact Us

* **Bug reports, Suggestions** : Post in our [issue tracker](https://github.com/se-edu/rcs/issues)
  if you noticed bugs or have suggestions on how to improve.
* **Contributing** : We welcome pull requests. Follow the process described [here](https://github.com/oss-generic/process)

