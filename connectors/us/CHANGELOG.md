# Changelog
### Fabrica Trust

#### v4.3

**Involuntary loss of Property title (new Section 10.5, related cross-reference updates):** New Alternative Dissolution Event covering the case where record title leaves the Trust by external operation of law without Trustee or Beneficiary consent — tax sale, judicial or nonjudicial foreclosure, eminent domain, escheat, or court-confirmed adverse possession. Closes a documented gap in v4.2: previously, the Trust would lose its corpus to such events but the agreement was silent on termination, leaving the Property Token alive onchain with no clean dissolution mechanism.

- **Automatic dissolution (Section 10.5):** When the entirety of the Property is transferred out of the Trust by operation of law through an "Operative Instrument" executed by a third party (tax collector, sheriff, condemning authority, etc.), the Trust dissolves automatically upon recording of the Operative Instrument and the Property Token becomes a Void Token. No Deed of Distribution and no Trustee action required. The recorded Operative Instrument substitutes for both the Section 1.2(a) condition precedent and the Section 10.1.2 cryptographic signature requirement. Examples enumerated include tax deed, sheriff's deed, trustee's deed upon sale, foreclosure instruments (judicial or nonjudicial), order of condemnation, escheat, and adverse possession adjudications
- **Partial transfers (Section 10.5.1):** An Operative Instrument affecting less than the entirety of the Property does not dissolve the Trust. The Trust continues with respect to the remaining Property; partial-transfer proceeds flow to the Beneficiary under Section 10.7
- **Wind-up via bearer-token mechanic (Section 10.5.2):** Notwithstanding the dissolution, the Trust continues in existence for the limited purpose of pursuing claims and collecting/distributing residual proceeds (tax-sale surplus, condemnation awards, refunds, insurance recoveries). The person who from time to time holds the Property Token has wind-up authority and proceeds entitlement — as a representative authorized under the Agreement, not as a successor Trustee — and a Transfer of the Property Token during the wind-up period passes both. Fallback: if the Token is destroyed or irretrievable, the last identifiable onchain holder retains the authority
- **Pre-recording and challenge rights preserved (Section 10.5.3):** Section 10.5 does not impair the Beneficiary's or any interested party's rights to redeem the Property before recording or to challenge the validity of the Operative Instrument in court
- **Reinstatement on judicial reversal (Section 10.5.4):** If a court sets aside or vacates the recording of the Operative Instrument and record title is restored to the Trust, the Trust is reinstated as of the date of the original recording and is deemed to have continued in existence without interruption. Any Transfers of the Property Token during the void period are given full effect under Section 7, and the then-current onchain holder becomes the Beneficiary upon reinstatement. If the Property Token has been destroyed or is otherwise irretrievable at the time of reinstatement, Beneficiary identity falls back to the last identifiable onchain holder (parallel to the wind-up fallback in Section 10.5.2). The bearer-token mechanic lets a buyer of the Void Token (e.g., a speculator who pays for the residual recovery option) end up as the post-reinstatement Beneficiary if they prevail in setting aside the Operative Instrument

**Cross-reference and definition updates supporting Section 10.5:**

- **Section 1.2:** "title to the Property will remain in the Trust until such time as either the then-present Beneficiary distributes the Property out of the Trust, or record title is transferred out of the Trust by operation of law as described in Section 10.5"
- **Section 2.22 (Alternative Dissolution Event):** Definition extended to include Section 10.5 dissolutions
- **Section 2.25 (Void Token):** Refined to "A Void Token confers no beneficial ownership rights, no Owner Rights, and no interest in the Property" (dropped "or the Trust" since the Trust may survive for the limited wind-up purpose under Section 10.5.2), with explicit carve-out for the rights granted under Sections 10.5.2 and 10.5.4. Also dropped "permanently" from the opening sentence ("permanently dissociated" → "dissociated"), since dissociation under Section 10.5 is reversible if the Operative Instrument is later set aside under Section 10.5.4
- **Section 4.2:** Action-validity exception list extended to include Section 10.5
- **Section 8.2:** Trustee reliance list extended; added new clause (e) authorizing the Trustee to rely on a recorded copy of the Operative Instrument
- **Former Sections 10.5/10.6/10.7 renumbered to 10.6/10.7/10.8** to accommodate the new Section 10.5. No incoming cross-references to those sections elsewhere in the document, so the renumbering is contained
- **Section 10.6.1 (common provisions for AD Events):** Restructured into three sentences: (i) the Property Token becomes a Void Token upon recording; (ii) a Void Token does not convey beneficial ownership of the Property; (iii) in Section 10.5 cases, the Void Token additionally carries the wind-up and reinstatement-eligibility rights set out in Sections 10.5.2 and 10.5.4, each travelling with the Void Token through subsequent Transfers
- **Section 10.6 common provisions (subsections 1, 2, 4):** Updated to reference both the Deed of Distribution (for Sections 10.2–10.4) and the Operative Instrument (for Section 10.5) where the legal effect attaches

