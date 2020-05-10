# Development process

Here's a quick summary:

* Assign issues you're working on to yourself.
* Work on a branch per issue, something like `issue-number-name-of-feature`. One branch per feature/bug, please.
* When you're finished, mark the PR for review by labelling with "Review &amp; Merge".
* Get someone to review your code, and assign to them

### Git Flow

If you're new to them here are a few steps to help you get started:

* Ensure you're in the on the `development` branch. `git checkout development`
* Ensure this branch is up to date. `git pull`
* Create a new branch `git checkout -b issue-number-name-of-feature`
* Add your files.  `git add .` or if you've changed a lot of files use `git add -p` to be prompted about small chunks of code
* Commit your files. `git commit -m "Adds name of feature`
* Push the branch to Github. `git push`
* Submit a new pull request to the team and request a review
* Merge PR into `development` and make sure the branch is deleted

### Client testing
Once the code is ready for the client to test, merge to staging doing the following

* Create a new branch off of staging, `git checkout -b issue-number-name-of-feature-staging`
* Then cherry pick the PR that was merged into development `git cherry-pick -m 1 <PR hash>`
* Push the branch to Github
* Submit a new pull request and assign to one of the other developers
* Merge PR into `staging` and make sure the branch is deleted
