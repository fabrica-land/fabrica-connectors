# Changelog
### Fabrica Trust

#### v4.4 (proposed — open for comment)

**Beneficial-interest characterization, financed-purchase and succession mechanics, unsolicited-transfer doctrine, and a full UCC Article 9/12 build-out.** v4.4 states, for the first time in the instrument, what the token holder's interest *is* as a matter of property law (personal property, in the American land-trust tradition), and builds the transfer, lending, succession, and disclaimer rules on top of that foundation. It hardens the trust against state-law validity attacks (Texas passive-trust and merger doctrines), closes the financed-purchase ownership gap, gives holders a self-help disclaimer against hostile transfers, and adds a non-operative plain-language summary. The instrument roughly triples in length; no load-bearing v4.3 provision is weakened.

**Ownership & Transfers:**

- **Beneficial interest declared personal property (new Section 1.4, new definitions 2.27–2.28, recital):** The entire beneficial interest in the Trust is personal property in the land-trust tradition, not an estate in land. It passes by assignment under Section 7 without a deed; the token is its authoritative record and instrument of transfer. The Property itself remains real property governed only by real-property law (Section 11.6, unchanged)
- **Trust corpus sealed at creation (new Section 1.5):** What the trust holds is fixed at the Trust's creation — the described Property together with its legal appurtenances, accessions, and proceeds, and nothing else. While the property is operated through the token, no beneficiary direction, trustee act, or third-party instrument may substitute, augment, or partially convey the corpus, and the Trustee must refuse any standalone addition, so a stranger cannot deed an unwanted, liability-laden asset into the trust. The only exceptions are mandatory law and the recorded events of Section 10; the seal releases entirely at dissolution, leaving the former holder free to direct the distribution deed, including dividing rights among multiple grantees
- **Free alienability (Section 6.2):** The beneficial interest is freely alienable, not subject to any spendthrift restraint, and reachable by the Beneficiary's creditors as applicable law provides
- **Occupancy right (new Section 6.4):** The Beneficiary has the right, but never the obligation, to occupy the Property as a principal residence rent-free; the right travels with the beneficial interest and vests in no named person
- **Unauthorized transfers broadened (Section 7.5.1):** A transfer is unauthorized, and moves no beneficial ownership, whenever it is not made or authorized by the present Beneficiary, expressly including misuse of a previously granted operator approval or delegation, not only key theft
- **Persons dealing with the Trustee (new Section 8.3):** A good-faith purchaser or lender taking under a facially compliant deed from the apparent Trustee need not inquire into chain state, token provenance, or Trustee authority; the deed is valid and the remedy for any defect runs against the wrongdoer and the proceeds
- **Active-trust duties enumerated (Section 8.1, retitled Trustee Duties):** The Trustee's affirmative powers and duties are stated expressly (hold, preserve, and defend title; execute and record instruments; verify conditions precedent; convey only on direction), making the trust demonstrably active

**Lending & Designations:**

- **Financed-purchase designation rule (new Section 7.3(c)):** Beneficial ownership can change hands while the token remains in a lending pool, escrow, or other smart-contract facility, but only through a "Qualified Designation" supported by the designated owner's assent. A bare naming of a borrower-of-record, by anyone, transfers nothing and imposes no tax, debt, or liability on the person named
- **Tiered assent safe harbor (Section 7.3(c)(2)):** Any signed record manifesting assent qualifies; a record carrying four stated content elements is conclusively sufficient; a record anchored by a cryptographic commitment in the originating operation is presumed authentic. Assent may be captured on-chain or off-chain (for example, a checkout confirmation), and no platform is required to keep or produce records
- **Collateral is the token, never the land (Section 11.2):** The collateral in any token financing is the Property Token and, where expressly granted, the beneficial interest; no mortgage or lien on the Property itself is created. A Confirmed Transaction and its signed records may form an authenticated security agreement under UCC Section 9-203; the debtor's redemption right under Section 9-623 is preserved and enforcement follows Sections 9-610 through 9-624

**Succession & Death:**

