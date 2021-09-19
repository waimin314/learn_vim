# Vim motion (normal mode)

## Faster motion

`f{character}`

Move the cursor to the **next** occurrence of the character **in the line current**.

Put the cursor at the `⤋` and type `fs`. The cursor will move to the first `s`.

**Before** `fs`
```
    ⤋
“Everything happens for a reason. 
Sometimes the reason is you're stupid and make bad decisions.”
- Marion G. Harmon
```

**After**
```
                  ⤋
“Everything happens for a reason. 
Sometimes the reason is you're stupid and make bad decisions.”
- Marion G. Harmon
```

`F{character}`

Move the cursor to the **previous** occurrence of the character **in the line current**.

**Before** `Fa`
```
                        ⤋
“Everything happens for a reason. 
Sometimes the reason is you're stupid and make bad decisions.”
- Marion G. Harmon
```

**After**
```
             ⤋
“Everything happens for a reason. 
Sometimes the reason is you're stupid and make bad decisions.”
- Marion G. Harmon
```

`t{character}`

Move the cursor to **just before** the **next** occurrence of the character **in the line current**.

**Before** `ts`
```
    ⤋
“Everything happens for a reason. 
Sometimes the reason is you're stupid and make bad decisions.”
- Marion G. Harmon
```

**After**
```
                 ⤋
“Everything happens for a reason. 
Sometimes the reason is you're stupid and make bad decisions.”
- Marion G. Harmon
```

`T{character}`

Yeah, you guessed it. It will move the cursor to **just before** the **previous** occurrence of the character **in the line current**.

**Before** `Ta`
```
                        ⤋
“Everything happens for a reason. 
Sometimes the reason is you're stupid and make bad decisions.”
- Marion G. Harmon
```

**After**
```
              ⤋
“Everything happens for a reason. 
Sometimes the reason is you're stupid and make bad decisions.”
- Marion G. Harmon
```

## Misc.

`;`  after `f` `F` `t` `T` will go to the **next** occurrence of the {character}

`,`  after `f` `F` `t` `T` will go to the **previous** occurrence of the {character}
