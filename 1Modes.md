
# Modes

Vim has 3 modes. **Normal, Insert and Visual**.
You can use `Esc` key to traverse between different modes.

## Normal (Navigate)

The cursor looks like ▊ in normal mode. You can move through the
whole documents in this mode. More on this later.

## Edit (Type)

`i`

Inserts the cursor **before** the current position.
Make sure you are in **normal** mode by typing `Esc`.
Then put the cursor right below the arrow and type `i`.
The cursor will be inserted between *r* and *s* like this `r|s`.
After that you may proceed to type like how you normally do in the other normal text/code editors.

### Before `i`

```text
     ↓
["First", "Second", "Third]
```

### After

```text
["Fir|st", "Second", "Third]
```

`a`

Similar to `i`, but puts the cursor **after** the current position.
Then put the cursor right below the arrow and type `a`.
The cursor will be inserted between *s* and *t* like this `s|t`.
You may do your typing like how you normally do in normal text/code editors.

**Before** `a`

```text
     ↓
["First", "Second", "Third]
```

**After**

```text
["Firs|t", "Second", "Third]
```

`o`

Adds an empty line below the current line and insert cursor at the empty line.
Put the cursor anywhere in and type `o`.

**Before** `o`

```text
["First", "Second", "Third]
```

**After**

```text
["First", "Second", "Third]
|
```

`I`

Inserts the cursor **at the beginning** of the current **line**.
Make sure you are in normal mode and try typing `I`.
The cursor should be inserted before the first `[` like this `|[`

**Before** `I`

```text
     ↓
["First", "Second", "Third]
```

**After**

```text
|["First", "Second", "Third]
```

`A`

Like `I` but inserts the cursor at the end of the current line.

**Before** `A`

```text
["First", "Second", "Third]
```

**After**

```text
["First", "Second", "Third]|
```

`O` (Capital o)

Similar to `o` but adds the empty line **above** the current line.

**Before** `O`

```text
["First", "Second", "Third]
```

**After**

```text
|
["First", "Second", "Third]
```

## Visual (Select)

`v` Visual mode (Select by character)

**Before** `v` `3l`

```text
          ↓
["start", "curl", "stain", "brain", "such"]
```

**After** (the characters between `→ ←` are selected )

```text
["start", →"cur←l", "stain", "brain", "such"]
```

`V` Visual mode (Select by line)

**Before** `V` `4j`

```text
          ↓
["start", "curl", "stain", "brain", "such"]
["crowd", "presence", "serious", "puzzle", "base"]
["ink", "thread", "pure", "slippery", "around"]
["silent", "curl", "stain", "brain", "such"]
["crowd", "presence", "serious", "puzzle", "base"]
["ink", "thread", "pure", "slippery", "around"]
["silent", "curl", "stain", "brain", "such"]
["crowd", "presence", "serious", "puzzle", "base"]
["ink", "thread", "pure", "slippery", "around"]
["silent", "curl", "stain", "brain", "such"]
["ink", "thread", "pure", "slippery", "around"]
["crowd", "presence", "serious", "puzzle", "base"]
```

**After** (the lines between `→ ←` are selected )

```text
→["start", "curl", "stain", "brain", "such"]
["crowd", "presence", "serious", "puzzle", "base"]
["ink", "thread", "pure", "slippery", "around"]
["silent", "curl", "stain", "brain", "such"]
["crowd", "presence", "serious", "puzzle", "base"]←
["ink", "thread", "pure", "slippery", "around"]
["silent", "curl", "stain", "brain", "such"]
["crowd", "presence", "serious", "puzzle", "base"]
["ink", "thread", "pure", "slippery", "around"]
["silent", "curl", "stain", "brain", "such"]
["ink", "thread", "pure", "slippery", "around"]
["crowd", "presence", "serious", "puzzle", "base"]
```

`Ctrl+V` Visual mode (Select in Rectangle)
