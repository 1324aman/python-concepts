## UUID
- uuid is universal unique identifier.
- It is of 32 chars.

## How uuid is created
- Different versions of uuids are created in different ways.
- version 1 uses current time and mac address to create uuid
- versino 2 are almost similar to version1 with a small change, but they are not preffered.
- version 3 uses MD5 (message digest algorithm) to created uuids.
- version 4 is created by random alpha numerics.
- version 5 uses SHA-1 hash algorithm.
- there are few more versions, not very much useful.

## Which version should we use
- If you don’t know what to go with, go with v4. It’s good enough, and the chances of collision are practically none.

- If you actually want your UUID to give some indication of the date and computer in which it was created, then UUID v1 may be for you (although it is).

- UUID v5 is normally used only for very specific use cases, when you want to derive a UUID from another piece of information on the fly.