IPFS CID: `<TBD>`

#### v4.2

**Production-readiness hardening (Sections 10.2, 10.3, 11.6, 12.3–12.4):** Operational and recordation changes to support deed-out actions at scale across multiple jurisdictions:

- **Recordation hardening (Sections 2.23, 10.2):** Notice of Lost Token Control now defined as a sworn affidavit (or equivalent sworn recordable instrument), executed under oath and notarized in whatever form the situs jurisdiction requires — ensuring universal county-recorder acceptance across all 50 states. If the county recorder refuses to accept the Notice, the Beneficiary must proceed to the court-ordered path under Section 10.4. Contest mechanism broadened from "counter-notice" to any instrument permitted by applicable recording statutes (lis pendens, affidavit of adverse claim, or equivalent). If contested, process halts and routes to Section 10.4. Notice delivery expanded to include known lienholders and encumbrance holders in addition to the Property address
- **Succession evidence gating (Section 10.3.2):** Proof of legal succession must now be valid under the laws of the jurisdiction where the Property is located. If the legal successor cannot obtain sufficient proof, mandatory fallback to court-ordered dissolution under Section 10.4
- **Real-property law savings clause (Section 11.6):** Explicit statement that UCC Article 12 "control" does not displace real-property recording statutes, deed requirements, or title-vesting rules. Token control determines rights in the token as a CER, but transfer of record title requires a deed satisfying applicable real-property law
- **Situs-law and venue preservation (Sections 12.3–12.4):** California governing-law clause now expressly preserves mandatory situs-state rules for conveyancing, recording, lien priority, and probate. Venue clause preserves jurisdiction in the Property's location for quiet title, foreclosure, and similar real-property actions

IPFS CID: `bafkreihkphcet3ncjlmd7kv4wgc32ot3mnkpudavtydnwt4hdaa3q5z6mi`

#### v4.1

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
| 4.3     | `<TBD>`                                          | `<TBD>`                                                      |
| 4.2     | `bafkreihkphcet3ncjlmd7kv4wgc32ot3mnkpudavtydnwt4hdaa3q5z6mi` | https://ipfs.fabrica.land/ipfs/bafkreihkphcet3ncjlmd7kv4wgc32ot3mnkpudavtydnwt4hdaa3q5z6mi |
| 4.0     | `bafkreigc4ckzv5agna3tohs5tcqvvze6wgu7oocj5ecpqcg3gxaspyxpue` | https://ipfs.fabrica.land/ipfs/bafkreigc4ckzv5agna3tohs5tcqvvze6wgu7oocj5ecpqcg3gxaspyxpue |
| 3.7     | `bafkreielajiqjyqjwofuxaep6heoxx6ag4ifum7u6mafvkkhuif2dcqvc4` | https://ipfs.fabrica.land/ipfs/bafkreielajiqjyqjwofuxaep6heoxx6ag4ifum7u6mafvkkhuif2dcqvc4 |
| 3.6     | `bafkreifiv6x6a77v6gnjxw3tfxo5exzo736x6fvr2inx46qpn3woemgxky` | https://ipfs.fabrica.land/ipfs/bafkreifiv6x6a77v6gnjxw3tfxo5exzo736x6fvr2inx46qpn3woemgxky |
| 3.5     | `QmNxY3ooc4VXbW6ETd1wVAxvajZYWu81U95MmWJiNBQw14` | https://ipfs.fabrica.land/ipfs/QmNxY3ooc4VXbW6ETd1wVAxvajZYWu81U95MmWJiNBQw14 |
| 3.4     | `QmeRZqhU59Vpn4JQvggBVQ97uMfmS68utweUury8n5JLPR` | https://ipfs.fabrica.land/ipfs/QmeRZqhU59Vpn4JQvggBVQ97uMfmS68utweUury8n5JLPR |
| 3.3     | `Qmf6Aia6gJfRgGyGroYft3kjxsLUhJEhMYVKPKj2JwY41Z` | http://ipfs.fabrica.land/ipfs/Qmf6Aia6gJfRgGyGroYft3kjxsLUhJEhMYVKPKj2JwY41Z |
| 3.2     | `QmcgEJkgCwizvs6Tu12jCaNMGciRNtH8dLA2TRS3aYWStX` | https://ipfs.fabrica.land/ipfs/QmcgEJkgCwizvs6Tu12jCaNMGciRNtH8dLA2TRS3aYWStX |
| 3.1     | `QmXRQx7wPxSwQDVVr1pTkiwvBHBUd1SYLbLgSn1Bvirqpc` | https://ipfs.fabrica.land/ipfs/QmXRQx7wPxSwQDVVr1pTkiwvBHBUd1SYLbLgSn1Bvirqpc |
| 3.0     | `QmRH7d7TGJ3DymLSRimjnH5cNGHzYfcvUTUA1tM9gizFY8` | http://ipfs.fabrica.land/ipfs/QmRH7d7TGJ3DymLSRimjnH5cNGHzYfcvUTUA1tM9gizFY8 |

