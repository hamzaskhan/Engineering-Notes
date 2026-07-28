# Redis

Draft note.

I try not to think of Redis as "makes things faster," and more as moving a consistency boundary (staleness, invalidation, failure modes).

```mermaid
flowchart LR
  API --> Cache{Redis}
  Cache -->|hit| Client
  Cache -->|miss| DB[(Mongo)]
  DB --> Cache
```

Main footgun for me: caching aggregates without a clear invalidation owner.
