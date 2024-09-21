# Redis with Go

## 1. In-Memory Data Store
Sartch stores all data in memory, ensuring lightning-fast read and write operations. It's ideal for use cases that demand real-time performance, such as caching and session storage.

## 2. Concurrency with Go
Sartch leverages Go's built-in goroutines to handle thousands of concurrent connections effortlessly. This design makes Sartch highly scalable and efficient in managing client requests and commands.

## 3. Data Structures
Sartch supports essential Redis-like data structures:

- **Strings**: For key-value storage
- **Hashes**: For storing collections of key-value pairs
- **Lists**: For ordered lists of strings
- **Sets**: For unordered collections of unique strings
- **Sorted Sets**: For sorted collections of unique strings with scores

These data structures are implemented using Go's native types, ensuring efficient memory usage and fast operations.

## 4. Persistence
Sartch offers two methods for data persistence:

- **RDB (Redis Database)**: Periodically saves snapshots of the dataset to disk.
- **AOF (Append Only File)**: Logs every write operation for data recovery.

This ensures data durability, preventing data loss even in the event of a server crash.

## 5. Lightweight Communication Protocol
Sartch implements Redis's lightweight communication protocol, **RESP** (REdis Serialization Protocol), for client-server communication. It manages TCP connections efficiently using Go’s `net` package, ensuring low-latency interactions with minimal overhead.
