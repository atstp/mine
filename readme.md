![mine](http://atstp.github.io/hey_git_thats_mine/mine_logo.svg?v2)

> keep your notes, wips, and tinkerings out of git's hands (and _semi_ tracked)

## commands

  * **`mine snap`** - replace the old snapshot with your current `_mine_` files
  * **`mine restore`** - restore the last `_mine_` snapshot to your project
  * **`mine clean`** - remove all `_mine_` files from your repo
  * **`mine touch`** - simpler than `touch someFileName_mine_`
  * **`mine list`** - list the files under _mine_'s aegis

### quickstart

    git clone https://github.com/atstp/hey_git_thats_mine.git ~/.mine && cd ~/.mine
    bash ./configure
    # now exit and reopen your terminal

--------------------------------------------------------------------------------

#### install/config extra info

the not-so-hairy details: it adds two lines to your shell startup file

    export MINE_LOCATION=~/.mine   # where you cloned the repo
    function mine () { ${MINE_LOCATION}/mine $@; }

and adds one line to your global gitignore/excludesfile

    *_mine_*


you'll have to restart your termial for the changes to take effect
