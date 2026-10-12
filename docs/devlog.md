# NOVA Dev Log

A day-by-day record of what I did on NOVA. Newest entry at the top.
Things I learned and mistakes I made go in [learnings.md](learnings.md).

---

## Day 1: 12 Oct 2026

**Focus:** Project planning and repository foundation

### What I did
- Broke NOVA into 10 phases (0 to 9), from foundations to a documented, deployable platform.
- Chose Go as the main language and VS Code as the editor.
- Checked my Git setup and set the default branch name to `main`.
- Created the GitHub repository and cloned it to my machine.
- Created the folder structure, README, MIT license, `.gitignore`, and the design and ADR templates.
- Made the first commit and pushed it to GitHub.
- Installed Go 1.27.2 and the Go extension for VS Code.
- Created the Go module and ran my first Go program.
- Made a second commit and pushed it.

### Foundations laid

| Foundation | What it is | Why it matters |
|---|---|---|
| Git and GitHub repo | Version history, backed up online | Every change is recorded and can be undone |
| `README.md` | Project overview, status, phase table | The front page for anyone visiting the repo |
| `LICENSE` (MIT) | Terms for using the code | Without a license, others can't legally reuse it |
| `.gitignore` | Files Git must never track | Keeps binaries, logs, and editor files out of history |
| `docs/design/` and `docs/adr/` | Templates for design docs and decision records | Every component gets planned and every decision explained |
| `docs/roadmap.md` | Phase tracking | Shows progress and what is next |
| `docs/learnings.md` | Personal learning journal | Records understanding, not just output |
| `docs/devlog.md` | This file | Daily record of work |
| `playground/` | Practice programs | Keeps learning code separate from the real system |
| `go.mod` | The Go module definition | Required before any Go code can be built |

### Problems I hit
- My local `Nova` folder was created by hand, so it had no `.git` folder. I fixed it by cloning into the empty folder with `git clone <url> .`
- The first `go run` was slow because Go had to compile its standard library for the first time.

### Commits
- `chore: initial repo structure`
- `feat(playground): init Go module and add hello program`

### Next
- Work through the Basics section of the Tour of Go.
- Write a practice program in `playground/tour-basics`.