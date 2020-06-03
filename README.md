# Add Labels

A GitHub Action to add labels on PR / Issue events

## Inputs

### `labels`

**Required** Labels to add.

### `issue_number`

**Optional** Issue/Pull number

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
      - uses: christianvuerings/add-labels@v1
        with:
          labels: |
            minor release
            bug
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
```

## Update compiled files

```
npm i
npm i -g @zeit/ncc
ncc build index.js
```
