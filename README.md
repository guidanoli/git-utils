# Utilities for Git

## List ignored files (`git-ls-ignored-files`)

The `git status --ignored` command prints all ignored files, but you can't pipe it to `xargs rm -rf`, for example, because it prints other stuff too.

**Suggested usage:** `git-ls-ignored-files | xargs -d '\n' rm -rf`

## List old branches (`git-ls-old-branches`)

After a branch gets merged, you can delete it locally. This script lists all branches that don't exist anymore on remote.

**Suggested usage:** `git-ls-old-branches | xargs -d '\n' git branch -D`
