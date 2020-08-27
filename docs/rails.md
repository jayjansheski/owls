---
title: Rails Cheat Sheet
description: How to do Rails things
date: 2020-06-17
tags:
  - rails
  - ruby
layout: layouts/post.njk
---

### What methods does an object have?

```bash
irb
```

then

```ruby
irb(main):001:0> import 'rails'
irb(main):002:0> ActionDispatch::Reloader.methods()
```

## Reset user's password from the Rails console (if you're using _Devise_) [^1]

```ruby
user = User.where(email: 'user@example.com').first
user.password = 'THE_NEW_PASSWORD'; user.save
```

## Gotchas

### Environment variables aren't available in the console.

[Rails 5 Sending STDOUT via environment variable | BigBinary Blog](https://blog.bigbinary.com/2016/04/12/rails-5-allows-to-send-log-to-stdout-via-environment-variable.html)

## Troubleshooting

### \$color: "foreground(#2199e8)" is not a color for `red'

Use `color-pick-contrast()` instead of `foreground()`

### Invalid CSS after "&.": expected class name, was "2em"

You may see this error if you're upgrading `foundation-rails`. The solution is to define `$close-button-size` as a _list_.

````css
$close-button-size: (
  small: 1.5em,
  medium: 2em
);
```s

## Footnotes

[^1]: https://stackoverflow.com/questions/8306430/devise-password-reset-from-rails-console
````
