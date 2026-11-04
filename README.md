# Phantom bootstrap manifest

This repository carries the **signed** bootstrap manifest used by Phantom
clients when their usual address is blocked. It contains no secrets: the
payload is public by design and is only trusted after its Ed25519 signature
is checked against the key compiled into the app.

- key id: `boot-2026-01`
- public key: `a7006f6e0ed23dbacc694150b4c99b63afa01aff06eecd356406219a0e193f53`
- artifact: `manifest.txt` (one `bootstrap/1` line, then the signed envelope)

Do not hand-edit `manifest.txt`. It is produced by `pt-bootstrap sign` and
published by `pt-bootstrap publish`; a changed byte invalidates the signature
and clients will reject it.
