# Fabrica Trust Agreement (US)

A legal framework for operating on real estate using smart contracts by holding title in a nominee trust.

> **Quick links:**
> - [Trust Agreement (v4.4)](us-trust-agreement.md) — The current version
> - [Changelog](CHANGELOG.md) — Version history and detailed changes

## Overview

The Fabrica Trust is a nominee trust where the token holder is always the beneficiary (owner). The trust holds a single piece of real property, and owning the Property Token carries the entire beneficial interest in the trust that holds title — every practical right of ownership, no intermediaries required.

The trust is created under California law but has been used across multiple US states. The design allows the beneficiary to serve as their own trustee, leaving no doubt that the token holder owns the property.

## Design Principles

| Principle | Implementation |
|-----------|----------------|
| **Token → Trust → Title** | Owning the Property Token carries the entire beneficial interest in the trust that holds title — every practical right of ownership, one transfer |
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

## Questions lawyers and registries ask

Short answers, each pointing at the operative text. Read the agreement; this is a map, not a substitute.

**What kind of asset is the Property Token?** A "controllable electronic record" under UCC Article 12 (Section 11.1). Article 12 governs the token as a record. It does not, of its own force, carry the beneficial interest: "the parties do not assert that UCC Article 12, of its own force, transfers the Beneficial Interest" (Section 11.7).

**What kind of asset does the holder own?** The Beneficial Interest in the trust that holds title. It is declared personal property, "an interest in the Trust, and not an estate or interest in land", in the tradition of the American land trust (Section 1.4), and a "general intangible" under UCC § 9-102(a)(42) (Section 11.7). It is not a controllable account or a controllable payment intangible: no one owes a monetary obligation.

**Which law moves the Beneficial Interest when the token moves?** The agreement itself, as a matter of trust law and party agreement. Each valid Transfer of the token effects "the full assignment of all interests, rights, duties, liabilities, and obligations under the Trust" (Section 7.2); the Beneficial Interest "passes by assignment under Section 7 upon each valid transfer of beneficial ownership, without a deed" (Section 1.4(a)); the token is "the authoritative record and instrument of transfer" (Section 1.4). The agreement and the trust's internal affairs are governed by California law (Section 12.3). Record title to the land moves only by a recorded deed under the real-property law of the situs (Sections 11.6, 11.8).

**Where does Article 12 come in?** As the third-party layer. A qualifying purchaser takes the token free of property claims to it under UCC § 12-104(e); and the agreement, as a term of the trust, gives a person with control the power to transfer the Beneficial Interest to a qualifying purchaser and makes every holder's interest defeasible in that purchaser's favour (Sections 11.4.2, 11.4.3). That power rests on trust law and is preserved as "law other than UCC Article 12" under UCC § 12-104(f); the statute does not supply it. The agreement designates California as the token's jurisdiction under UCC § 12-107(c)(1) (Sections 11.1, 11.9.1). Where no enactment of Article 12 applies, the assignment mechanics do not depend on it; "only the third-party negotiability layer varies" (Section 11.9.2).

**How does a lender perfect?** The collateral is the token and, where expressly granted, the Beneficial Interest; "no mortgage, deed of trust, lien, or other security interest in the Property itself is created" (Section 11.2). A security interest attaches under UCC § 9-203; a Confirmed Transaction and its signed records "may constitute an authenticated security agreement" (Section 11.2). A security interest in the token is perfected by control (UCC §§ 9-107A, 12-105, 9-314) or by filing; a smart contract holding the token "may serve as a method of obtaining and evidencing 'control'" (Section 11.2). The agreement "does not deem control of the Property Token to perfect a separately granted security interest in the Beneficial Interest if applicable law requires another method of perfection for that collateral" (Section 11.2), so a lender taking the Beneficial Interest as collateral perfects it as applicable law provides, ordinarily by filing.

**What happens on default?** UCC Article 9 Part 6, on the token: enforcement and disposition "are governed by UCC §§ 9-610 through 9-624, including the notification standards of UCC §§ 9-611 through 9-614"; nothing in the agreement "constitute[s] post-default consent to acceptance of collateral in satisfaction of an obligation under UCC § 9-620" or waives the debtor's right to redeem under UCC § 9-623 (Section 11.2). Whoever becomes the rightful holder takes the Beneficial Interest through Section 7 and Section 11.7. The agreement does not vary mandatory law that, by the substance of a financing secured by a Beneficiary's homestead or occupied residence, applies homestead-lending, mortgage-foreclosure, redemption, anti-deficiency, or consumer-protection rules (Section 11.2).

**Can the holder amend or cancel the agreement?** Cancel, yes: the Beneficiary may dissolve the trust by burning the token and directing a deed out (Sections 6.1, 10.1). Amend, no: the Token ID is "generated based on the digital signature of multiple fields from the Token Metadata, including the precise language of this Agreement" (Section 2.17), so the text is fixed when the trust is created; a new version is a new trust.

**What if the keys are lost, or someone falsely claims them?** Section 10.2: a sworn Notice of Lost Token Control recorded at the county and indexed against the Trust (Section 2.23); within ten days, certified mail to the property and assessee addresses, every recorded lienholder, and every UCC secured party of record, plus a Confirmed Transaction sent onchain to the Account holding the token (Section 10.2.1); a ninety-day Quiet Period (Section 2.24) during which any interested party may contest by recording an instrument (Section 10.2.2) and any Confirmed Transaction originating from the holding Account halts the process (Section 10.2.3); then a sworn certificate and a Deed of Distribution (Sections 10.2.4 to 10.2.6).

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
