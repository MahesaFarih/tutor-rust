<details>
<summary>Commit 1 Reflection</summary>
This milestone introduced the foundational structure of a web server in Rust, emphasizing TCP socket management and basic concurrency handling in a single-threaded environment. It highlighted Rust’s low-level networking capabilities and set the stage for improving performance in later milestones.

<details>
<summary>Commit 2 Reflection</summary>
This milestone transformed the server from a passive listener to an active responder, introducing foundational concepts of HTTP response construction and static content delivery. It emphasized protocol compliance and error-prone details like headers and line endings, setting the stage for more dynamic behavior in later milestones.

<details>
<summary>Commit 3 Reflection</summary>
This milestone introduced dynamic request handling, emphasizing path validation and appropriate HTTP responses. It laid the groundwork for more advanced features like concurrency (Milestone 5) and error handling.

<details>
<summary>Commit 4 Reflection</summary>

- Single-Threaded Servers Are Brittle: One slow request stalls the entire server.

- Concurrency Is Critical: To handle multiple users efficiently, tasks must run in parallel.

- Rust’s Safety: Even with blocking code, Rust’s ownership system prevents memory leaks or crashes during delays.


<details>
<summary>Commit 5 Reflection</summary>

### Why ThreadPool?
- Avoids the overhead of spawning unlimited threads (prevents DoS attacks).
- Balances performance and resource usage.

### Challenges:
- Understanding Rust’s concurrency primitives (Arc, Mutex, mpsc).
- Ensuring thread safety without data races.

### Key Learnings:
- How thread pools manage concurrent tasks efficiently.
- Rust’s compiler guarantees thread safety at compile time (e.g., Send and Sync traits).