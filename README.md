## Live status

🟢 **Healthy and operational**

**Latest report:** [November 18, 2026](https://github.com/CYBERMED1C/Daily-Bad-Known-Hashes/blob/main/2026/11/18/evidence.csv).

**Last successful IOC publication:** Confirmed 2026-11-18 16:07 UTC (data commit; minute precision).

**Overall health:** The 2026-11-18 collection contains 15 validated new SHA-256 malware hashes, published in the dated data commit. Research, independent review, data validation and committed-file readback checks passed. Ten poisoned web responses have November 13–16 HTTP delivery captures and separate exact-file analysis. Five agent-framework files have documented November 17 live-package acquisition and independent code analysis; victim installs are not established. Historical web-body findings are credited to Kirk/Ohey and hash-corroborated by Hudson Rock. Public report HTML was available; URLscan full-result JSON returned HTTP 403 and PyPI version JSON returned HTTP 404. These are dated observations, with no claim of present availability or victim compromise. Other candidates were held or excluded where required evidence or legitimate-use review was incomplete.

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
