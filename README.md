# build-with-muon

Use this action to install a specific muon version.

## Usage

Add the following step to your workflow:

```yml
- name: Install muon
  uses: muon-build/build-with-muon@v2
  with:
    version: edge # optional, specify a git tag or sha, defaults to edge
    git_url: "..." # optional, specify a different git url to clone from
```

A simple example:

```yml
name: CI
on:
  push:
    branches:
      - master
jobs:
  test-action:
    name: Build my project
    runs-on: ubuntu-latest

    steps:
      - name: Install muon
        uses: muon-build/build-with-muon@v1

      - name: Checkout
        uses: actions/checkout@v4

      - name: Build
        run: muon setup build
