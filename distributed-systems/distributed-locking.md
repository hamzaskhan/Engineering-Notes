# Distributed locking

Draft note.

Locks without ownership + expiry tend to go badly.

Often a unique constraint in the DB is enough; Redis lock is for fast fail, not the source of truth.
