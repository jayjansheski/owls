---
title: "Bash · Make & CD Into Directory"
description: Make and CD into a directory with nested path.
date: 2020-06-12
tags:
  - shell
  - command-line
layout: layouts/post.njk
---

Add this to your `.zshrc` or `.bashrc` file

```bash
mkcd () {
  case "$1" in
    */..|*/../) cd -- "$1";; # that doesn't make any sense unless the directory already exists
    /*/../*) (cd "${1%/../*}/.." && mkdir -p "./${1##*/../}") && cd -- "$1";;
    /*) mkdir -p "$1" && cd "$1";;
    */../*) (cd "./${1%/../*}/.." && mkdir -p "./${1##*/../}") && cd "./$1";;
    ../*) (cd .. && mkdir -p "${1#.}") && cd "$1";;
    *) mkdir -p "./$1" && cd "./$1";;
  esac
}
```

---

[Source](https://unix.stackexchange.com/a/9124)
