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
