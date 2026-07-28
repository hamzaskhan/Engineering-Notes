# JWT

Draft note.

JWTs are often described as "stateless auth." That only goes so far once you need logout, revoke, or role changes.

Rough pattern I use:

```text
Access token  → short-lived JWT
Refresh token → opaque, stored server-side
```

Still figuring out when a plain session is simpler.
