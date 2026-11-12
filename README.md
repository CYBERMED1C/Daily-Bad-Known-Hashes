# Daily-Bad-Known-Hashes

**Version 2.1.1 · Collection started November 11, 2026**

Verified SHA-256 hashes of malicious files with recent public malware-delivery evidence. This is a fresh collection; no data or history from the previous repository is imported.

## Structure

```text
README.md
2026/
├── 11/
│   └── 11/
│       ├── sha256.txt
│       └── evidence.csv
└── 46th week of 2026/
    ├── sha256.txt
    └── evidence.csv
```

Daily folders use the collection date in America/Los_Angeles. Weeks use ISO numbering, Monday through Sunday. November 11 is in week 46, November 9–15; this first collection covers November 11 onward. Future weekly folders follow the same naming pattern.

Each weekly list is the sorted, deduplicated union of that week's daily lists from this repository. Its evidence contains one row per hash, retaining the latest review. No earlier dates are backfilled.

## Collection and verification

Every accepted hash must pass all checks:

1. A primary source documents the exact SHA-256 as a delivered malware payload within the preceding seven days. A new upload or a recent article alone is insufficient.
2. A separate analysis provider identifies the same submitted file and records malicious behavior. A vendor detection count alone is insufficient.
3. Review the file's role and legitimate-use risk. Exclude genuine operating-system files, administration/security tools, unmodified dependencies, test files and ambiguous samples, even when attackers use them.
4. Verify the 64-character hexadecimal value, remove duplicates and retain dated source links and limitations in `evidence.csv`. Hold anything that cannot be checked.

The initial collection uses URLhaus delivery evidence and independent Hatching Triage analysis. URLhaus records were available through the public search index; that limitation is recorded per hash. Source dates describe reported delivery, not continuous activity or newly created malware.

## Use

Import only `sha256.txt`: one lowercase SHA-256 per line. `evidence.csv` records provenance, behavior, confidence and the legitimate-tool review. It is not a blocklist.

Block only the exact listed file hashes. Check your approved software inventory and pilot in audit mode before enforcement; public evidence cannot guarantee zero false positives. These are dated snapshots: recheck older indicators before deployment. Remove a disputed hash from affected daily and weekly lists until resolved.
