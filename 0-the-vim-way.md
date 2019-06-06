## The VIM way



### 0. Mac Notes

- Map `<CAPS-LOCK>` to `<ESC>`

- `<C-a>` means `<CTRL>+<a>` from this point

- Karibiner Elements: Swap `<FN>` and `<CTRL>  `so 1 hand can do `<C-r>`

  

### 1. Dot Command

1. `x`: cut, `>G` indent 

2. `.`: repeat

   

### 2. Compound Movement

Basic motions:

- up/down: `j` /`k`
- left/right: `h`/`l`
- prev/next para: `<S-[>` /  `<S-]>` 

| Compound Command | Equivalent in Longhand |
| :--------------- | :--------------------- |
| C                | c$                     |
| s                | cl                     |
| S                | ^C                     |
| I                | ^i                     |
| A                | $a                     |
| o                | A`<CR>`                |
| O                | ko                     |



### 3. Repeatable Chunks

__e.g. Adding space between + sign:__

1. `f+`: find +
2. `s<SPACE>+<SPACE><ESC>`: replace '+' with ' + '
3. `;`: repeat search (1)
4. `.`: repeat replacement



### 4. Repeat Forward, or Backward

| Intent                           | Act                   | Repeat | Reverse |
| :------------------------------- | :-------------------- | :----- | :------ |
| Make a change                    | {edit}                | .      | u       |
| Scan line for next character     | f{char}/t{char}       | ;      | ,       |
| Scan line for previous character | F{char}/T{char}       | ;      | ,       |
| Scan document for next match     | /pattern`<CR>`        | n      | N       |
| Scan document for previous match | ?pattern`<CR>`        | n      | N       |
| Perform substitution             | :s/target/replacement | &      | u       |
| Execute a sequence of changes    | qx{changes}q          | @x     | u       |

 

### 5. Replace by Hand

intent: replace selected 'target' with 'new_word'

1. `/targ`: search for 'target' word with prefix
2. `*`: make search cursor highlight 'target' word

3. `cw<new_word><ESC>`: _change_ 'target' to 'new word'
4. `n`: move the next match for 'target'
5. `.`: repeat the change word action



### 6. Dot Formula

The ideal is 1 command for movement, 1 command for action (repeatable with the `.` command) :smile:

