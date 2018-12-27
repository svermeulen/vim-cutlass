<img align="left" width="122" height="420" src="https://i.imgur.com/30weJjp.png">

## Cutlass

Very simple plugin that just overrides the delete operations to not affect the current yank.

The following keys are overridden to always use the black hole register:  `c`, `cc`, `C`, `s`, `S`, `d`, `dd`, `D`, `x`, `X`.

Note that if you have already mapped these keys to something else (like we do below with 'x') then it will not change it again.

All of these operations now simply delete and do not cut.  However, you will still want to have a key for 'cut', which you can add for example by including the following to your .vimrc:

```
nnoremap m d
xnoremap m d

nnoremap mm dd
nnoremap M D
```

'm' here can be thought of as 'move'.  Or you might want to use the 'x' key:

```
nnoremap x d
xnoremap x d

nnoremap xx dd
nnoremap X D
```

## Credits

Based off of [vim-easyclip](https://github.com/svermeulen/vim-easyclip) and also [Drew Neil's ideas](https://github.com/nelstrom/vim-cutlass) (as well as the name)

