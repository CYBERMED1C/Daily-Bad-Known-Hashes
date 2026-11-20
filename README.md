## Live status

**Latest published data:** [November 18, 2026](https://github.com/CYBERMED1C/Daily-Bad-Known-Hashes/blob/main/2026/11/18/evidence.csv)

- **Publication health:** 🟢 Published at 16:07 UTC. All three daily files and all three weekly files match the [GitHub data commit](https://github.com/CYBERMED1C/Daily-Bad-Known-Hashes/commit/e0da6d909e80ec18fa2719a72c4b1f13c061f3c4).
- **Hash validation health:** 🟢 All 15 SHA-256 hashes passed source, format, duplicate and cross-file checks. Reviewers found no unmodified legitimate tools among the listed files.
- **Research collection health:** 🟢 Every hash has delivery evidence from the preceding seven days and independent analysis. The review used public reports where URLscan and PyPI API records were unavailable.

**Daily schedule:** Active — 8:00 AM Pacific time (America/Los_Angeles).

> [!IMPORTANT]
> **TLP:CLEAR**
>
> Intelligence is drawn from publicly available sources. Use it for defensive investigation and assess every match in context.

# Daily Bad Known Hashes — Version 2.1.2

Verified SHA-256 hashes of malicious files with recent public malware-delivery evidence. This is a fresh collection; no data or history from the previous repository is imported.

## Structure

This example shows one collection date and its weekly folder.

```text
README.md
2026/
├── 11/
│   └── 11/
│       ├── sha256.txt
│       ├── comma-delimited list.txt
│       └── evidence.csv
└── 46th week of 2026/
    ├── sha256.txt
    ├── comma-delimited list.txt
    └── evidence.csv
```

Daily folders use the collection date in America/Los_Angeles. Weeks use ISO numbering, Monday through Sunday.

Each weekly list is the sorted, deduplicated union of that week's daily lists from this repository. Both text formats contain the same hashes in the same order. Weekly evidence contains one row per hash, retaining the latest review. No earlier dates are backfilled.

## Use

Import `sha256.txt` for one lowercase SHA-256 per line, or `comma-delimited list.txt` for one line separated by commas and spaces: `hash1, hash2, hash3`. Both lists contain exactly the same sorted hashes, with no trailing comma. Empty collections have empty list files. `evidence.csv` records provenance, behavior, confidence and the legitimate-tool review. It is not a blocklist.

Block only the exact listed file hashes. Check your approved software inventory and pilot in audit mode before enforcement; public evidence cannot guarantee zero false positives. These are dated snapshots: recheck older indicators before deployment. Remove a disputed hash from affected daily and weekly lists until resolved.
