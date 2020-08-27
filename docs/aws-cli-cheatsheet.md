---
title: An AWS CLI cheatsheet
description: An aws-cli cheatsheet
date: 2018-09-30
tags:
  - aws
  - cli
layout: layouts/post.njk
---

Describe instances

```bash
aws ec2 describe-instances
```

### Logs

[Where are my AWS logs?](https://blog.rapid7.com/2013/11/20/where-are-my-aws-logs/)

View apache logs [^1]

```bash
aws logs describe-log-groups
```

## Resources

- [AWS CLI](https://aws.amazon.com/cli/)
- [devhints.io AWS CLI cheatsheet](https://devhints.io/awscli)
- [AWS CLI Aliases](https://github.com/awslabs/awscli-aliases/)

## Footnotes

[^1]: [AWS CLI Reference: Logs](https://docs.aws.amazon.com/cli/latest/reference/logs/index.html)
