# NOVA Learnings

What I understood, what I got wrong, and what surprised me. Newest entry at the top.
What I did each day is in [devlog.md](devlog.md).

---

## Day 1: 12 Oct 2026

### What clicked
- Git has three areas: the working folder, the staging area, and the history. `git add` moves files into staging and `git commit` saves them as a snapshot. Nothing reaches GitHub until `git push`.
- Git tracks files, not folders, so an empty folder like `playground/` is invisible to it until a file goes inside.
- `.gitignore` has to be in place before the first commit. Once a file is in history, ignoring it later doesn't remove it.
- A design doc is written before building a component. An ADR is written when a decision is made. They answer different questions: "how will it work?" and "why did I choose this?"
- Every Go program starts in `package main` at `func main()`, and Go refuses to build if an import is unused.

### Mistakes and surprises
- My local `Nova` folder had no `.git` inside, because I had created it as a plain folder instead of using `git clone`. `git status` failed with "not a git repository". Fix: `git clone <url> .` into the empty folder.
- The first `go run` took a long time because Go compiles its standard library the first time. Later runs were fast.
- The warning "LF will be replaced by CRLF" looked alarming but is only Windows and Git translating line endings.

### Still unclear
- I'm still unsure about the git commands and the git folders terminologies 