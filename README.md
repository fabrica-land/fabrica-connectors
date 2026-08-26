# Connectors

**Connectors** are legal frameworks that bridge real property rights and their digital representations as onchain assets.

This repository contains the operating agreements used to create entity and non-entity wrappers that hold and represent real property rights onchain. The goal: owning the token means owning the property — delivered as the entire beneficial interest in a trust that holds title, with no intermediaries, notifications, or filings required after setup.

## Available Connectors

| Jurisdiction | Connector | Status |
|--------------|-----------|--------|
| United States | [Fabrica Trust Agreement](connectors/us/) | Active (v4.4) |

## The Fabrica Trust

The [Fabrica Trust Agreement](connectors/us/us-trust-agreement.md) is a nominee trust structure designed to hold real property and represent its ownership onchain. It has been under continuous development by Fabrica since 2017.

**Key features:**
- Token holder is always the beneficiary (owner) of the property
- Onchain transactions are the source of truth for ownership
- No third-party involvement in or control over the trust
- Works even if Fabrica disappears — the legal mechanism is self-contained

**v4.4 highlights:**
- Beneficial interest declared personal property in the land-trust tradition (§1.4): it passes by token assignment under §7, no deed required
- Financed-purchase "Qualified Designation" (§7.3(c)): beneficial ownership vests in the buyer at settlement even while the token sits in a lending pool or escrow
- Succession follows lawful key control (§7.6): a Key Successor operates immediately, with no ancillary situs probate
- Unsolicited-transfer doctrine (§7.7): presumptive defeasible vesting with an onchain disclaimer (return or burn), retroactive to receipt
- Full UCC Article 9/12 build-out (§§11.1–11.9): collateral is the token, never the land; two-lane priority; fallback where Article 12 is not enacted
- Texas hardening (active-trust duties, anti-merger, homestead/occupancy) and a plain-language "How This Trust Works" summary

## Repository Structure

```
connectors/
└── us/
    ├── us-trust-agreement.md   # The trust agreement (current version)
    ├── CHANGELOG.md            # Version history and changes
    └── README.md               # US trust details and key terms
CLAUDE.md                       # Repository conventions
DISCLAIMER.md                   # Legal disclaimer
LICENSE                         # CC0 1.0
README.md                       # This file
```

## Learn More

- [Fabrica Documentation](https://docs.fabrica.land) — Protocol overview and implementation details
- [Legal Wrappers Guide](https://docs.fabrica.land/docs/legal-wrappers) — Deep dive on the trust structure

## Disclaimer

These materials are for informational purposes only and do not constitute legal advice. See [DISCLAIMER.md](DISCLAIMER.md) for full terms.
