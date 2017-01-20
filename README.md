# vim-paste-easy

Automatically `set paste` for you.

This is a tiny plugin that simply monitors your typing speed. When then typing
interval between two typed character is less than 0.01s, it automatically `set
paste` for you. Because there's no human could type that fast! After you
finish pasting, and leave insert mode, vim-paste-easy will automatically `set
nopaste` for you.

## Motivation

I'm using terminal (n)vim with xshell. Many times I need to paste a block of
code from other documents or web pages, I have to `:set paste` before
`<Shift><Insert>`, otherwise the indentation will be messed up. I want this to
work automatically, and it seems there's no way to detect `<Shift><Insert>`
key in this case. Finally I decided to use the typing interval.

