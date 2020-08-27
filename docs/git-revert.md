---
title: Git · revert a branch to a previous commit
description: Revert a Git branch to a previous commit
date: 2020-06-13
tags:
  - git
layout: layouts/post.njk
---

```bash
git	 rebase -i <hash>
```

change `pick` to `d` of (probably) all commits

```bash
:%s/^pick/d/g
wq
git push -f origin branch-name
```
