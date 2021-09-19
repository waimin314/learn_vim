## Period `.`

`.` will repeat the last `Edit` operation. Type in `ci"` and then `apple` and `<Esc>` to go back to normal mode. The word `First` will now be replaced with `apple`. Now you can repeat the `ci"` and type again for `Second` and `Third`. But that's too repetitive. Typing `.` will repeat the last command you type in for the change. In our case `.` will repeat `ci"apple<Esc>`

**Before** `ci"` and `apple` and type `<Esc>`
``` 
    ⤋
["First", "Second", "Third"]
```

**After**
``` 
["apple", "Second", "Third"]
```

Move the cursor to `⤋` and type `.`

**Before** `.`

``` 
            ⤋
["apple", "Second", "Third"]
```

**After**

``` 
["apple", "apple", "Third"]
```

## Search

Vim has two search operations `/` and `?`

Type in `/{entry}` and then `<Enter>` will search the `{entry}` **forward** from the current position.

Type in `?{entry}` and then `<Enter>` will search the `{entry}` **backward** from the current position.

After typing search `{entry}`, use `n` to go to the **next** occurrence of the `{entry}` and `N` to go to the **previous** occurrence of the `{entry}`

## Plugins

### Easymotion

