# Combining count, operator and motion (In Normal mode)

## Vim operators

1. `d` Delete
2. `D` Delete everything from current position to the end of the line.
3. `c` Change (Delete + insert)
4. `C` `D` + insert at the current position
5. `y` Yank (Copy)
6. `Y` copy the whole line
7. `p` Paste after the current position or current line
8. `P` Paste before the current position or current line

## Count + Operator + Motion

`2` `d` `w` = `d` `2` `w` = delete 2 words from current position. Put the cursor at `⤋` and type `2dw` or `d2w`. I prefer `d2w` as it sounds like `delete 2 words`.

**Before**

```
      ⤋
Don’t look for the next opportunity.
The one you have in hand is the opportunity. 
- Paul Arden
```

After

```
Don’t the next opportunity.
The one you have in hand is the opportunity. 
- Paul Arden
```

Note that `d2w` will delete from the current position. If your cursor is in the middle of a word, it will delete the current position to the end of the word and also the subsequent word.

```
                     ⤋
Don’t look for the next opportunity.
The one you have in hand is the opportunity. 
- Paul Arden
```

After

```
Don’t look for the ne.
The one you have in hand is the opportunity. 
- Paul Arden
```

This could cause inconvenience as normal you will want to delete the whole word instead of partial. There are two options to fix this. One is to make sure the cursor is at the beginning of the word by typing `b`. Another is to use `a` operator.
`daw` (delete a word) will delete the word of the current position.

```
                     ⤋
Don’t look for the next opportunity.
The one you have in hand is the opportunity. 
- Paul Arden
```

After

```
Don’t look for the opportunity.
The one you have in hand is the opportunity. 
- Paul Arden
```

## `C` Change operator
