# Contributing to Malicious Domain Threat Intelligence Feed

## Ways to Contribute

1. **Report False Positives** — Use issue template
2. **Submit New Malicious Domains** — Use IOC submission template
3. **Request Tool Integrations** — Use integration request template
4. **Improve Documentation** — Submit PRs

## Domain Format Requirements

### Valid
```
evil-phishing-site.com
malware-c2-domain.ru
fake-banking-login.net
sub.domain.example.com
```

### Invalid
```
http://evil-domain.com          ← no protocol
evil-domain.com/login           ← no URL paths
*.evil-domain.com               ← no wildcards (strip *.)
EVIL-DOMAIN.COM                 ← no uppercase (lowercase only)
evil-domain.com:8080            ← no ports
```

### Validation Checklist
- [ ] Plain domain only (FQDN)
- [ ] Lowercase
- [ ] No protocol prefix
- [ ] No URL path
- [ ] No wildcard prefix
- [ ] Verified on VirusTotal (≥3 detections) or PhishTank/URLScan.io

## Automated Pipeline

Updates every 12 hours from:
- URLhaus (malware URLs → domains)
- PhishTank (verified phishing)
- AlienVault OTX (pulses)
- Spamhaus DBL
- Disconnect.me (tracking)

25 new domains selected per cycle.

## License

MIT License — contributions licensed under MIT.