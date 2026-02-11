# Changelog
### Fabrica Trust

#### v4.2 (draft)

**Production-readiness hardening (Sections 10.2, 10.3, 11.6, 12.3–12.4):** Operational and recordation changes to support deed-out actions at scale across multiple jurisdictions:

- **Recordation hardening (Section 10.2):** If the county recorder refuses to accept the Notice of Lost Token Control, the Beneficiary must proceed to the court-ordered path under Section 10.4. Contest mechanism broadened from "counter-notice" to any instrument permitted by applicable recording statutes (lis pendens, affidavit of adverse claim, or equivalent). If contested, process halts and routes to Section 10.4. Notice delivery expanded to include known lienholders and encumbrance holders in addition to the Property address
- **Succession evidence gating (Section 10.3.2):** Proof of legal succession must now be valid under the laws of the jurisdiction where the Property is located. If the legal successor cannot obtain sufficient proof, mandatory fallback to court-ordered dissolution under Section 10.4
- **Real-property law savings clause (Section 11.6):** Explicit statement that UCC Article 12 "control" does not displace real-property recording statutes, deed requirements, or title-vesting rules. Token control determines rights in the token as a CER, but transfer of record title requires a deed satisfying applicable real-property law
- **Situs-law and venue preservation (Sections 12.3–12.4):** California governing-law clause now expressly preserves mandatory situs-state rules for conveyancing, recording, lien priority, and probate. Venue clause preserves jurisdiction in the Property's location for quiet title, foreclosure, and similar real-property actions

#### v4.1 (draft)

**Anti-merger hardening (Sections 2.26, 6.2, 7.1, 8.1, 12.5–12.7):** Structural changes to defend against the doctrinal argument that merger of legal and equitable interests collapses the Trust when the Beneficiary also serves as Trustee:

- **Beneficial Interest Holders (Section 2.26):** New defined term recognizing that equitable interests in the Trust are held not only by the present Beneficiary but also by determinable future Beneficiaries (via token transfer, Smart Wallet transfer, or explicit assignment under Section 7.3(b)(ii)) and legal successors (via Section 10.3). Explicitly preserves tax pass-through treatment
- **Beneficiary definition (Section 2.3):** Clarified as referring to the present interest holder; cross-references the broader Beneficial Interest Holders class
- **Owner Rights qualification (Section 6.2):** "Absolute, sole, and uncontrolled" now expressly scoped to the present Beneficiary's exercise of rights during their period of ownership, and does not extinguish contingent equitable interests
- **Trustee fiduciary scope (Section 7.1):** Trustee duties now expressly run to all Beneficial Interest Holders, with future/contingent interests limited to preservation of the trust res — no present right of action or control granted except narrow procedural standing to petition for Continuity Trustee appointment under Section 12.6
- **Trustee obligations (Section 8.1.1):** Trustee acts for the benefit of all Beneficial Interest Holders
- **Anti-merger savings clause (Section 12.5):** If any provision would cause merger, it is automatically construed/reformed to preserve trust continuity to the minimum extent required
- **Springing Continuity Trustee (Section 12.6):** If a court finds merger, a temporary special trustee activates solely to preserve the trust res. Beneficiary-directed appointment, no platform dependency, no standing professional trustee, no discretion over distributions. Terminates automatically on transfer, new trustee appointment, or dissolution
- **Tax treatment (Section 12.7):** Explicit statement that contingent future interests do not alter pass-through treatment

#### v4.0

**Alternative dissolution (Sections 10.2–10.5):** Three new paths to dissolve the Trust when the Beneficiary cannot Redeem the Property Token:
- **Uncontested recovery (10.2):** Record a Notice of Lost Token Control at the county → 90-day Quiet Period → Deed of Distribution. The process runs entirely through public records with no intermediary required. An eligibility gate protects lenders: if the token is in a Functional Contract (lending, escrow), the Beneficiary must first cause it to be returned
- **Estate succession (10.3):** Same process, with the legal successor (executor, heir) stepping in using probate documents. Successors who inherit wallet access need no special process
- **Court-ordered dissolution (10.4):** Fallback for theft, disputes, or contested claims. Court order substitutes for the burn requirement
- **Void Token (10.5):** After alternative dissolution, the token continues to exist onchain but confers no rights. Control of a Void Token confers no property interest under UCC Article 12

**Smart Wallet support:**
- Introduced "Smart Wallet" (multisig, account-abstraction wallets) and "Functional Contract" (escrow, bridges, lending) as short-form defined terms (Section 2.6)
- All references to the holder of the Property Token now consistently use "Account or Smart Wallet" and "private keys or signing credentials" where applicable
- Smart Wallet DoS prevention: only transactions where the Smart Wallet successfully executes an outbound action halt the Quiet Period — external calls to the wallet do not

**Unauthorized transfers and lender protection (Sections 7.5, 11.4):**
- A Transfer resulting from theft or key compromise does not transfer beneficial ownership; the prior Beneficiary retains Owner Rights
- Protected secured party provision extends qualifying purchaser protection to good-faith lenders who take a security interest without notice of the unauthorized Transfer

**Other changes:**
- **Section 7.1:** Trustee default rule — unless separately appointed, the Beneficiary is deemed to be the Trustee
- **Section 6.3:** Fractionalization governance is governed by a separate agreement; this Agreement applies to fractional owners as a group
- **Section 3.1.3:** Conveyance deed attachment is optional (facilitates validation but not required for legal effectiveness)
- **Section 8.1.3:** Trustee liability limited to willful misconduct or gross negligence
- **Section 4.1:** Digital signature equivalence applies "to the maximum extent permitted by applicable law"
- **Definitions (Section 2):** Added Alternative Dissolution Event, Notice of Lost Token Control, Quiet Period, Void Token; clarified Beneficiary definition to account for functional contract custody, unauthorized transfers, and loss of token control
- **Readability:** Shorter sentences, bullet-point formatting, consistent terminology throughout

