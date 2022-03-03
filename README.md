# Utilities for Git

## Setup

1. Clone this repository anywhere
2. Add `bin/` to your `PATH` environment variable

## Scripts

### List ignored files (`git-ls-ignored-files`)

The `git status --ignored` command prints all ignored files, but you can't pipe it to `xargs rm -rf`, for example, because it prints other stuff too.

### Remove ignored files (`git-rm-ignored-files`)

Removes recursively all files and folders listed by `git-ls-ignored-files`.

### List old branches (`git-ls-old-branches`)

After a branch gets merged, you can delete it locally. This script lists all branches that don't exist anymore on remote.

### Remove old branches (`git-rm-old-branches`)

Removes all branches listed by `git-ls-old-branches`.

### Fuzzy-find file (`git-fzf`)

It's easier to find files in your git repository that way. It ignores what's on `.gitignore` too.

**Suggested usage:** `git-fzf | xargs -r vi` opens the file in vi.
