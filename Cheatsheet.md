## Entering Edit/Insert mode

`i` Inserts the cursor **before** the current position

`a` Similar to `i`, but puts the cursor **after** the current position

`o` Adds an empty line below the current line and insert cursor at the empty line

`I` Inserts the cursor **at the beginning** of the current **line**

`A` Like `I` but inserts the cursor at the end of the current line

`O` Similar to `o` but adds the empty line **above** the current line

## Motion

`w` Move to the start of the next word. (punctuation considered words)

`W` Move to the start of the **next** word. (spaces is the separator)

`b` Move to the start of the **current or previous** word. (punctuation considered words)

`B` Move to the start of the **current or previous** word. (spaces is the separator)

`%` Go to the matching ([{}])

`}` Move to the **next** empty line

`{` Move to the **previous** empty line

`f{character}` Move the cursor to the **next** occurrence of the character **in the current line**

`F{character}` Move the cursor to the **previous** occurrence of the character **in the current line**

`t{character}` Move the cursor to **just before** the **next** occurrence of the character **in the current line**

`T{character}` Move the cursor to **just before** the **previous** occurrence of the character **in the current line**

`;`  after `f` `F` `t` `T` will go to the **next** occurrence of the {character}

`,`  after `f` `F` `t` `T` will go to the **previous** occurrence of the {character}

## Operators

`d` Delete

`D` Delete everything from current position to the end of the line.

`c` Change (Delete + insert)

`C` equals to `D` + insert at the current position

`y` Yank (Copy)

`Y` copy the whole line

`p` Put (Paste) after the current position or the current line

`P` Put (Paste) before the current position or current line

`dd` Delete the current line

`cc` Change the current line

`yy` Copy the current line ( Same as `Y`)

`r` Replace one character

`x` Delete one character

`.` Repeat the last Edit operation

## Search

`/{entry}` + `<Enter>` will search the `{entry}` **forward** from the current position.

`?{entry}` + `<Enter>` will search the `{entry}` **backward** from the current position.

`n` go to the **next** occurrence of the `{entry}` 

`N` to go to the **previous** occurrence of the `{entry}`

`*` go to the next occurrence of the current word
## Useful patterns ( Operator + Count + Motion)

`d{number}w` delete {number} of words

`c{number}w` delete {number} of words and enter insert mode

`ct{character}` delete anything between the current position and the {character}, **excluding** the character, and enter insert mode

`cf{character}` delete anything between the current position and the {character}, **including** the character, and enter insert mode

`caw` delete the current word the cursor is at regardless of the cursor position inside the word and enter insert mode

`ci{` delete anything inside the `{}` and enter insert mode

`ca{` delete the whole block of `{}` including `{}` and the spaces around it
