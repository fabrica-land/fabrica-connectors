# Connectors

**Connectors** are legal frameworks that bridge real property rights and their digital representations as onchain assets.

This repository contains the operating agreements used to create entity and non-entity wrappers that hold and represent real property rights onchain. The goal: owning the token means owning the property, with no intermediaries, notifications, or filings required after setup.

## Available Connectors

| Jurisdiction | Connector | Status |
|--------------|-----------|--------|
| United States | [Fabrica Trust Agreement](connectors/us/) | Active (v4.3) |

## The Fabrica Trust

The [Fabrica Trust Agreement](connectors/us/us-trust-agreement.md) is a nominee trust structure designed to hold real property and represent its ownership onchain. It has been under continuous development by Fabrica since 2017.

**Key features:**
- Token holder is always the beneficiary (owner) of the property
- Onchain transactions are the source of truth for ownership
- No third-party involvement in or control over the trust
- Works even if Fabrica disappears — the legal mechanism is self-contained

**v4.3 highlights:**
- Involuntary loss of title (§10.5): automatic dissolution when record title leaves the Trust by external operation of law (tax sale, foreclosure, eminent domain, etc.); bearer-token wind-up authority and proceeds entitlement; judicial reinstatement if the operative instrument is later set aside
- Two-tier recovery mechanism for lost keys or death (no stuck assets)
- Anti-merger hardening (Beneficial Interest Holders, springing Continuity Trustee)
- Production-readiness: sworn-affidavit form for universal county-recorder acceptance
- UCC Article 12 integration for secured lending
- Smart Wallet support (multisig, account abstraction)

## Repository Structure

```
connectors/
├── us/
│   ├── us-trust-agreement.md   # The trust agreement (current version)
│   ├── CHANGELOG.md            # Version history and changes
│   └── README.md               # US trust details and key terms
├── DISCLAIMER.md               # Legal disclaimer
└── README.md                   # This file
```

## Learn More

- [Fabrica Documentation](https://docs.fabrica.land) — Protocol overview and implementation details
- [Legal Wrappers Guide](https://docs.fabrica.land/docs/legal-wrappers) — Deep dive on the trust structure

## Disclaimer

These materials are for informational purposes only and do not constitute legal advice. See [DISCLAIMER.md](DISCLAIMER.md) for full terms.
