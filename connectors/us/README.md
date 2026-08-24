# Fabrica Trust Agreement (US)

A legal framework for operating on real estate using smart contracts by holding title in a nominee trust.

> **Quick links:**
> - [Trust Agreement (v4.4)](us-trust-agreement.md) — The current version
> - [Changelog](CHANGELOG.md) — Version history and detailed changes

## Overview

The Fabrica Trust is a nominee trust where the token holder is always the beneficiary (owner). The trust holds a single piece of real property, and owning the Property Token means owning the property — no intermediaries required.

The trust is created under California law but has been used across multiple US states. The design allows the beneficiary to serve as their own trustee, leaving no doubt that the token holder owns the property.

## Design Principles

| Principle | Implementation |
|-----------|----------------|
| **Token = Title** | Owning the Property Token confers full beneficial ownership of the property |
| **Onchain Truth** | The blockchain is the authoritative record of ownership |
| **No Gatekeepers** | The trust works even if Fabrica disappears |
| **Self-Custody** | The beneficiary controls their own keys and their own property |
| **Interoperability** | Works with lending protocols, escrow, bridges, and smart wallets |

## Key Concepts

### Beneficiary & Trustee

- **Beneficiary**: The token holder — has all economic rights, controls the property, responsible for taxes and obligations
- **Trustee**: The titleholder of record — acts at the beneficiary's direction. Unless separately appointed, the beneficiary is deemed to be the trustee

### Account Types (Section 7.3)

| Type | Examples | Effect on Ownership |
|------|----------|---------------------|
| **Account (EOA)** | Standard wallet | Owner of the wallet is the Beneficiary |
| **Smart Wallet** | Multisig, Safe, account-abstraction wallets | Controller(s) of the wallet are the Beneficiary(ies) |
| **Functional Contract** | Lending protocol, escrow, bridge | Custody only — original Beneficiary retains ownership |

### Trust Dissolution (Section 10)

The trust can be dissolved in several ways:

1. **Standard (10.1)**: Burn the token → Trustee executes deed
2. **Uncontested Recovery (10.2)**: Lost keys? Record a Notice at the county → wait 90 days → execute deed. No intermediary required
3. **Estate Succession (10.3)**: Same as 10.2, but the legal successor (executor, heir) steps in with probate documents
4. **Court Order (10.4)**: For theft, disputes, or contested claims — court order substitutes for the burn requirement
5. **Involuntary Loss of Title (10.5)**: When record title leaves the Trust by external operation of law (tax sale, foreclosure, eminent domain, etc.), the Trust dissolves automatically on recording of the operative instrument and the token becomes a Void Token. The Trust continues for a limited wind-up purpose to collect any residual proceeds; if the operative instrument is later set aside by a court, the Trust is reinstated as of the original recording date

### UCC Article 12 (Section 11)

The Property Token is a "controllable electronic record" under UCC Article 12. This enables:
- Secured lending with the token as collateral
- Qualifying purchaser protection for good-faith buyers
- Clear priority rules for competing claims

## Version History

See [CHANGELOG.md](CHANGELOG.md) for the complete history. Major versions:

| Version | Highlights |
|---------|------------|
| **4.4** | Beneficial interest as personal property (land-trust tradition); financed-purchase Qualified Designation; succession via lawful key control; unsolicited-transfer disclaimer; full UCC Article 9/12 build-out; Texas passive-trust and merger hardening |
| **4.3** | Involuntary loss of Property title: automatic dissolution on tax sale, foreclosure, eminent domain, etc.; bearer-token wind-up authority and proceeds entitlement; judicial reinstatement on operative-instrument reversal |
| **4.2** | Production-readiness hardening: sworn-affidavit form for county recording, situs-law preservation, real-property savings clause |
| **4.1** | Anti-merger hardening: Beneficial Interest Holders, Springing Continuity Trustee |
| **4.0** | Alternative dissolution (recovery mechanism), Smart Wallet support, UCC Article 12 integration |
| **3.7** | UCC Article 12 as primary framework |
| **3.0** | Self-custody redesign, onchain-first architecture |

## Learn More

- [Fabrica Documentation](https://docs.fabrica.land) — Protocol overview
- [Legal Wrappers Guide](https://docs.fabrica.land/docs/legal-wrappers) — Deep dive on the trust structure

## Disclaimer

These materials are for informational purposes only and do not constitute legal advice. See [DISCLAIMER.md](../../DISCLAIMER.md) for full terms.
