# 🚀 Git 2.50 Release Notes

Welcome to **Git 2.50**, the latest release of the world’s most popular distributed version control system! This version includes contributions from **98 developers**, **35 of whom are new** 🎉.

Whether you’re managing massive monorepos, fine-tuning your DevOps pipelines, or contributing to open source, Git 2.50 packs powerful updates to help you scale, automate, and debug more efficiently.

---

## 🧵 Peak view of what changed with Git 2.5
- [🧹 Better Cruft Pack Management](#-better-cruft-pack-management)
- [📦 Incremental Multi-Pack Reachability Bitmaps](#-incremental-multi-pack-reachability-bitmaps)
- [🔀 Merge Engine: ORT by Default](#-merge-engine-ort-by-default)
- [🛠 git maintenance: More Tasks & Configs](#-git-maintenance-more-tasks--configs)
- [🗑 Reflog: Now Supports Delete](#-reflog-now-supports-delete)
- [📚 Reference Performance Improvements](#-reference-performance-improvements)
- [🌐 Advanced HTTP Keepalive Controls](#-advanced-http-keepalive-controls)
- [🐪 Reduced Perl Dependency](#-reduced-perl-dependency)
- [🧾 UI/UX: More Clear Rebase Interactions](#-uiux-more-clear-rebase-interactions)
- [🧩 Sparse Checkout Improvements](#-sparse-checkout-improvements)
- [🌍 Faster Bundle-URI Clones](#-faster-bundle-uri-clones)
- [📅 Git Merge 2025 Conference](#-git-merge-2025-conference)
- [🔗 Additional Resources](#-additional-resources)

---

## 🧹 Better Cruft Pack Management

Git introduced *cruft packs* in v2.37 to manage unreachable objects more efficiently. These are objects not reachable from any ref (branches, tags, etc.), but still stored temporarily to avoid data loss.

### 🆕 Improvements in 2.50:
- `--combine-cruft-below-size=<size>`: 
  - 💡 New flag to **combine cruft packs** smaller than the given size into a single pack.
  - Helps reduce fragmentation from many small cruft packs.
- `--max-cruft-size`:
  - 🔄 Behavior updated to **only** control the size of the newly written cruft pack (previously, it also governed selection, which caused confusion).
- 🐛 Bug fix: Unreachable objects now correctly have their modification times refreshed when rewritten, preventing premature deletion.

---

## 📦 Incremental Multi-Pack Reachability Bitmaps

### 🧠 Background:
- Git’s *multi-pack index (MIDX)* allows Git to treat multiple `.pack` files as one, speeding up object lookups.
- *Reachability bitmaps* accelerate operations like cloning and pushing by precomputing which objects are reachable from certain commits.

### 🚀 What’s New:
- Support for **incremental multi-pack bitmaps** across layered MIDX files.
- Each layer in an incremental MIDX now gets its own `.bitmap`, enabling Git to append new objects and bitmaps without rewriting everything.
- ⚠️ Still **experimental**, but crucial for performance in massive monorepos and CI pipelines.

---

## 🔀 Merge Engine: ORT by Default

- The **ORT merge engine** (Ostensibly Recursive’s Twin), first introduced in Git 2.33, continues to **replace the older "recursive" strategy**.
- ORT is **faster and more memory-efficient**, particularly in large repos with frequent merges and complex histories.

---

## 🛠 `git maintenance`: More Tasks & Configs

The `git maintenance` command, which automates background tasks like cleaning and optimizing repositories, is now more powerful.

### 🆕 New Maintenance Tasks:
- `worktree-prune`: Removes stale/broken worktrees (like `git gc`).
- `rerere-gc`: Expires old conflict resolution entries.
- `reflog-expire`: Removes stale unreachable objects from reflog history.

### 🔧 New Config:
- `maintenance.loose-objects.batchSize`: Controls the number of objects per pack when rewriting loose objects (previously hardcoded to 50,000).

---

## 🗑 Reflog: Now Supports `delete`!

Reflogs track changes to references (like branches). You can use them to restore deleted commits or navigate history.

### Before:
```sh
git reflog expire <branch> --expire=all  # cumbersome
```

### Now:
git reflog delete <branch>  ✅  # intuitive and clear

### 📚 Reference Performance Improvements
Git handles millions of references in large-scale repos. This release includes several low-level optimizations:

git update-ref no longer checks if a refname is a valid SHA1/ID (it’s low-level; trust the caller).

Efficient prefix conflict checks prevent accidental nesting (e.g., refs/foo blocking refs/foo/bar).

Reuses reference iterators instead of reinitializing them for each prefix check. ⚡️ Faster ref operations!


### 🌐 Advanced HTTP Keepalive Controls
When using Git over HTTP/S, especially in CI/CD or across slow networks, keepalive settings matter.

### 🆕 New Config Options:


```sh
http.keepAliveIdle     # Time (sec) before sending first probe
http.keepAliveInterval # Interval (sec) between probes
http.keepAliveCount    # Max number of probes before giving up

```


### 🐪 Reduced Perl Dependency
Git continues removing legacy Perl from its test suite and tooling.

Most Perl one-liners now replaced with shell or C.

If Perl isn’t available on your system, tests depending on it are now skipped instead of failing.


### 🧾 UI/UX: More Clear Rebase Interactions
When running git rebase -i, commit messages in the TODO list now appear as comments:
```sh
pick c108101daa # Fix: add auth check
pick d2a0730acf # Refactor: update utils


```
### 🧩 Sparse Checkout Improvements
git add -p and git add -i now fully support sparse-indexes.

You can interactively stage partial changes without expanding the entire index — faster and more efficient for large projects.


### 🌍 Faster Bundle-URI Clones
Git bundles package your repo (objects + refs) into a single .bundle file for offline or partial cloning.

Git 2.50 now advertises all refs from the bundle in the fill-in fetch, not just refs/heads/*.

Result: faster and more complete cloning when using bundle-uri.
