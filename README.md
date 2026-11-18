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
│   ├── 13/
│   │   ├── sha256.txt
│   │   ├── comma-delimited list.txt
│   │   └── evidence.csv
│   ├── 14/
│   │   ├── sha256.txt
│   │   ├── comma-delimited list.txt
│   │   └── evidence.csv
│   ├── 15/
│   │   ├── sha256.txt
│   │   ├── comma-delimited list.txt
│   │   └── evidence.csv
│   ├── 16/
│   │   ├── sha256.txt
│   │   ├── comma-delimited list.txt
│   │   └── evidence.csv
│   ├── 17/
│   │   ├── sha256.txt
│   │   ├── comma-delimited list.txt
│   │   └── evidence.csv
│   └── 18/
│       ├── sha256.txt
│       ├── comma-delimited list.txt
│       └── evidence.csv
├── 46th week of 2026/
│   ├── sha256.txt
│   ├── comma-delimited list.txt
│   └── evidence.csv
└── 47th week of 2026/
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

The November 13 review added five custom SCKit files tied to the November 11 deliveries documented by Huntress. Blackpoint independently recovered and analyzed the same exact hashes. Legitimate ScreenConnect and SQLite files, demonstration payloads, and unsupported components were excluded or held. These indicators describe malicious code and attempted propagation; neither vendor established successful technician compromise, patch bypass or complete propagation. Other vendor, government and delivery-record searches did not yield additional fully supported pairs. That publication brought the weekly union to 8 hashes; prior daily archives remained unchanged.

The November 14 review added 12 files across two supply-chain campaigns. Aikido and Endor bind the wfx script to November 10 delivery and credential theft. For Ethersphere, public capture records and independent code analysis establish November 9 delivery of the modified bee-js loader, wallet-stealing JavaScript, four custom Go backdoors, and the trojanized Swarm Desktop amd64 Debian package and its nested Electron archive. The package and archive are separate file indicators in one chain. Older backdoor analysis dates are distinguished from fresh delivery, and no present availability is claimed. Benign decoys, unmodified remote-management software, uninspected installers and unsupported indicators were excluded or held. That publication brought the weekly union to 20 hashes.

The November 15 review added one Mozi ELF file observed in URLhaus delivery records on November 14. Independent Triage input-hash tables and successful behavioral runs identify the same exact file and show scanning, watchdog tampering and persistence. The sandbox evidence was reviewed through public search-index snapshots; direct reports were inaccessible. The older file bytes qualify through freshly researched delivery evidence. Broader vendor, government and delivery-record research did not establish additional complete pairs: Agent Tesla, GCleaner, ClickFix, GeoVision and Moldova campaign candidates were held where required evidence was missing; older-delivery campaigns, mining tools, a legitimate driver and a test file were excluded. That publication completed week 46 with 21 hashes; earlier daily data remained unchanged.

The November 16 review begins ISO week 47 with one Macfinger Bash installer. SANS documents the exact script in a November 11 ClickFix delivery; an independent Triage report submitted November 15 records the same input hash and commands for concealed payload staging and attempted shell-history removal. The source gives no delivery timezone, so the UTC delivery field is empty; all possible adjacent UTC dates still fall within the seven-day window. Triage ran the script on Linux, where the payload download failed, so this record does not claim macOS payload execution or credential theft. Broader current vendor, government and delivery-record searches did not establish additional complete pairs. Unsupported new payloads, older-delivery investigations, ordinary software, security tools and test or cleanup artifacts were held or excluded. That publication began week 47 with 1 hash; week 46 remained unchanged at 21.

The November 17 review added eight OPTIMJACK JavaScript files: one theft payload, one minute-ly loader and six poisoned Optimizely project assets. November 16 URLscan HTTP response metadata binds each exact file to delivery. Separate Hudson Rock analysis identifies malicious code in those bytes. Only the poisoned variants are included; clean vendor assets and genuine dependencies are excluded. Government, vendor and delivery-record coverage also considered Gootloader, FaceStealer, Retadup/CoffeeLoader, Trigram, Phantom53, Agent Tesla and package-malware reports. Candidates lacking a qualifying recent exact-file delivery and separate analysis pair were held. The URLscan full-result JSON API returned HTTP 403; public report HTML supplied response hashes, status, dates and page context. Captures and static analysis do not prove victim compromise or continued availability. That publication brought week 47 to 9 hashes; week 46 remained unchanged at 21.

The November 18 review added 15 files across two supply-chain campaigns. Ten poisoned web responses comprise eight JavaScript files and two JSON widgets with injected loaders. Primary browser-capture metadata records exact response hashes, HTTP 200 status, dates and legitimate page context; the separate Hudson Rock report publishes Kirk/Ohey's body analysis and corroborates those hashes. The earlier BBC variant is distinct from the later embedded-fallback variant, and the legitimate Confiant initiator is excluded. Five agent-framework indicators identify two malicious wheels and three malicious internal Python files from the November 17 PyPI compromise. Firsthand live acquisition and dated vendor analysis establish package delivery, without establishing victim installs; separate providers bind the same files to credential theft or its loader. Bare-import PTH hooks, unchanged metadata, clean files and ordinary dependencies are excluded. Broader government, vendor and delivery-record research did not establish further qualifying pairs. URLscan full-result JSON returned HTTP 403, while public HTML provided response metadata; removed PyPI versions returned HTTP 404 from the version JSON endpoint. Week 47 now contains 24 hashes; week 46 remains unchanged at 21.

## Use

Import `sha256.txt` for one lowercase SHA-256 per line, or `comma-delimited list.txt` for one line separated by commas and spaces: `hash1, hash2, hash3`. Both lists contain exactly the same sorted hashes, with no trailing comma. Empty collections have empty list files. `evidence.csv` records provenance, behavior, confidence and the legitimate-tool review. It is not a blocklist.

Block only the exact listed file hashes. Check your approved software inventory and pilot in audit mode before enforcement; public evidence cannot guarantee zero false positives. These are dated snapshots: recheck older indicators before deployment. Remove a disputed hash from affected daily and weekly lists until resolved.
