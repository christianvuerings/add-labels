# Add Labels

A GitHub Action to add labels on PR / Issue events

## Inputs

### `labels`

**Required** Labels to add.

## Example usage

```
name: Add Label
on:
  pull_request:
    branches:
      - master
    types:
      - opened

jobs:
  add-label:
    name: Add Label
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - uses: christianvuerings/add-labels@1
        with:
          labels: |
            minor release
            bug
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
```

## Update compiled files

```
npm i -g @zeit/ncc
ncc build index.js
```
