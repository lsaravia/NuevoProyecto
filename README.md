# NuevoProyecto

* Tutoriales de como crear proyectos en git github y Rstudio

## Creating a Pull Request

There are 2 main work flows when dealing with pull requests:

1. Pull Request from a forked repository
2. Pull Request from a branch within a repository

Here we are going to focus on 2.

### Creating a Topical Branch

First, we will need to create a branch from the latest commit on master. Make sure your repository is up to date first using

`git pull origin master`

Note: git pull does a git fetch followed by a git merge to update the local repo with the remote repo. For a more detailed explanation, see this stackoverflow post.

To create a branch, use git checkout -b <new-branch-name> [<base-branch-name>], where base-branch-name is optional and defaults to master. I'm going to create a new branch called pull-request-demo from the master branch and push it to github.

`git checkout -b pull-request-demo`
`git push origin pull-request-demo`

### Creating a Pull Request

To create a pull request, you must have changes committed to the your new branch.

Go to the repository page on github. And click on "Pull Request" button in the repo header.

Pull Request Button

Pick the branch you wish to have merged using the "Head branch" dropdown. You should leave the rest of the fields as is, unless you are working from a remote branch. In that case, just make sure that the base repo and base branch are set correctly.

Head Branch Dropdown

Enter a title and description for your pull request. Remember you can use Github Flavored Markdown in the description and comments

Title and Description

Finally, click on the green "Send pull request" button to finish creating the pull request.

Send Pull Request

You should now see an open pull request.

### Using a Pull Request

You can write comments related to a pull request,

Writing a comment

view all the commits by all contained by a pull request under the commits tab,

Commits tab

or see all the file changes from the pull request across all the commits under the "Files Changed" tab.

Files Changed

You can event leave a comment on particular lines in the code change simply by hovering to the left of a line and clicking on the blue note icon.

Comment in line

### Merging a Pull Request

Once you and your collaborators are happy with the changes, you start to merge the changes back to master. There are a few ways to do this.

First, you can use github's "Merge pull request" button at the bottom of your pull request to merge your changes. This is only available when github can detect that there will be no merge conflicts with the base branch. If all goes well, you just have to add a commit message and click on "Confirm Merge" to merge the changes.

Merge pull request buttonConfirm Merge

### Merging Locally

If the pull request cannot be merged online due to merge conflicts, or you wish to test things locally before sending the merge to the repo on Github, you can perform the merge locally instead.

You can find the instruction to do so by clicking the (i) icon on the merge bar.

Merging Instructions

