# What?

say you're working on `something.c` and have this kinda thing in your `.vimrc` for a quick compile and run:

```vim
map <leader>cc :wa\|:!gcc %; ./a.out<cr>
```

and `a.out` isn't cutting it.

`something.c` should compile to `something`.

do this instead:

```vim
map <leader>cc :wa\|:!gcc % -o $(stripext %); ./$(scripext %)<cr>
```

# Install
* will create `~/bin/stripext`
* pick your poison
  * Ruby `./install_ruby.sh`
  * Crystal `./install_crystal.sh`

