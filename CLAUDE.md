# Style Guide

## Terminology

- **onchain** — one word, no hyphen. Not "on-chain."
- **offchain** — one word, no hyphen. Not "off-chain."

## Trust Agreement: Key Design Concepts

The Fabrica trust agreement (currently v4.0) is the legal instrument that governs the relationship between a real property and its token. Key design principles:

### Recovery Mechanism (Section 10)

The trust agreement includes a two-tier recovery mechanism for when token control is lost (lost keys, stuck contracts, death):

- **Tier 1 (Uncontested):** Record a Notice of Lost Token Control at the county, wait 90 days, deliver a sworn certificate, Trustee executes a Deed of Distribution. Self-service, no gatekeeper required.
- **Tier 2 (Contested):** Court order required. For theft, disputes, or when the token moves during Tier 1's quiet period.

### Key Sections to Know

| Section | What it covers |
|---|---|
| 2.3 | Beneficiary definition (the person identified by the Fabrica validator as the owner of the wallet holding the token) |
| 7.3(a) | Custody Contract Accounts (wallets, multi-sig, custody solutions controlled by the Beneficiary) |
| 7.3(b) | Functional Contract Accounts (lending, escrow, collateral, bridges) where custody does not confer ownership |
| 8.2 | Trustee reliance safe harbor (can rely on recorded documents without independent blockchain investigation) |
| 10.1 | Standard dissolution (burn token, get deed) |
| 10.2 | Alternative dissolution (recovery mechanism). Eligibility gate requires token in EOA or 7.3(a), not 7.3(b) |
| 10.2.3 | Token movement during quiet period halts the process |
| 10.2.4 | Sworn certificate delivered to Trustee after quiet period |
| 10.3 | Estate succession provisions |
| 10.3.2 | Legal successor files Notice with letters testamentary |
| 10.3.3 | Legal successor steps into Beneficiary position for Deed of Distribution |
| 10.3.4 | Heirs who inherit key access exercise Owner Rights directly |
| 10.5.2 | Offchain records (confidence scores) are administrative convenience, not legally required |
| 11.4 | UCC Article 12 qualifying purchaser protection |

### Design Principles

- **Walk-away independence:** Everything must work if Fabrica disappears. No gatekeeper, no admin key, no trust protector.
- **Separation of concerns:** The trust agreement governs the property-token relationship. Wallet security (key management, 2FA) is a wallet-layer concern. Lending protocol risk management (borrower verification) is a protocol-layer concern. The trust agreement is the wrong layer for any of these.
- **Eligibility gate protects lenders structurally:** Token in a 7.3(b) lending contract cannot enter Tier 1. The borrower must pay off the loan first. This works with any lending protocol because it is based on onchain token location.
- **Void token = confidence score at 1:** Onchain, a token is just a token. "Void" is a legal concept communicated via the confidence score. Validators see the recorded Deed of Distribution and permanently set the recovery digit to 1.
- **Confidence score is a risk signal, not a legal determination:** Computed by independent validators, exposed offchain (APIs) and sometimes onchain (oracles). The trust agreement does not depend on any specific validator.

### Writing About the Trust Agreement

- Reference specific section numbers when discussing provisions.
- The Beneficiary is defined in Section 2.3, not by wallet address alone. The validator's identification matters.
- "Notice of Lost Token Control" is the formal name for the Tier 1 filing. It is a sworn document recorded at the county.
- The 90-day quiet period starts from recording, not from filing.
- The trust agreement uses "Property Token," "Beneficiary," "Trustee," "Account," "Contract Account" as defined terms. Use them consistently.
