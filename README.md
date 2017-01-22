# vim-paste-easy

Automatically `set paste` for you.

This is a tiny plugin that simply monitors your typing speed and `set paste`
automatically. When then typing interval between two typed characters is less
than 0.01s, it will `set paste` for you. Because there's no human being could
type that fast! After you have finished pasting and leave insert mode, or if
the file stays unchanged for about 0.1s, vim-paste-easy will `set nopaste` for
you.

## Motivation

I'm using terminal (n)vim with xshell. Many times I need to paste a block of
code from other documents or web pages, I have to `:set paste` before
`<Shift><Insert>`, otherwise the indentation will be messed up. I want this to
work automatically, and it seems there's no way to detect `<Shift><Insert>`
key in this case. Finally I decided to use the typing interval.

## commands

- `:PasteEasyDisable` disable paste-easy temporary
- `:PasteEasyEnable` enable paste-easy. This plugin is enabled by default,
  This command is only needed after you `PasteEasyDisable`.

If you don't want vim-paste-easy enabled by default, add
`let g:paste_easy_enable=0` into your vimrc.

