![mine](http://atstp.github.io/mine/mine_logo.svg?v2)

> keep your in-repo notes, wips, and tinkerings out of git's hands (and _semi_ tracked)

## what's it do?

add `_mine_` to the name of any file that is well... yours.

    # the file with names contiaining "_mine_" are ignored by git

    some_repository/
      readme.md
      cleanUp_mine_.sh                # ✓ this file
      bin/
        build
        generate
        fixEveryonesWhitespace_mine_  # ✓ this file
      src/
        main.file
        ...
      _mine_/                         # ✓ this dir
        notes                         # ✓ this file
        todays-todo                   # ✓ this file

`mine` commands _only_ touch those files

## commands

  * **`mine snap`** - replace the old snapshot with your current `_mine_` files
  * **`mine restore`** - restore the last `_mine_` snapshot to your project
  * **`mine clean`** - remove all `_mine_` files from your repo
  * **`mine touch`** - simpler than `touch someFileName_mine_`
  * **`mine list`** - list the files under _mine_'s aegis

### quickstart

    git clone https://github.com/atstp/mine.git ~/.mine && cd ~/.mine
    bash ./configure
    # now exit and reopen your terminal

--------------------------------------------------------------------------------

#### install/config extra info

the not-so-hairy details: (what the configure script does)

add two lines to your shell startup file

    export MINE_LOCATION=~/.mine   # where you cloned the repo
    function mine () { ${MINE_LOCATION}/mine $@; }

add one rule to your global ignore file

    *_mine_*

you'll have to restart your termial for the changes to take effect
