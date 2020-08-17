# git-todo

git-todo maintains a local per-branch todo list to keep
track of what you want to do on each branch before you
feel ready to push it upstream.

## Usage

Put in your path, make sure it's executable and run
`git todo` from a git directory while not in a
detached head state. It will launch a text editor
for you to enter whatever freeform text you want.

With the -p argument, it will instead send it to
your pager so you can see the branch's todo in the
terminal without editing it.

`git-todo` will check for the text editor by looking
for the environment variable `$TODO_EDITOR`, then
`$GIT_EDITOR`, then `$EDITOR`, and fall back to the
standard editor, `ed` if none of the above are set.

Similarly, with the `-p` argument it will go through
`$X_PAGER` environment variables before falling back
on `cat`.
