# Code 401 - Reading Notes

<!-- All references used were from Code 401 reading
assignment 29 -->
[comment]: <> (https://developer.android.com/training/data-storage/room)

[comment]: <> (https://developer.android.com/training/data-storage/room/defining-data)

[comment]: <> (https://developer.android.com/training/data-storage/room/relationships)

[comment]: <> (https://developer.android.com/training/data-storage/room/accessing-data#java)

## Room
Apps that handle non-trivial amounts of structured data can benefit greatly from persisting that data locally. The most common use case is to cache relevant pieces of data so that when the device cannot access the network, the user can still browse that content while they are offline.

The Room persistence library provides an abstraction layer over SQLite to allow fluent database access while harnessing the full power of SQLite. In particular, Room provides the following benefits:

Compile-time verification of SQL queries.
Convenience annotations that minimize repetitive and error-prone boilerplate code.
Streamlined database migration paths.
Because of these considerations, we highly recommend that you use Room



[BACK TO HOME](../README.md)