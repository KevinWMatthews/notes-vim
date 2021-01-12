# Vim Plugin: Terminal

See `:help terminal` or [vimhelp's terminal.txt](https://vimhelp.org/terminal.txt.html).

* Enter terminal mode:
  - `:terminal`
  - `:term`

## Special Keys

`CTRL-W` is a special key in terminal mode.
It can be used to move between windows or execute several special commands:

* Return to normal mode
  - `CTRL-W N`
  - `CTRL-\ CTRL-N`
  - **this is how to exit terminal mode**
* Send `CTRL-C`
  - `CTRL-W CTRL-C`
* Send `CTRL-\`
  - `CTRL-W CTRL-\`
* next/previous tab
  - `CTRL-W gt`, `CTRL-W gT`

The usual window commands still work.

## Terminal-Job Mode

The job has control of the terminal.
Anything you type goes directly to the job.
This is the default mode after a terminal is opened.

`:tmap` mappings apply in Terminal-Job mode:

* Set keymaps using `tmap` and `tnoremap`
* Inspect the current key map: `:tmap`

## Terminal-Normal Mode

Use this mode to enter a "vim" mode.
Normal commands apply.

To reenter the Terminal-Job as if entering insert mode:

* `i`
* `a`
* ? `:startinsert`

`:nmap` mappings apply in Terminal-Normal mode.

## Terminal-Debug

This plugin offers integration with gdb.
Be sure to know how to navigate in/out of terminal mode!

Load:

```
:packadd termdebug
```

Launch:

```
:Termdebug
```

### Commands

Navigate between `termdebug` windows using:

* `:Gdb`
* `:Program`
* `:Source`
* `:Asm`

Inspect variables in the source window using:

* `K`   <-- **use this!**
* `:Evaluate`
* `:Ev`


Several gdb commands can be entered in the vim editor itself, including:

* `:Run`
* `:Break`
* `:Clear`
* `:Delete` <-- this **is not** supported!
* `:Step`
* `:Over` (equivalent to gdb's `next`; `Next` is a vim command)
* `:Finish`
* `:Continue`
* `:Stop`
