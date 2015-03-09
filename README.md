# vim-til

Delicious morsels of Vim awesomeness.

## Capture the result of an Ex command into a register

I was trying to figure out a setting with the `comments` option and wanted to work with it in a buffer rather than just viewing the results in the statusline.

```
:redir @a
:set comments?
:redir END
```

<kbd>"ap</kbd> results in `comments=sO:* -,mO:*  ,exO:*/,s1:/*,mb:*,ex:*/,://` right there in the editor for playing with.

[Source](http://vim.wikia.com/wiki/Capture_ex_command_output)

## Yank (or delete) lines matching a pattern into a register

`:g/Line Pattern/d A` - Delete all lines matching 'Line Pattern' into *appended* register **A** (note the capitalization).

`:g/Line Pattern/y B` - Yank all lines matching 'Line Pattern' into *appended* register **B**.
