[Basically an implementation in C from scratch of my HTTP Server in Rust](https://github.com/saumayrustagi/http_server_rust)

- [x] Use Memory Arenas for serving requests.
- [x] Port from mutex+cond to semaphores.
- [ ] Serve files directly (like images, videos)

# Web Server in C

Project to learn how multithreading, threadpools, function pointers and manually-managed memory works in C.

## Implemented Components

* **Task Queue:** A thread-safe queue to store incoming tasks (client connections) awaiting processing.

* **Thread Pool:** A pool of worker threads that retrieve tasks from the queue and execute them in parallel.

* **Web Server:** The core server component responsible for listening for incoming connections, accepting them, and enqueuing them as tasks for the thread pool.

## Building

```bash
git clone https://github.com/saumayrustagi/http_server_c.git
cd http_server_c
```

### Prerequisites

* `clang`/`gcc` (change in `Makefile` as suitable)
* `make`
* `glibc`

### Debug Mode (Sanitizers)

```bash
make            # Builds the project in debug mode
./main.out      # Runs the server with sanitizers enabled
```

### Release Mode (-O2)

```bash
make fast       # Builds the project in release mode
./fast_main.out # Runs the server with optimizations
```

## Demo

https://github.com/user-attachments/assets/23dd1ef1-e6bf-436f-b1a1-f011d6c85f30
