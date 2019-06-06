# I. Modes



## Normal Mode



### 7. Pause - Brush Off Canvas

Exiting insert mode in normal mode allows reading, thinking, and other non-write things.

- `u`: undo
- `<C-r>`: redo



### 8. Chunk Undos

 `<ESC>o` might be better than <CR> in insert mode, as it alloss undo to not go so far back in time.



### 9. Compose Repeatable Diffs

`dbx`, `bdw`, `daw` has same effect, but `daw` is repeatable



### 10. Counts in Commands

`180<C-x>`: subtract 180 from number

`180<C-a>`: add 180 from number

`  set nrformats-=octal`: treat numerals as decimal, regardless of whether they are padded with zero (default in vim 8)



### 11. Don't Count if can `.`

`c3w ` / `3cw` to change 3 words forward, but  `dw` and `..` may be better because you can undo in chunks.

In general,  more worth it to do `.` when larger counts as are easier to count wrong, but less worth it for smaller counts as you to type more`.`



### 12. Operator + Motion = Action

##### Operators

| Trigger | Effect                                                       |
| :------ | :----------------------------------------------------------- |
| c       | Change then go into insert mode                              |
| s       | Substitute then go into insert mode, `3s` deletes 3 chars in front, = `3cl` |
| d       | Delete                                                       |
| r       | Replace (remain in normal mode)                              |
| y       | Yank into register                                           |
| g~      | Toggle upper/lowercase                                       |
| gu      | Make lowercase                                               |
| gU      | Make uppercase                                               |
| >       | Shift right                                                  |
| <       | Shift left                                                   |
| =       | Autoindent                                                   |
| !       | Filter {motion} lines through an external program            |

_Operator-Pending mode_: before motion is pressed, go back to normal w/ <ESC>

When operator is pressed twice: it affects the whole line. `dd` deletes line, `gUgU / gUU` capitalizes line.



##### __Motions__

- Text Objects: `i`/inner does not include trailing whitespace

- `iw`, `aw` - inner word, a word

- `ip`, `ap` - inner paragraph, a paragraph

- `i)`, `ap` - inner parenthesis, a parenthesis

- `i'`, `a'` - inner single quote

- `i"`, `a"` - inner double quote

- `it`, `at` - inner tag, a tag

  

##### Actions

- `dw` - delete to the next word

- `dt,` - delete up until the next comma on the current line

- `de` - delete to the end of the current word

- `d2e` - delete to the end of next word

- `dj` - delete down a line (current and one below)

- `dt)` - delete up until next closing parenthesis

- `d/rails` - delete up until the first search match for “rails”

  

- `gg=G` - autoindent whole file

- `gcae` - to toggle comment whole file





## Insert Mode

### 13. Correct in Insert

Don't need to go back to normal mode to delete back

| Keystroke | Effect                                |
| --------- | ------------------------------------- |
| `<C-h>`     | Delete back one character (backspace) |
| `<C-w>`     | Delete back one word                  |
| `<C-u>`     | Delete back to start of line          |

Can use in cmd line or bash shell too!



### 14. Back to Normal mode

| Keystrokes | Effect                       |
| :--------- | :--------------------------- |
| `<Esc>`      | Switch to Normal mode        |
| `<C-[>`      | Switch to Normal mode        |
| `<C-o>`      | Switch to Insert Normal mode |



## Visual Mode





## Command-Line Mode

