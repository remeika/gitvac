# gitvac
Boldly clean your local git repo.

A tiny script based on an [SO answer](https://stackoverflow.com/a/38404202/2701578) that deletes any local orphaned git branches. gitvac will:

- Not touch any branches that also exist on your remote
- Delete any branches that _used_ to exist on your remote, but no longer do
- Not touch any branches that have never been pushed to remote

## Installation

1. Copy the `gitvac` file to a directory that is on the `PATH`. For MacOS users, `~/bin` is a good choice.
2. Make sure its executable: `$ chmod +x gitvac`

## Usage

Make sure the current directory is within the git repo you want to clean. Then:

```
$ gitvac
From github.com:remeika/my-dirty-repo
 - [deleted]             (none)     -> origin/branch-a
 - [deleted]             (none)     -> origin/branch-b
 - [deleted]             (none)     -> origin/branch-c
 - [deleted]             (none)     -> origin/branch-d
 - [deleted]             (none)     -> origin/branch-e
 - [deleted]             (none)     -> origin/someone-elses-branch

Deleted branch branch-a (was f19320e5f).
Deleted branch branch-b (was ed3646685).
Deleted branch branch-c (was b00f7a368).
Deleted branch branch-d (was 12a8460f1).
Deleted branch branch-e (was 3d223e150).
```