# 02 Language

Vim has its own language, based on verbs, names and modifiers.

## Verbs

- `d`: delete
- `c`: change
- `y`: junk
- `p`: put

## Modifiers

- `i`: inside
- `a`: around
- `t`: till (uppercase for till backwards)
- `f`: find (like till, but includes the char) (uppercase for find backwards)
- '/' find (multichar)
- any number

## Names

- `l`: letter
- `w`: word
- `s`: sentence (also `)`)
- `p`: paragraph (also `}`)
- `t`: tag
- `"`: text between doble quotes
- `'`: text between single quotes
- `(`: parentheses (same for `{` and `[`)

## Some examples

- `diw`: delete inside word
- `daw`: delete around word
- `dap`: delete around paragraph
- `dt.`: delete till next `.`
- `d5w`: delete 5 words
- `d/abc`: delete until `abc`
- `di(` or `di)`: delete inside ().

## Language structure

The language structure follows the following pattern:

```
<number><verb><modifier><name or movement>
```

Yes, you can use names or movements. In case you use a movement instead of a name, the verb will apply to all text between your current position and the position after the movement. Its like `till`, but using more than just single letters. For example, `dgg` will delete everything between your current position till the begining of the file.

## More examples

-`d2l`: delete 2 letters 
-`yip`: yank inside paragrap 
-`cis`: change inside sentence 
-`ct,`: change till `,` 
-`di"`: delete inside double quotes 
-`di]`: delete inside brackets
- dT.``: delete until the previous `.`

## Some special actions

- `.`: repeat the last action
