# git-fxwt

`git fxwt` is a Git sub-command wrapper around `git worktree` designed for Firefox development. It automatically deploys your dotfiles into each new worktree, making it easy to maintain consistent configurations across multiple worktrees.

## Usage example

### 1. Init Firefox worktree

```bash
~$ mkdir firefox

~$ cd firefox

~/firefox$ git fxwt init
Initializing Firefox worktree...
Cloning into bare repository '.git'...
...
Creating dotfiles directory...
Created dotfiles directory
Initialized Firefox worktree
IMPORTANT: Copy your dotfiles into ~/firefox/dotfiles before adding worktrees
```

### 2. Copy dotfiles

```bash
~/firefox$ cp ~/.mozconfig ~/firefox/dotfiles
```

### 3. Create new worktree

```bash
~/firefox$ git fxwt add test-worktree -b test-branch
Preparing worktree (new branch 'test-branch')
...
Copying dotfiles into worktree test-worktree...
Copied dotfiles/.mozconfig into test-worktree/.mozconfig
```

## Configuration

Add the script directory to the `PATH` environment variable.
