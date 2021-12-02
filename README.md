# gitflow_release_action
##### Copied from https://github.com/thomaseizinger/github-action-gitflow-release-workflow

This workflow allows for automated releases using git-flow

# Usage

1. Using git-flow, create a release or hotfix branch and push it to GitHub
2. Create a PR targeting main
3. Create a workflow as below in order to trigger this workflow when closing the PR:

```yml
name: publish release

on:
  pull_request:
    branches:
      - main
    types:
      - closed
jobs:
  publish_release:
    uses: kdubroff/gitflow_release_action/.github/workflows/publish_release.yml@8e8c36c336da44de5ac52cfc81e391c3c7df13d9
```
