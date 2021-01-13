---
title: "Example note"
date: "2020-11-04"
last-modified: "2021-01-13"
excerpt: "Example note"
---

This is example note.

Example code blocks:

- Bash

```bash
gatsby develop
```

- Yml

```yml
# Dispatch push event to PTR-KLK/electron-brain repository

name: Dispatch to Electron Brain

on:
  push:
    branches:
      - master
jobs:
  dispatch:
    runs-on: ubuntu-latest
    steps:
      - name: Repository Dispatch
        uses: peter-evans/repository-dispatch@v1
        with:
          token: ${{ secrets.REPO_ACCESS_TOKEN }}
          repository: PTR-KLK/electron-brain
          event-type: new-note
          client-payload: '{"ref": "${{ github.ref }}", "sha": "${{ github.sha }}"}'
```

- Javascript

```javascript
console.log("Hello World!");
```