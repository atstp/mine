# mine

If you're a fan of sticky notes, this could be for you.

`mine` uses a global ignore along with a handful of bash functions to let you
keep personal, _backup-able_ notes and repo-related records with your repo and
_insulated from its history_.

## about

an example:

                                           yours?
    hypothetical_repo/
        readme.md
        AWSloginInfo._mine                 ✓
        usabilityIdeas._mine               ✓
        bin/
            build
            generate
            fixEveryonesWhitespace._mine   ✓
        src/
            main.file
            ...
        dev._mine/                         ✓
            notes                          ✓
            todays-todo                    ✓
        ...

the `mine` command along with the `._mine` files leave you free to

:closed_lock_with_key: keep login info for a related service with your repo
&mdash; :pencil: leave notes for yourself about where you left off and what to do later
&mdash; :running: work with a slapdash script until you get a real one together
&mdash; :white_check_mark: maintain a personal todo list
&mdash; :dash: remove all your personal files in an instant (perhaps before you ftp or rsync)
&mdash; :page_with_curl: store curled or pasted code for personal reference
&mdash; :link: store a collection of useful links that would otherwise clutter the history.

## commands

  * **`mine snap`** - take a snapshot of your current `._mine` files
  * **`mine restore`** - restore the last snapshot
  * **`mine clean`** - remove all `._mine` files from your repo
  * **`mine purge`** - purge all mine files from the current project _and_ backups
  * **`mine touch`** - an alternative to `touch fileName._mine`
  * **`mine list`** - list the files under mine's aegis
  * **`mine help`**

### get it

    git clone https://github.com/atstp/mine.git ~/.mine
    cd ~/.mine
    bash ./configure
    # exit and reopen your terminal

mercurial users: after running `./configure`, add a rule to globally ignore
`*._mine*` files, in the `syntax: glob` section

### update it

    cd ~/.mine
    git pull

### license

MIT

--------------------------------------------------------------------------------

### colophon

The "users" will likely be myself, but it's here for anyone who finds it useful.
This thing came about naturally for me: a local ignore, a global ignore, then a
few convenience commands; hopefully that helped. Now it's here :octocat:.

Any issues and a pull requests are welcome. Enjoy!
