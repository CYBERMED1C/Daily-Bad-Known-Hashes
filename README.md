## Live status

🟢 **Healthy and operational**

**Latest report:** [November 13, 2026](https://github.com/CYBERMED1C/Daily-Bad-Known-Hashes/blob/main/2026/11/13/evidence.csv).

**Last successful IOC publication:** Confirmed 2026-11-13 16:03 UTC (data commit; minute precision).

**Overall health:** The 2026-11-13 collection contains 5 validated SHA-256 malware hashes. Research, independent review, data validation, publication and GitHub readback checks passed. All five have matching vendor hash attribution and independently analyzed malicious code; coverage is limited to one recent campaign. The preferred daily count is not a verification requirement.

**Daily schedule:** Active — 8:00 AM Pacific time (America/Los_Angeles).

> [!IMPORTANT]
> **TLP:CLEAR**
>
> Intelligence is drawn from publicly available sources. Use it for defensive investigation and assess every match in context.

# Daily Bad Known Hashes — Version 2.1.2

Verified SHA-256 hashes of malicious files with recent public malware-delivery evidence. This is a fresh collection; no data or history from the previous repository is imported.

## Structure

```text
README.md
2026/
├── 11/
│   ├── 11/
│   │   ├── sha256.txt
│   │   ├── comma-delimited list.txt
│   │   └── evidence.csv
│   ├── 12/
│   │   ├── sha256.txt
│   │   ├── comma-delimited list.txt
│   │   └── evidence.csv
│   └── 13/
│       ├── sha256.txt
│       ├── comma-delimited list.txt
│       └── evidence.csv
└── 46th week of 2026/
    ├── sha256.txt
    ├── comma-delimited list.txt
    └── evidence.csv
```

Daily folders use the collection date in America/Los_Angeles. Weeks use ISO numbering, Monday through Sunday. November 11 is in week 46, November 9–15; this first collection covers November 11 onward. Future weekly folders follow the same naming pattern.

Each weekly list is the sorted, deduplicated union of that week's daily lists from this repository. Both text formats contain the same hashes in the same order. Weekly evidence contains one row per hash, retaining the latest review. No earlier dates are backfilled.

## Collection and verification

Every accepted hash must pass all checks:

1. A primary source documents the exact SHA-256 as a delivered malware payload within the preceding seven days. A new upload or a recent article alone is insufficient.
2. A separate analysis provider identifies the same submitted file and records malicious behavior. A vendor detection count alone is insufficient.
3. Review the file's role and legitimate-use risk. Exclude genuine operating-system files, administration/security tools, unmodified dependencies, test files and ambiguous samples, even when attackers use them.
4. Verify the 64-character hexadecimal value, remove duplicates and retain dated source links and limitations in `evidence.csv`. Hold anything that cannot be checked.

The initial collection uses URLhaus delivery evidence and independent Hatching Triage analysis. URLhaus records were available through the public search index; that limitation is recorded per hash. Source dates describe reported delivery, not continuous activity or newly created malware.

The November 12 review also checked recent vendor investigations, government advisory searches and malware-delivery records. One additional file met the verification standard. Its independent Hatching Triage and Joe Sandbox findings were reproduced on an exact-hash MalwareBazaar entry available through the public search index; the full provider reports were inaccessible. Recent SCKit components and other candidates lacking separate exact-file analysis were held. That publication brought the weekly union to 3 hashes. Coverage limitations and conflicting verdicts are recorded in the evidence.

The November 13 review added five custom SCKit files tied to the November 11 deliveries documented by Huntress. Blackpoint independently recovered and analyzed the same exact hashes. Legitimate ScreenConnect and SQLite files, demonstration payloads, and unsupported components were excluded or held. These indicators describe malicious code and attempted propagation; neither vendor established successful technician compromise, patch bypass or complete propagation. Other vendor, government and delivery-record searches did not yield additional fully supported pairs. The weekly union contains 8 hashes; prior daily archives remain unchanged.

## Use

Import `sha256.txt` for one lowercase SHA-256 per line, or `comma-delimited list.txt` for one line separated by commas and spaces: `hash1, hash2, hash3`. Both lists contain exactly the same sorted hashes, with no trailing comma. Empty collections have empty list files. `evidence.csv` records provenance, behavior, confidence and the legitimate-tool review. It is not a blocklist.

Block only the exact listed file hashes. Check your approved software inventory and pilot in audit mode before enforcement; public evidence cannot guarantee zero false positives. These are dated snapshots: recheck older indicators before deployment. Remove a disputed hash from affected daily and weekly lists until resolved.
