![mine](http://atstp.github.io/mine/mine_logo.svg?v2)

**mine** lets you add `_mine_` to the name of any files that are well... yours;
git will steer clear of them.

    some_repository/
        readme.md
        update_mine_.sh                   # ✓ yours!
        bin/
            build
            generate
            fixEveryonesWhitespace_mine_  # ✓ yours!
        src/
            main.file
            ...
        _mine_/                           # in a _mine_ dir
            notes                         # ✓ yours!
            todays-todo                   # ✓ yours!

`mine` commands _only_ touch those files

## commands

  * **`mine snap`** - replace the old snapshot with your current `_mine_` files
  * **`mine restore`** - restore the last `_mine_` snapshot to your project
  * **`mine clean`** - remove all `_mine_` files from your repo
  * **`mine purge`** - purge all mine files from the current project _and_ backups
  * **`mine touch`** - simpler than `touch someFileName_mine_`
  * **`mine list`** - list the files under _mine_'s aegis

### get it

    git clone https://github.com/atstp/mine.git ~/.mine
    cd ~/.mine
    bash ./configure
    # now exit and reopen your terminal

### update it

    cd ~/.mine
    git pull
    # hooray!

--------------------------------------------------------------------------------

mercurial users: after running `./configure`, you'll have to manually add a rule
to globally ignore `*_mine_*` files
