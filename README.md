# gitflow_release_action
This workflow allows for automated releases using git-flow

##### Copied from https://github.com/thomaseizinger/github-action-gitflow-release-workflow
##### Changes:
- changed master to main
- changed dev to develop

# Usage

1. Using git-flow with a branch named `develop` and a branch named `main`, create a release or hotfix branch and push it to GitHub
2. Create a PR targeting main
3. Merge the PR into main

The workflow will run and:

- create a Release using the version number parsed from the release/hotfix branch
- create a PR merging `main` into `develop`
