# Changelog — Malicious Domain Threat Intelligence Feed

## [2026-01-15] — Automated Pipeline Launch

### Added
- Automated 12-hour collection pipeline
- Multi-source: URLhaus, PhishTank, AlienVault OTX, Spamhaus DBL, Disconnect.me
- Validation: VirusTotal, Talos, URLScan.io
- Deduplication with Bloom filter + Git history
- Partition management (100K domains/file)

### Statistics
| Feed | Before | Added | After |
|------|--------|-------|-------|
| Total Domains | 135,000 | 3,700+ | 138,700+ |

---

## [2025-11-01] — Source Expansion

### Added
- PhishTank verified phishing feed
- Spamhaus DBL integration
- Disconnect.me tracking domains

### Statistics
| Feed | Before | Added | After |
|------|--------|-------|-------|
| Total Domains | 52,000 | 83,000 | 135,000 |

---

## [2025-05-01] — Initial Release

### Added
- URLhaus malware URL → domain extraction
- Basic repository structure and documentation