- **Succession follows lawful control (new Section 7.6):** On a Beneficiary's death the beneficial interest passes as personal property under the law governing the estate, and the person who lawfully succeeds to control of the wallet (the "Key Successor") may keep operating immediately, without a court order as a condition of continuity. A person who obtains access by theft is not a Key Successor
- **No ancillary situs probate (Section 7.6.2):** Because the beneficial interest is intangible personal property, its succession follows the holder's domicile law; the recording of probate proof remains only an evidentiary condition of deeding the Property out of the Trust, not an administration of the interest. The instrument makes no claim of automatic probate avoidance
- **Lost-keys fallback narrowed (Sections 10.3, 10.4):** The recorded-probate dissolution path now applies solely where no Key Successor has lawful key access; competing-successor claims are resolved by a court

**Unsolicited Transfers & Disclaimer:**

- **Presumptive vesting with a right to disclaim (new Section 7.7):** A token sent to a wallet without the recipient's agreement vests beneficial ownership presumptively and immediately, so every ownership right is usable at once, but the vesting is defeasible. The recipient bears the incidents of ownership (including tax) only until they refuse
- **On-chain disclaimer (Section 7.7.2):** A recipient may refuse the entire interest by sending the token back (the ordinary disclaimer) or by burning it, with a recorded-refusal fallback where neither is possible. A valid disclaimer relates back to the moment of receipt, to the maximum extent applicable law permits
- **Acceptance is conclusive (Section 7.7.4):** Any voluntary exercise of ownership, or express acceptance, is acceptance, confirmed retroactively to receipt. A listing that is cancelled or expires without a sale is not acceptance. A transfer the recipient solicited or agreed to is accepted on receipt, with no disclaimer right
- **Recovery after a disclaimer burn (new Section 10.2.7):** Where a recipient burns an unwanted token, the original holder can restore control of the Property through the recorded, contestable Notice procedure, with additional sworn attestations and notice to the burner

**UCC Articles 9/12:**

- **Controllable-electronic-record status (Section 11.1):** The Property Token is a controllable electronic record for so long as it is capable of being subjected to control under UCC Article 12 (as it is intended and expected to be at all times, save the fractionalized configuration Section 6.3 describes); the classification is statutory, and no custody, holding, or other arrangement varies it. The prior rule that suspended that status inside an intermediated securities-account arrangement is removed. California is expressly designated as the token's jurisdiction under UCC Section 12-107(c)(1)
- **Custodial holding (Section 11.3):** Notwithstanding the default vesting rules (Sections 1.3, 2.3, 7.1, 7.3(a)), a person who holds the token as custodian for another — directly or through tiers of sub-custodians — acquires no beneficial interest by reason of that holding; the beneficial interest vests in the person for whom the token is ultimately held, as the custody arrangement and the custodian's records identify that person. A transfer of that person's rights against the custodian transfers the beneficial interest on the same terms as a token transfer, the custody agreement plus the transfer record serving as the Section 7.3(b)(ii) assignment instrument. Where the token is held for more than one person, their proportions and internal governance are those the custody arrangement and the custodian's records provide. The custodian-customer relationship, and whether any person has control of the token, are left to the custody arrangement and to law other than the Agreement
- **Take-free mechanism made explicit (Section 11.4):** The qualifying-purchaser and protected-secured-party protections are set out in layers, declaring a trust-created power to transfer the beneficial interest — given effect as law other than Article 12 under Section 12-104(f), keyed to the Section 12-104(d) power-to-transfer concept and operating alongside the purchaser's Section 12-104(d)–(e) rights in the token itself — an independent born-defeasance of prior claims, a control predicate for secured parties, and a single "Adverse Claim" notice standard (Section 12-102(a)(2))
- **Beneficial interest classified (new Section 11.7):** The beneficial interest is a "general intangible" under UCC Section 9-102(a)(42), of which the token is the authoritative record; a security interest in it is governed by Article 9
- **Two-lane priority framework (new Section 11.8):** Interests in the Property (the land lane) are governed always by real-property law; interests in the token and beneficial interest (the token lane) by this Agreement, trust law, and UCC Articles 9 and 12; a recorded instrument is the crossing gate between them
- **Fallback without Article 12 (new Section 11.9):** Where no Article 12 enactment applies, the token stays fully operative on the trust-law assignment floor; only the third-party take-free layer varies

**Texas & State Doctrine:**

