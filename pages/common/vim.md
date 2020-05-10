# vim

> Vi IMproved, a programmer's text editor, providing several modes for different kinds of text manipulation.
> Pressing `i` enters edit mode. `<Esc>` goes back to normal mode, which doesn't allow regular text insertion.

- Copy ("yank") or cut ("delete") the current line (paste it with `P`):

`<Esc>{{yy|dd}}`

- Search for a pattern in the file (press `n`/`N` to go to next/previous match):

`<Esc>/{{search_pattern}}<Enter>`

- Perform a regex substitution in the whole file:

`<Esc>:%s/{{pattern}}/{{replacement}}/g<Enter>`

- Redirect ouput to vim

`vim <(ls -la)`
`ls -la | vim -`

- Save/Restore session

`:mks`
`:mks!`
`vim -S`

- Copy and past word

`yiw   Yank inner word (copy word under cursor, say "first").`
`viwp  Select "second", then replace it with "first".`
`viw"0p  Select "third", then replace it with "first".`

`yiw   Yank inner word (copy word under cursor, say "first"). `
`
- see logs in vim to a file

`vim -V20`


