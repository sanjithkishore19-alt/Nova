# ADR-001: Use Go as the main language

Date: 12 Oct 2026
Status: accepted

## Context
NOVA needs strong support for concurrency and networking, because it will run many tasks at once across many workers. I have no prior Go experience, so the language also has to be learnable alongside the project.

Alternatives considered:
- **Rust:** very strong guarantees and low-level control, but a steep learning curve that would slow down learning the distributed systems concepts themselves.
- **C++:** the most control, but manual memory management and many pitfalls would pull attention away from the core ideas.
- **Python:** quick to write, but weaker for concurrency and performance-sensitive work, and it hides details I want to understand.

## Decision
Use Go for all main NOVA components. Small C programs are allowed for operating-system experiments (for example in Phase 1).

## Consequences
- **Easier:** goroutines and channels make concurrency straightforward. The standard library handles networking well. Real systems like Kubernetes, Docker, and etcd are written in Go, so their source is useful reading.
- **Harder:** I need a few weeks to learn Go before Phase 0 can really start. Go hides some low-level details such as manual memory management.
- **Giving up:** the fine-grained control that C, C++, or Rust would offer.