---
layout:   post
title:    "rbenv Build System On Ubuntu Sublime Text 3"
date:     2016-11-11 22:11:22 +0900
---

When you install `ruby` using `rbenv` on ubuntu, sometimes `build` doesn't work. Then you should make custom build system for `ruby`. Make new build system `rbenv.sublime-build`, use the following JSON codes:

```json
{
  "cmd": ["/home/[user]/.rbenv/shims/ruby", "$file"],
  "file_regex": "^(...*?):([0-9]*):?([0-9]*)",
  "selector": "source.ruby"
}
```
