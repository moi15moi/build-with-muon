# build-with-muon

Use this action to install a specific muon version.

## Usage

Add the following step to your workflow:

```yml
    steps:
      - name: install muon
        uses: muon-build/build-with-muon
        with:
          version: edge # optional, specify a git tag or sha, defaults to edge
          git_url: "..." # optional, specify a different git url to clone from
```
