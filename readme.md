# Development process

Here's a quick summary:

* Assign issues you're working on to yourself.
* Work on a branch per issue, something like `issue-number-name-of-feature`. One branch per feature/bug, please.
* When you're finished, mark the PR for review by labelling with "Review &amp; Merge".
* Get someone to review your code, and assign to them

### Git Flow

If you're new to them here are a few steps to help you get started:

* Ensure you're in the `development` branch. `git checkout development`
* Ensure this branch is up to date. `git pull`
* Create a new branch `git checkout -b issue-number-name-of-feature`
* Add your files.  `git add .` or if you've changed a lot of files use `git add -p` to be prompted about small chunks of code
* Commit your files. `git commit -m "Adds name of feature`
* Push the branch to Github. `git push`
* Submit a new pull request to the team and request a review
* Merge PR into `development` and make sure the branch is deleted

### Production deployment
Once the code is ready for production, merge to master doing the following

* Create a new branch off of master, `git checkout -b issue-number-name-of-feature-master`
* Then cherry pick the PR that was merged into development `git cherry-pick -m 1 <PR hash>`
* Push the branch to Github
* Submit a new pull request and assign to one of the other developers
* Merge PR into `master` and make sure the branch is deleted

### Handling messes/mistakes
* If your local repo has many unwanted changes and want to clear them all use `git reset --hard`
* If you want to save some changes and want to work on another issue use `git stash save {any name for future reference}`. To view all stashed items use `git stash list`, this will show as 
  `stash@{0}: On development: readme`
  And then you can use `git stash apply 0` to bring back this item.
* Sometimes we forget to make new branch and start the coding in `development` branch and then commit change in `development` branch, to uncommit change you can use `git reset HEAD~1`. This command will uncommit your local change and you can create new branch with these changes.
