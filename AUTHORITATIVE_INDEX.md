# Authoritative Index

## This repository

speedkit.eu is the **authoritative index** for:
- System discovery URLs
- System status (live/discontinued)
- Canonical system names

## Authoritative files

| File | Authority |
|------|-----------|
| `index.html` | System listing |
| `INDEX_CHECKSUM.txt` | Index integrity |
| `DEPRECATION.md` | Retention policy |

## Non-authoritative

- Styling (CSS)
- README
- System descriptions (summaries only)

## Related systems

| System | Relationship |
|--------|--------------|
| VERIFRAX | Listed system |
| MK10-PRO | Listed system |
| VATFIX | Listed system |

## Verification

```bash
sha256sum index.html
cat INDEX_CHECKSUM.txt
```

## Policy

- Append-only (no deletions)
- No deprecation (DEPRECATION: NEVER)
- No interaction (static read-only)
