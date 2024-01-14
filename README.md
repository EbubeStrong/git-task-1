1. Version control is a system that allows you to track changes to files and manage different versions of a project over time. It is particularly useful in collaborative software development, but it can be applied to any context where tracking changes is important. The primary goals of version control are to:

Track Changes: Version control systems keep track of all changes made to files in a project. This includes additions, deletions, and modifications. Each change is associated with a specific user, timestamp, and description.

Collaboration: Multiple developers can work on the same project simultaneously. Version control helps manage concurrent edits, merging changes made by different contributors, and resolving conflicts that may arise.

Revert to Previous States: If a mistake is made or if you need to revert to an earlier version of a file or the entire project, version control makes it easy to roll back changes. This is crucial for maintaining project stability and integrity.

Branching and Merging: Version control systems support branching, which allows developers to create separate lines of development. This is useful for working on new features or fixing bugs without affecting the main project. Later, branches can be merged back into the main line of development.

Traceability: Every change is logged and attributed, providing a clear history of who did what and when. This traceability is valuable 

GitHub Alternatives:
- GitLab
- BitBucket
- Gitea

- Differences between git fetch and git pull
- Git fetch changes from remote repository to local repository: This means that when Git fetch is ran, git contacts the remote repository(origin) and fetches any new changes, branches, or tags that have been added to the remote since the last fetch. THese changes are brought into your local repository, allowing you to see what has been updated on the remote without automatically integrating those changes into your working directory or current branch. This separation allows you to review the changes before deciding to merge them into the local branch. Its a way to keep your local repository aware of the latest developments on the remote without immediately impacting your work.
- While git pull fetches changes from a remote repository like git fetch but also automatically merges those changes into your current working branking: This means that when git pull is ran, git fetches the latest changes from the remote repository(origin), similar to git fetch. But, however, git pull goes a step further by automatically merging those changes into ones current local branch.

- Git fetch is useful for reviewing changes before deciding to merge. Example: git fetch origin: This means git fetch is a Git command that allows you to retrieve changes from a remote repository without automatically merging them into your current working branch. This separation of fetching and merging is beneficial for reviewing changes before deciding to merge.
- While Git pull is essentially a combination of git fetch followed by git merge:
- git fetch - This part of git pull retrieves changes from the remote repository without merging them into your local branch.
It updates your remote tracking branches, such as origin/main or origin/feature-branch, to reflect the latest state of the remote repository.
git merge - After fetching, git pull automatically merges the changes from the remote branch into your current local branch.
If you are on the "main" branch, for example, and you ran git pull origin main, it would fetch changes from "main" on the remote repository and merge them into your local "main" branch.
By combining these two steps into a single command (git pull), you achieve the same result as separately running git fetch and git merge. However, separating these steps using git fetch allows you to review changes before merging, making the process more explicit and giving you greater control over the integration of remote changes into your local branch.

Git rebase is a command in Git that helps you reorganize or clean up your commit history. Instead of merging changes, it allows you to move your changes on top of the latest updates from a branch, creating a more linear and streamlined history.
Start a Feature: You're working on a feature branch, making several commits as you develop.
Fetch Latest Changes: Before integrating your changes, you fetch the latest updates from the main branch (or any branch you want to base your changes on).
Reorganize Your Changes: You use git rebase to reorganize your commits. This involves placing your changes on top of the latest changes from the branch you fetched.
Resolve Conflicts (if any): During the rebase, Git might detect conflicts between your changes and the latest updates. You resolve these conflicts before continuing.
Complete the Rebase: After resolving conflicts, you continue the rebase until it's complete.
Finish and Push: Once the rebase is finished, you can update the remote branch with your cleaned-up history. This often involves force-pushing your changes.
In summary, git rebase is a tool for reorganizing your commits, placing them on top of the latest changes from another branch. It's useful for maintaining a clean and understandable project history.

Git cherry-pick is a Git command that allows you to copy a specific commit from one branch and apply it onto another branch. It's like picking a commit from one branch and placing it on another branch.
