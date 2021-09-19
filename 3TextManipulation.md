# Combining count, operator and motion (In Normal mode)

## Vim operators

1. `d` Delete
2. `c` Change (Delete + insert)
3. `y` Yank (Copy)
4. `p` Put (Paste) after the current position or current line

## Count + Operator + Motion

`2` `d` `w` = `d` `2` `w` = delete 2 words from current position. Put the cursor at `⤋` and type `2dw` or `d2w`. I prefer `d2w` as it sounds like `delete 2 words`.

**Before**

```
      ⤋
Don’t look for the next opportunity.
The one you have in hand is the opportunity. 
- Paul Arden
```

**After**

```
Don’t the next opportunity.
The one you have in hand is the opportunity. 
- Paul Arden
```

Note that `d2w` will delete from the current position. If your cursor is in the middle of a word, it will delete the current position to the end of the word and also the subsequent word.

**Before**

```
                     ⤋
Don’t look for the next opportunity.
The one you have in hand is the opportunity. 
- Paul Arden
```

**After**

```
Don’t look for the ne.
The one you have in hand is the opportunity. 
- Paul Arden
```

This could be inconvenience as normally you will want to delete the whole word instead of partially. There are two options to fix this. One is to make sure the cursor is at the beginning of the word by typing `b` before deleting it. Another is to use `a` operator.
`daw` (delete a word) will delete the word of the current position.

**Before**

```
                     ⤋
Don’t look for the next opportunity.
The one you have in hand is the opportunity. 
- Paul Arden
```

**After**

```
Don’t look for the opportunity.
The one you have in hand is the opportunity. 
- Paul Arden
```

## `c` Change operator

Most of the the time you might want to replace a word instead of just deleting it. For example, to delete a word you have to `dw` and type `i` to go into insert mode and start typing. Vim has a shortcut for this. You can just type `cw`. This will delete the word and put you into insert mode.

Try typing `cw` and type "test". The word `next` is now replaced with `test`.

**Before** 

```
                   ⤋
Don’t look for the next opportunity.
The one you have in hand is the opportunity. 
- Paul Arden
```

**After**

```
Don’t look for the test opportunity.
The one you have in hand is the opportunity. 
- Paul Arden
```

## `y` yank and `p` Paste

As the title implies, `y` and `p` are copy and paste operators. As you might have guessed, you can combine these operators with motions that we learnt earlier.

Type `yf.`, the phrase `look for the next opportunity.` will be copied. You can paste it by simply typing `p`. 

**Before** 

```
      ⤋
Don’t look for the next opportunity.
The one you have in hand is the opportunity. 
- Paul Arden
```

**After**

```
Don’t llook for the next opportunity.ook for the next opportunity.
The one you have in hand is the opportunity. 
- Paul Arden
```

Notice how the phrase was pasted after the current position `llook ...`. If you want to paste it before the current position `P` will do the trick.

## Capitalized operators

`P` works differently from `p`. Yes, the other operators also behave differently when capitalized.

1. `D` Delete everything from current position to the end of the line.
2. `C` equals to `D` + insert at the current position
3. `Y` copy the whole line
4. `P` Put (Paste) before the current position or current line


## Misc

Remember how we use `a` above in `daw` to delete a word regardless of where the cursor position is in a word? Well, there are a few special ones just like it.

### `i` (Inner)

Put the cursor at the arrow and type `ci"`. The word inside the double quotes will be deleted and you will be in insert mode. This could be quite handy as it works for `()` `{}` `''` as well.


**Before** 

```
            ⤋
["First", "Second", "Third]
```

**After**

```
["First", "|", "Third]
```

Type  `ca"` will also delete the quotes as well as the spaces around the quotes.

**Before** 

```
            ⤋
["First", "Second", "Third]
```

**After**

```
["First",|, "Third]
```