IPFS CID: `bafkreigc4ckzv5agna3tohs5tcqvvze6wgu7oocj5ecpqcg3gxaspyxpue`

#### v3.7

- Adopted UCC Article 12 as primary framework, designating Property Tokens as controllable electronic records (CERs)
- Added explicit definition of Article 12 "control" requirements and how blockchain mechanisms satisfy them
- Smart contracts may serve as control mechanisms; programmed restrictions do not defeat control
- Enforcement standards in smart contracts are agreed standards under UCC § 9-603, with explicit preservation of non-waivable debtor rights under § 9-602
- Added qualifying purchaser provision enabling take-free transfers for good faith buyers
- Retained Article 8 as supplementary framework when tokens are held through securities intermediaries with express agreement
- Resolved CER/investment property conflict: token is CER except when held as Article 8 financial asset
- Clarified that UCC treatment does not affect securities law classification
- Reframed deed validity as Trustee condition precedent (shall not execute unless token burned) rather than deed invalidity
- Trust termination now requires deed in recordable form with cryptographically signed authorization from last token controller
- Simplified termination language using "burn" for clear onchain verification

#### v3.6

- Enhanced clarity around token custody vs. beneficial ownership
- Improved consistency in terminology around token operations
- Added explicit conditions for beneficial ownership changes
- Strengthened legal language regarding Contract Account interactions

#### v3.5

- Definitions: switched from `burn` to `redeem` to improve the readability of the Trust Agreement.

#### v3.4

- Definitions: moved from *Fabrica Smart Contracts* and *Fabrica NFTs* to more generic un-branded definitions.
- Generalized language to abstract the underlaying blockchain used,  primarily intended to support L2s and bridging assets across different chains.

#### v3.3

- Added UCC article 8 opt-in, bolstering ability to create security interests in tokens when used as collateral.

#### v3.2

- Updated definitions around finality to reflect latest developments of Ethereum.

#### v3.1

- Incorporated references to and consideration of fractional ownership.
- Bolstered transfer definitions, including the concept that movement from one address to another does not necessarily equate a transfer.

#### v3.0

- Major redesign for new protocol version.
- Primary focus to rely as heavily as possible on onchain data. Removed all data inputs, and replaced with definitions pointing to relevant onchain locations.
- Converted from a custodial system to self-custody.
- Removed all signature lines and created definitions around finality and reliance on blockchain signatures exclusively.
- Improved fraud prevention.



| Version | IPFS CID                                         | HTTP Link                                                    |
| ------- | ------------------------------------------------ | ------------------------------------------------------------ |
| 4.0     | `bafkreigc4ckzv5agna3tohs5tcqvvze6wgu7oocj5ecpqcg3gxaspyxpue` | https://ipfs.fabrica.land/ipfs/bafkreigc4ckzv5agna3tohs5tcqvvze6wgu7oocj5ecpqcg3gxaspyxpue |
| 3.7     | `bafkreielajiqjyqjwofuxaep6heoxx6ag4ifum7u6mafvkkhuif2dcqvc4` | https://ipfs.fabrica.land/ipfs/bafkreielajiqjyqjwofuxaep6heoxx6ag4ifum7u6mafvkkhuif2dcqvc4 |
| 3.6     | `bafkreifiv6x6a77v6gnjxw3tfxo5exzo736x6fvr2inx46qpn3woemgxky` | https://ipfs.fabrica.land/ipfs/bafkreifiv6x6a77v6gnjxw3tfxo5exzo736x6fvr2inx46qpn3woemgxky |
| 3.5     | `QmNxY3ooc4VXbW6ETd1wVAxvajZYWu81U95MmWJiNBQw14` | https://ipfs.fabrica.land/ipfs/QmNxY3ooc4VXbW6ETd1wVAxvajZYWu81U95MmWJiNBQw14 |
| 3.4     | `QmeRZqhU59Vpn4JQvggBVQ97uMfmS68utweUury8n5JLPR` | https://ipfs.fabrica.land/ipfs/QmeRZqhU59Vpn4JQvggBVQ97uMfmS68utweUury8n5JLPR |
| 3.3     | `Qmf6Aia6gJfRgGyGroYft3kjxsLUhJEhMYVKPKj2JwY41Z` | http://ipfs.fabrica.land/ipfs/Qmf6Aia6gJfRgGyGroYft3kjxsLUhJEhMYVKPKj2JwY41Z |
| 3.2     | `QmcgEJkgCwizvs6Tu12jCaNMGciRNtH8dLA2TRS3aYWStX` | https://ipfs.fabrica.land/ipfs/QmcgEJkgCwizvs6Tu12jCaNMGciRNtH8dLA2TRS3aYWStX |
| 3.1     | `QmXRQx7wPxSwQDVVr1pTkiwvBHBUd1SYLbLgSn1Bvirqpc` | https://ipfs.fabrica.land/ipfs/QmXRQx7wPxSwQDVVr1pTkiwvBHBUd1SYLbLgSn1Bvirqpc |
| 3.0     | `QmRH7d7TGJ3DymLSRimjnH5cNGHzYfcvUTUA1tM9gizFY8` | http://ipfs.fabrica.land/ipfs/QmRH7d7TGJ3DymLSRimjnH5cNGHzYfcvUTUA1tM9gizFY8 |

