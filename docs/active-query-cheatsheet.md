---
title: A Rails ActiveQuery cheatsheet
description: A Rails ActiveQuery cheatsheet
date: 2020-08-27
tags:
  - rails
  - sql
layout: layouts/post.njk
---

### Select only certain fields
```ruby
Book.select(:name, :summary)
# OR
Book.select("name, summary")
```