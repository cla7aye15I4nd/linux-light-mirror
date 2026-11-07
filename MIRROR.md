# Linux light mirror

This repository is a space-efficient source snapshot of
[`torvalds/linux`](https://github.com/torvalds/linux). It is intended for tools
that need the current Linux source tree but do not need the kernel's full Git
history.

The `main` branch contains exactly one reachable commit. A scheduled GitHub
Action checks upstream daily and force-replaces `main` with a new orphan commit
when `master` changes. The snapshot commit records the upstream repository,
ref, full commit SHA, commit date, and subject. The same full SHA is stored in
[`.upstream-commit`](.upstream-commit).

Because updates intentionally replace history, existing clones should fetch and
reset to `origin/main` rather than merge. Use the upstream repository when you
need Linux development history, tags, or stable branches.

The mirrored Linux source retains its upstream licensing and notices.
