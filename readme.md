![mine](http://atstp.github.io/mine/mine_banner.svg?v0)

add `_mine_` to a filename and it's, well... yours

    some_repository/
        readme.md
        update_mine_.sh                   # ✓ yours
        bin/
            build
            generate
            fixEveryonesWhitespace_mine_  # ✓ yours
        src/
            main.file
            ...
        _mine_/                           # (in a _mine_ dir)
            notes                         # ✓ yours
            todays-todo                   # ✓ yours
        ...

`_mine_` files

  * stay out of git's history
  * persist through `git checkout`, `rebase`, and `reset`
  * respond to `mine` commands
  * can be wiped from the repo with a single command
  * are easily backed-up and restored (separate from git)

which means you can

  * :closed_lock_with_key: store your login info for a related service with your repo
    _confident it won't be published_
  * :pencil: leave notes for yourself about where you left off and what to do later
  * :running: keep working with a slapdash script until you get a real one together
    (and commit that one)
  * :white_check_mark: maintain a personal todo list
  * :dash: remove all your personal files in an instant (perhaps before you ftp a bunch of stuff?)
  * :page_with_curl: store curled or pasted code that will be a good reference
  * :link: maintain a collections of useful links that don't belong in git's history

**It's for you**: if you're already comfortable using git through the command line,
and you're open to new workflows.

**It might not be**: if your workflow hasn't changed because it's already perfect, or if
you're happy keeping your repo related stuff outside the repo it relates to.

## commands

  * **`mine snap`** - take a snapshot of your current `_mine_` files
  * **`mine restore`** - restore the last snapshot
  * **`mine clean`** - remove all `_mine_` files from your repo
  * **`mine purge`** - purge all mine files from the current project _and_ backups
  * **`mine touch`** - simpler than `touch someFileName_mine_`
  * **`mine list`** - list the files under _mine_'s aegis
  * **`mine help`**

### get it

    git clone https://github.com/atstp/mine.git ~/.mine
    cd ~/.mine
    bash ./configure
    # exit and reopen your terminal

### update it

    cd ~/.mine
    git pull

--------------------------------------------------------------------------------

mercurial users: after running `./configure`, you'll have to manually add a rule
to globally ignore `*_mine_*` files
