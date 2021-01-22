# gitmoji-changelog-action
runs gitmoji-changelog and commits the changes

example:
```
name: "Bump Version"

on:
  push:
    branches:
      - "main"

jobs:
  generate-changelog:
    runs-on: ubuntu-latest

    steps:
      - name: "Checkout source code"
        uses: "actions/checkout@v2"
        with:
          fetch-depth: 0 # 👈 Required to retrieve git history for changelog
      - name: Gitmoji Changelog Action
        uses: MarkLyck/gitmoji-changelog-action@1.0.2
```