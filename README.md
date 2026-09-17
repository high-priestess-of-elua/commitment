# Signed commitment — Vanessa Kosoy

This repository holds a PGP-signed copy of a public commitment I made, so that it can be verified independently of any website.

## Files

- `commitment.txt` — the commitment text
- `commitment.txt.asc` — the same text, clearsigned with my PGP key
- `pubkey.asc` — my PGP public key

## Key

Fingerprint: `9B8B 9C42 C44E 5B92 9A4B DA3D 88C3 7785 C7AA BCC8`

The same key is published at:

- https://coral-research.org/vanessa-kosoy/ (under "PGP key")
- https://github.com/high-priestess-of-elua.gpg

## Verify

```
gpg --import pubkey.asc
gpg --fingerprint 88C37785C7AABCC8     # must match the fingerprint above
gpg --verify commitment.txt.asc
```

## Timestamp

`commitment.txt.asc.ots` and `pubkey.asc.ots` are [OpenTimestamps](https://opentimestamps.org) proofs anchoring the SHA-256 hashes of the corresponding files in the Bitcoin blockchain. They show the files existed no later than the block they are anchored in, without relying on any organization.

```
ots verify commitment.txt.asc.ots
ots verify pubkey.asc.ots
```

(A proof created on 2026-09-17 was submitted to the calendar servers that day and upgraded to a Bitcoin attestation once confirmed. `ots verify` needs a Bitcoin node or, with `--no-bitcoin`, falls back to trusting a block explorer.)

## Provenance

- Original statement: https://www.lesswrong.com/posts/dPmmuaz9szk26BkmD?commentId=ZLGLCgPb6JYibsQHu
- Internet Archive snapshots (2026-09-17):
  - https://web.archive.org/web/20260917124032/https://coral-research.org/vanessa-kosoy/
  - https://web.archive.org/web/20260917124357/https://github.com/high-priestess-of-elua.gpg
  - https://web.archive.org/web/20260917124420/https://www.lesswrong.com/posts/dPmmuaz9szk26BkmD?commentId=ZLGLCgPb6JYibsQHu
