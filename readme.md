# mine

If you're a fan of sticky notes, this could be for you.

`mine` uses a global ignore :globe_with_meridians: along with a handful of bash
functions to let you keep personal, _backup-able_ notes :memo: and repo-related
records with your repo and _insulated from its history_.

## about

an example:

                                           yours?
    hypothetical_repo/
        readme.md
        _mine_AWSloginInfo                 ✓
        usabilityIdeas_mine_               ✓
        bin/
            build
            generate
            fixEveryonesWhitespace_mine_   ✓
        src/
            main.file
            ...
        _mine_/                            ✓
            notes                          ✓
            todays-todo                    ✓
        ...

the `mine` command along with the `_mine_` files leave you free to

:closed_lock_with_key: keep login info for a related service with your repo
&mdash; :pencil: leave notes for yourself about where you left off and what to do later
&mdash; :running: work with a slapdash script until you get a real one together
&mdash; :white_check_mark: maintain a personal todo list
&mdash; :dash: remove all your personal files in an instant (perhaps before you ftp or rsync)
&mdash; :page_with_curl: store curled or pasted code for personal reference
&mdash; :link: store a collection of useful links that would otherwise clutter the history.

## commands

  * **`mine snap`** - take a snapshot of your current `_mine_` files
  * **`mine restore`** - restore the last snapshot
  * **`mine clean`** - remove all `_mine_` files from your repo
  * **`mine purge`** - purge all mine files from the current project _and_ backups
  * **`mine touch`** - an alternative to `touch fileName_mine_`
  * **`mine list`** - list the files under mine's aegis
  * **`mine help`**

### get it

    git clone https://github.com/atstp/mine.git ~/.mine
    cd ~/.mine
    bash ./configure
    # exit and reopen your terminal

mercurial users: after running `./configure`, add a rule to globally ignore
`*_mine_*` files, in the `syntax: glob` section

### update it

    cd ~/.mine
    git pull

### license

MIT

--------------------------------------------------------------------------------

### colophon

The "users" will likely be myself, but it's here for anyone who finds it useful.
This thing came about naturally for me: a local ignore, then a global ignore,
followed by a few convenience commands, now it's wrapped up here :octocat:.
If you've got an idea to make it more natural or intuitive, let me know with
an issue or a pull request. Enjoy!
