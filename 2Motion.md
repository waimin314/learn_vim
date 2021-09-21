# Vim motion (normal mode)

## Basic Navigation ( h j k l )

          ↑ 
    ← h j k l →
        ↓

h j k l acts as arrow keys. Try navigating the following using just the `h j k l` keys

```
cursor here
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

Adding a number `n` in front of the `h j k l` makes the keys repeat by `n` times. For example, put the cursor at
`↓` and type `10j`. The cursor will move to 10 lines below.

### Fast Motion ( w W b B e E % {} )

`w` Move to the start of the next word. (punctuation considered words)

**Before** `w`
```
    ↓
["silent", "curl", "stain", "brain", "such"]
```

**After**
```
        ↓
["silent", "curl", "stain", "brain", "such"]
```

`W` Move to the start of the **next** word. (spaces is the separator)

**Before** `W`
```
    ↓
["silent", "curl", "stain", "brain", "such"]
```

**After**
```
           ↓
["silent", "curl", "stain", "brain", "such"]
```

You can type `{number}w` or `{number}W` to jump to `{number}` of words. Or you can just repeatedly type `w` or `W` to jump word by word.

**Before** `WWW`
```
    ↓
["silent", "curl", "stain", "brain", "such"]
```

**After**
```
                            ↓
["silent", "curl", "stain", "brain", "such"]
```

`b` Move to the start of the **current or previous** word. (punctuation considered words)

**Before** `b`
```
               ↓
["silent", "curl", "stain", "brain", "such"]
```

**After**
```
            ↓
["silent", "curl", "stain", "brain", "such"]
```

`B` Move to the start of the **current or previous** word. (spaces is the separator)

**Before** `2B`
```
                        ↓
["silent", "curl", "stain", "brain", "such"]
```

**After**
```
           ↓
["silent", "curl", "stain", "brain", "such"]
```

## Faster motion

`f{character}`

Move the cursor to the **next** occurrence of the character **in the line current**.

Put the cursor at the `↓` and type `fs`. The cursor will move to the first `s`.

**Before** `fs`
```
    ↓
“Everything happens for a reason. 
Sometimes the reason is you're stupid and make bad decisions.”
- Marion G. Harmon
```

**After**
```
                  ↓
“Everything happens for a reason. 
Sometimes the reason is you're stupid and make bad decisions.”
- Marion G. Harmon
```

`F{character}`

Move the cursor to the **previous** occurrence of the character **in the line current**.

**Before** `Fa`
```
                        ↓
“Everything happens for a reason. 
Sometimes the reason is you're stupid and make bad decisions.”
- Marion G. Harmon
```

**After**
```
             ↓
“Everything happens for a reason. 
Sometimes the reason is you're stupid and make bad decisions.”
- Marion G. Harmon
```

`t{character}`

Move the cursor to **just before** the **next** occurrence of the character **in the line current**.

**Before** `ts`
```
    ↓
“Everything happens for a reason. 
Sometimes the reason is you're stupid and make bad decisions.”
- Marion G. Harmon
```

**After**
```
                 ↓
“Everything happens for a reason. 
Sometimes the reason is you're stupid and make bad decisions.”
- Marion G. Harmon
```

`T{character}`

Yeah, you guessed it. It will move the cursor to **just before** the **previous** occurrence of the character **in the line current**.

**Before** `Ta`
```
                        ↓
“Everything happens for a reason. 
Sometimes the reason is you're stupid and make bad decisions.”
- Marion G. Harmon
```

**After**
```
              ↓
“Everything happens for a reason. 
Sometimes the reason is you're stupid and make bad decisions.”
- Marion G. Harmon
```

## Misc.

`;`  after `f` `F` `t` `T` will go to the **next** occurrence of the {character}

`,`  after `f` `F` `t` `T` will go to the **previous** occurrence of the {character}
