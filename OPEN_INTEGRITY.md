# Open Integrity

This repository uses [Open Integrity](https://github.com/OpenIntegrityProject) to establish a cryptographic root of trust for all commits.

## Inception Commit

The repository was initialized with a signed, empty inception commit that anchors the chain of trust for all subsequent commits.

| Field | Value |
|---|---|
| Commit | `6b851c1a9bc3ab4dfb16e18e132ab1fff5dd0481` |
| Signing key | `SHA256:MWgycszplTJXa3qjxeQabymJAxAiffHtlp/lz9fTX9g` |
| Date | 2026-03-07 |

## What This Means

- All commits in this repository are SSH-signed
- The inception commit establishes which keys are authorized to make commits
- Additional signers can be authorized via `.repo/config/verification/allowed_commit_signers`, which must itself be signed by the inception key or an already-authorized key
- Commit signatures can be verified independently of any hosting platform

## Verifying

```bash
git verify-commit 6b851c1a9bc3ab4dfb16e18e132ab1fff5dd0481
```

To verify all commits against the allowed signers file once it is established:

```bash
git log --show-signature
```
