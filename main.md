title: Git for Small Teams (Forking)
author:
    name: Kirk Byers
style: styles.css
output: index.html
controls: true

--

# Git for Small Teams

## A Forking Stratagy

--

### Context

When collaborating on a single git repo, there are several pain points developers encounter.

* What is the latest version of the project I should start working from?

* How do I add new features to the repo with out disrupting others?

* How do I consume the repo as part of another project?

-- 

### Enter Git Forks

Git Forks solve most of these problems out of the box.

Forking a project allows a developer to work independently while giving them an organized path to keep up to date with latest changes and pushing changes to repo.

We'll add a little bit of structure to the basic process to give us added benifits.

--

### Setup

Every repo should have a "master" branch and "dev" or "development" branch.

The "master" branch represents what is 100% stable and should be treated like production.

The "dev" branch is the development/working branch where all new branches should be started and merged back in. The "dev" branch should be stable for the most part; it is where breaking accidents should be caught. 

--

### Before We Start Development

1) `git clone` the main repo

2) Fork the main repo on Github

3) Add your fork to your remote by copying the clone URL and running `git remote add [remote-name] [clone-URL]`

You are now ready to start a new feature
--

### Workflow

1) Pull from `dev`

2) Branch from `dev`. Name your branch with your feature. Eg "kbye/loading-indicator"

3) When commiting changes write [quality commit messages](https://chris.beams.io/posts/git-commit/)

4) When your feature is complete, open a pull request

5) After some feedback, your feature will be merged in!

--

### Resolving Conflicting History

When you go to merge your feature back into "dev", you may encounter that "dev" has changed since your branched. To resolve

1) `git checkout dev` and `git pull`

2) `git checkout [feature-branch]` and `git merge dev`

3) `git push`

--

### Resolving Merge Conflict

Use `git status` after attempting a merge to see conflict files. Git will leave markers in the file to show you what code chunks are conflicting. Edit the conflicting files to remove the markers and have the desired resolution.

Check-in your resolved files and run `git commit` (no message) to commit the merge.

When in doubt on how to resolve files, ask the contributors. You can also run `git merge --abort` to cancel the merge.

--

## Example and Questions
