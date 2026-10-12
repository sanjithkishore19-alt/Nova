# NOVA

NOVA is a distributed computing platform that runs tasks across multiple workers, built from scratch to detect failures and recover from them automatically.

## Why this project exists

I'm building NOVA to learn how distributed systems actually work, by implementing the core pieces myself instead of relying on existing frameworks. The goal is a working, well-documented platform with measurable performance, and a deep understanding of operating systems, networking, concurrency, databases, and fault tolerance along the way.

## Current status

**Phase 0: Foundations.** Setting up the repository and building small practice programs (TCP server, concurrent key-value store) before starting the real system.

## Planned phases

| Phase | Focus | Status |
|---|---|---|
| 0 | Foundations (sockets, concurrency, KV store) | In progress |
| 1 | Single-node execution engine | Not started |
| 2 | Persistent job storage | Not started |
| 3 | Distributed architecture | Not started |
| 4 | Failure detection and recovery | Not started |
| 5 | Replication and consensus (Raft) | Not started |
| 6 | Distributed file storage | Not started |
| 7 | Monitoring and performance | Not started |
| 8 | Containerization, deployment, interface | Not started |
| 9 | Hardening and write-up | Not started |

## How to build and run

Nothing to run yet. This section will be filled in as components are built.

## Repository layout

- `docs/` holds the roadmap, design documents, architecture decision records, and my learning journal.
- `playground/` holds small practice programs from Phase 0, kept separate from the real system.