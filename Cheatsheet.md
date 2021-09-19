## Entering Edit/Insert mode

`i` Inserts the cursor **before** the current position

`a` Similar to `i`, but puts the cursor **after** the current position

`o` Adds an empty line below the current line and insert cursor at the empty line

`I` Inserts the cursor **at the beginning** of the current **line**

`A` Like `I` but inserts the cursor at the end of the current line

`O` Similar to `o` but adds the empty line **above** the current line

## Motion

`f{character}` Move the cursor to the **next** occurrence of the character **in the current line**

`F{character}` Move the cursor to the **previous** occurrence of the character **in the current line**

`t{character}` Move the cursor to **just before** the **next** occurrence of the character **in the current line**

`T{character}` Move the cursor to **just before** the **previous** occurrence of the character **in the current line**

## Operators

`d` Delete

`D` Delete everything from current position to the end of the line.

`c` Change (Delete + insert)

`C` equals to `D` + insert at the current position

`y` Yank (Copy)

`Y` copy the whole line

`p` Put (Paste) after the current position or the current line

`P` Put (Paste) before the current position or current line

`r` Replace one character

`x` Delete one character

## Useful patterns ( Operator + Count + Motion)

`d{number}w` delete {number} of words

`c{number}w` delete {number} of words and enter insert mode

`ct{character}` delete anything between the current position and the {character}, **excluding** the character, and enter insert mode

`cf{character}` delete anything between the current position and the {character}, **including** the character, and enter insert mode

`caw` delete the current word the cursor is at regardless of the cursor position inside the word and enter insert mode

`ci{` delete anything inside the `{}` and enter insert mode

`ca{` delete the whole block of `{}` including `{}` and the spaces around it
