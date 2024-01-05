# check-release-notes

This action runs the Kuberbetes release-notes tool to ensure a PR has a valid 
release notes block. The action run will fail if the block is not found and
the PR is not properly labeled with `release-notes-none`.

## Example Run

```yaml
name: Check Release Notes

on:
  pull_request:

jobs:
  check-release-notes:
    runs-on: ubuntu-latest

    permissions:
      pull-requests: read # needed to read the PR data

    steps:
      - name: Install publish-release
        uses: kubernetes-sigs/check-release-notes
```

