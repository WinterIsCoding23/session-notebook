### Git `branch` commands

| command                      | functionality                        |
| ---------------------------- | ------------------------------------ |
| `git switch -c <branchname>` | create a new branch and switch to it |
| `git switch <branchname>`    | switch branches                      |
| `git branch`                 | list your branches                   |
| `git branch -a`              | list all branches (local and remote) |
| `git branch -d <branchname>` | delete a branch                      |

## Git pull requests

GitHub offers us **pull requests** (PR) which we can use as a convenient way to request reviews of
the work on a feature branch.

A pull request is a request to merge one branch into another branch. Other developers review the PR
and suggest changes. If a pull request is approved we can merge the feature branch into the main
branch.

### Basic Workflow for a pull request

1. Create a new branch with `git switch -c <branchname>`.
2. Make changes to the code / write your code fpr the feature.
3. Push the changes and the new branch with `git push -u origin <branchname>` (after you have done
   this once you can use `git push` for this branch)
4. Create a pull request on GitHub from the new branch into main
5. Share the pull request with your team
6. Review the pull request, implement changes if needed, push again to update the pull request until
   it gets approved
7. Merge the pull request into main
8. Don't forget to `git pull` inside the main branch on your local machine
9. Delete the new branch on GitHub and locally

<img src="assets/git-basics-branching-workflow.png" width="900">