- **Passive/dry-trust defense (Section 8.1 closing paragraph):** The instrument states that the Trust is an active trust under Texas Property Code Section 112.032(b) and similar statutes, resting on the Trustee's enumerated duties in relation to the Property
- **Merger and perpetuities (Sections 12.5, 12.6):** A formation-instant recital confirms that legal and equitable interests are never united in one person (Texas Property Code Section 112.034(a) and (b)); construction, reformation, and any Trustee suspension take effect immediately before any merger event; a perpetuities savings clause with a defined termination date is added
- **Homestead and spousal joinder (new Section 5.2.3):** The Grantor represents that the Property is not homestead, or that every required spousal joinder (including under Texas Family Code Section 5.001 and Texas Property Code Section 41.0021(c)) appears on the recorded deed
- **Occupancy for homestead and Garn-St Germain (Section 6.4):** The occupancy right is drafted to support Texas Property Code Section 41.0021 homestead-through-trust treatment and the Garn-St Germain inter vivos trust transfer protection, without asserting that any exemption applies to a given property

**Recordable Instruments:**

- **Failed conveyance into the Trust (Section 10.5):** A final order or instrument establishing that the deed into the Trust was void, avoided, or failed to vest title (for example, for a missing spousal joinder) is an Operative Instrument that dissolves the Trust; a corrective instrument that confirms title remains in the Trust is not
- **Notice of Lost Token Control content (Section 2.23) and delivery (Section 10.2.1):** The Notice now carries the full legal description and parcel number, the Trust Name as vested, the deed-in reference, and indexing instructions; delivery adds the assessee mailing address and a no-situs-address alternative, notice to secured parties of record, an on-chain notice leg, and a certified-mail deposit-is-delivery rule
- **Contest channels (Section 10.2.2):** A contest is effective not only when recorded but also when a recorder refuses a tendered instrument or when noticed litigation is delivered to the Trustee and claimant
- **Deed recitals (Sections 3.1.2, 10.1.2):** The conveyance deed names the grantee using the Trust Name verbatim; the distribution deed shall (not should) carry the cryptographic-signature statement or its stated substitute and name the grantee

**Tax:**

- **Grantor-trust hooks (Section 12.7):** The Beneficiary is treated as the owner of the Property to the maximum extent applicable tax law permits, with the intended Code hooks stated (Section 678(a)(1) power to redeem and take, and purchaser-as-grantor treatment under Treasury Regulation Section 1.671-2(e)(3))
- **Honesty on limits (Section 12.7):** The attribution does not displace mandatory assessment, collection, or lien rules; a foreign holder may make the Trust a separate taxpayer (Section 672(f)); ownership changes without a recorded deed may be reportable and are not excused
- **Disclaimer-window attribution (Section 12.7):** During the disclaimable period the presumptive transferee is the tax owner; a valid disclaimer relates the attribution back to the transferor to the maximum extent tax law permits

**Drafting & Clarity:**

- **Plain-language summary (new "How This Trust Works"):** A non-operative summary box precedes the recitals; it creates no rights and yields to the operative text on any conflict
- **Onchain determinability principle (new Section 4.3):** Beneficial ownership and the validity of token operations are determinable from the blockchain record read with this Agreement, subject to mandatory law, recorded instruments, and the specific records the Agreement itself makes relevant; operations valid on the record are conclusive in favor of good-faith reliant parties
- **Digital execution and electronic records (Sections 4.1, 12.8):** A general digital-execution-and-acceptance rule confirms that parties become bound through the objective mechanics of the Agreement with no paper counterpart; electronic records and signatures satisfy applicable writing requirements under E-SIGN and UETA
- **Revocability simplified (Section 3.2):** The Trust is revocable by the Grantor until the token is minted and irrevocable afterward, a single objective event replacing the prior beneficiary-specification test
- **Record-title construction (Section 9, retitled):** A construction rule reads title held "in the Trust" as title held by the Trustee in a fiduciary capacity where local law treats a trust as a relationship, without altering any recorded vesting

IPFS CID: (pending publication)

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

IPFS CID: `bafkreihepeqissghiwo5zplcywrjlr6bfkgag5jm3jt5szxnsm6kptcpue`

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
| 4.3     | `bafkreihepeqissghiwo5zplcywrjlr6bfkgag5jm3jt5szxnsm6kptcpue` | https://ipfs.fabrica.land/ipfs/bafkreihepeqissghiwo5zplcywrjlr6bfkgag5jm3jt5szxnsm6kptcpue |
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

