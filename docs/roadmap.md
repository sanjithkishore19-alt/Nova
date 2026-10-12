# NOVA Roadmap

Tick items off as they are finished. Detail for later phases gets added when I reach them.

Last updated: 12 Oct 2026

## Phase 0: Foundations (current)
- [x] Create GitHub repo, folder structure, README, license, `.gitignore`
- [x] Write design and ADR templates
- [x] Write ADR-001 (use Go)
- [x] Install Go and the VS Code Go extension
- [x] Initialize the Go module and run a first program
- [ ] Tour of Go: Basics
- [ ] Tour of Go: Methods, interfaces, generics
- [ ] Tour of Go: Concurrency
- [ ] Practice program: TCP echo server
- [ ] Practice program: multi-client chat server
- [ ] Write design doc for the in-memory key-value store
- [ ] Build a thread-safe key-value store with a simple text protocol
- [ ] **Milestone:** KV server handles 100 concurrent clients with no data races

## Phase 1: Single-node execution engine
- [ ] Task model, priority queue (own heap), worker pool
- [ ] Run tasks as separate OS processes with timeouts
- [ ] Task dependencies (DAG) and retries with backoff
- [ ] **Milestone:** 10,000 tasks survive random worker kills with nothing lost

## Phase 2: Persistent job storage
- [ ] Job state machine, write-ahead log, crash recovery
- [ ] **Milestone:** recovers a consistent state after 1,000 random crashes

## Phase 3: Distributed architecture
- [ ] Coordinator and workers over TCP, own RPC layer, heartbeats, leases
- [ ] **Milestone:** a real workload runs across 3-5 machines or VMs

## Phase 4: Failure detection and recovery
- [ ] Failure detectors, task reassignment, fault-injection harness
- [ ] **Milestone:** hours-long chaos test with exactly-once effect

## Phase 5: Replication and consensus (Raft)
- [ ] Leader election, log replication, snapshots, replicated coordinator
- [ ] **Milestone:** cluster survives repeated leader kills

## Phase 6: Distributed file storage
- [ ] Chunking, replication, re-replication, consistent hashing
- [ ] **Milestone:** file survives two chunk-server failures

## Phase 7: Monitoring and performance
- [ ] Metrics, logging, tracing, dashboard, load testing
- [ ] **Milestone:** benchmark report with bottlenecks found and fixed

## Phase 8: Containerization, deployment, interface
- [ ] Docker, Compose, CI, API, CLI, web UI
- [ ] **Milestone:** one command brings up a working cluster

## Phase 9: Hardening and write-up
- [ ] Final docs, architecture document, demo, technical report