# Vim Plugin: Matchit

Built-in plugin  that extends the match operator `%`.

Not enabled by default! Enable using:

```
:packadd matchit
```

See `:help matchit` (after loading).

## Special Keys

Extends `%` matching from braces, brackets, and parens to general 'matchpairs'.
This includes if/else/endif, html, etc.

* Cycle through extended match pairs
  - `%`
* Move to use previous/next matched group (can move out)
  - `[%`
  - `]%`

# TODO

* in visual mode: `a%`
