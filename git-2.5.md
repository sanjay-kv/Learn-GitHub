# 🚀 Git 2.50 Release Notes – What’s New?  

Hello and welcome to Git 2.50, the world’s favorite distributed version control system! In this update, 98 developers contributed—35 of them for the very first time. 🎉

No matter if you’re wrangling giant monorepos, fine-tuning your CI/CD pipelines, or just hacking on your next open source project, Git 2.50 brings some cool new features and improvements to make your workflow smoother, faster, and easier.

---

## 🌟 Quick Highlights

Here’s a peek at what’s new:

- 🧹 Better cruft pack management (clean up made easier!)
- 📦 Faster, smarter multi-pack reachability bitmaps
- 🔀 The ORT merge engine is now the default (goodbye, old merge headaches)
- 🛠 More `git maintenance` tasks and configuration options
- 🗑 You can now delete reflog entries directly
- 📚 Speedier reference operations
- 🌐 Advanced HTTP keepalive controls
- 🐪 Less dependence on Perl
- 🧾 Clearer rebase interactions
- 🧩 Improvements to sparse checkout
- 🌍 Faster cloning with bundle-URI
- 📅 Upcoming Git Merge 2025 Conference
- 🔗 And more! (See resources below)

---

## 🧹 Cruft Pack Management Just Got Smarter

Ever wondered what happens to unreachable objects (the stuff not linked from any branch or tag)? Git uses something called “cruft packs” to hold onto those for a while, just in case you need them. With Git 2.50, managing these packs is even easier:

- **New flag:** `--combine-cruft-below-size=<size>` lets you merge small cruft packs together, so you don’t end up with a mess of tiny files.
- **Clearer behavior:** `--max-cruft-size` now only affects the new cruft pack being written, so it’s less confusing.
- **Bug fix:** Unreachable objects now keep their correct timestamps, so you don’t accidentally lose them too soon.

---

## 📦 Incremental Multi-Pack Reachability Bitmaps

If you have a giant repo, you’ll love this: Git can now build “reachability bitmaps” across multiple pack files incrementally. That means:

- Faster cloning, pushing, and pulling.
- Less time spent re-writing everything when new objects arrive.
- It’s still experimental, but if you work with huge repos or CI pipelines, keep an eye on this!

---

## 🔀 The ORT Merge Engine Is Now Default

Merging is faster and uses less memory, especially in big or complex repositories. The ORT merge engine (introduced in Git 2.33) officially replaces the old “recursive” strategy. Fewer merge headaches for everyone.

---

## 🛠 `git maintenance` – Now Even More Helpful

The `git maintenance` command helps keep your repo healthy automatically. New in 2.50:

- **New tasks:** Clean up stale worktrees, expire old conflict resolutions, and tidy up reflogs.
- **New config:** Control how many loose objects get packed together with `maintenance.loose-objects.batchSize`.

---

## 🗑 Delete Reflog Entries Directly

Reflogs track every change to your branches. Until now, deleting entries was a pain. Now it’s as simple as:

```sh
git reflog delete <branch>
```
No more complicated commands!

---

## 📚 Reference Handling Is Speedier

- Reference checks are smarter and faster, especially if you have a ton of branches or tags.
- Git avoids unnecessary checks and reuses iterators for better performance behind the scenes.

---

## 🌐 Fine-Tune HTTP Keepalive

If you use Git over HTTP/S (like in CI systems or slow networks), you now have more control:

```sh
http.keepAliveIdle     # Time before Git sends the first keepalive probe
http.keepAliveInterval # How often it checks in
http.keepAliveCount    # How many times it tries before giving up
```

---

## 🐪 Less Perl, More Portability

Git is moving away from Perl scripts. If your system doesn’t have Perl, tests that depend on it are simply skipped now, instead of failing.

---

## 🧾 Easier Interactive Rebase

When you use `git rebase -i`, commit messages in the todo list now show up as comments—making it clearer what’s happening as you edit.

---

## 🧩 Sparse Checkout Improvements

You can now use `git add -p` and `git add -i` with sparse-indexes. That means you can interactively stage changes even in huge repos, without loading everything.

---

## 🌍 Faster Cloning with Bundle-URI

Cloning from a Git bundle file is now faster and more complete—Git will advertise all available refs, not just branches.

---

