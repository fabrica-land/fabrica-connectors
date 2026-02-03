# Changelog
### Fabrica Trust

#### v4.0

- **Alternative dissolution provisions (Sections 10.2–10.5):** Added three new paths to dissolve the Trust when the Beneficiary cannot Redeem the Property Token — uncontested recovery for lost keys (Section 10.2), estate succession when the Beneficiary has died without passing on key access (Section 10.3), and court-ordered dissolution for contested or theft scenarios (Section 10.4)
- **Section 10.2 — Uncontested recovery:** Beneficiary records a Notice of Lost Token Control at the county recorder. The recording starts a 90-day Quiet Period. If no one moves the token or files a counter-claim during that period, the Beneficiary executes a Deed of Distribution. The entire process runs through public records — no intermediary, platform, or service provider is required for the legal mechanism to function
- **Section 10.2 — Eligibility gate:** Alternative dissolution under Section 10.2 is available only when the Property Token is held by an Account (EOA) or a Section 7.3(a) Contract Account (custody wallet). If the token is in a Section 7.3(b) functional contract (lending, escrow, collateral, etc.), the Beneficiary must first cause the token to be returned before initiating the process. This structurally protects lenders and other counterparties without requiring any off-chain verification
- **Section 10.3 — Estate succession:** Same process as 10.2, with the Beneficiary's legal successor (executor, administrator, or heir) stepping into the Beneficiary's position using probate documents recorded alongside the Notice. Clarifies that successors who inherit wallet access need no special process
- **Section 10.4 — Court-ordered dissolution:** Fallback for theft, disputed ownership, or any situation where Sections 10.1–10.3 cannot complete. Court order substitutes for both the burn requirement and the cryptographic signature requirement
- **Section 10.5 — General provisions for alternative dissolution:** Void Token treatment (token exists on-chain but confers no rights), UCC Article 12 interaction (control of a Void Token confers no property interest), explicit statement that off-chain record updates are administrative conveniences and do not affect legal validity
- **Section 1.2 amended:** Added carve-out so the burn-before-deed condition precedent does not apply to alternative dissolutions under Sections 10.2, 10.3, or 10.4
- **Section 7.5 — Unauthorized transfers:** Clarifies that a Transfer resulting from theft or misappropriation of private keys does not constitute a valid transfer of beneficial ownership; prior Beneficiary retains Owner Rights. States that the Beneficiary is responsible for maintaining the security of access to their Account. Preserves qualifying purchaser and protected secured party protections under Section 11.4 — conflicts between unauthorized transfer claims and Section 11.4 claims are resolved by courts
- **Section 11.4 — Protected secured party:** Extends UCC Article 12 qualifying purchaser protection to parties who obtain a security interest in the Property Token for value, in good faith, and without notice. When a stolen token is used as collateral with an innocent lender, the lender's position is protected and the prior Beneficiary's remedy is against the party who effected the unauthorized Transfer
- **New definitions (Section 2):** Alternative Dissolution Event, Notice of Lost Token Control, Quiet Period, Void Token
- **Beneficiary definition (Section 2.3) clarified:** Beneficial ownership is determined under Section 7 and may differ from the current onchain holder due to functional contract custody (7.3(b)), unauthorized transfers (7.5), or loss of token control (10.2, 10.3)
- **Section 10.2.3 — Wallet activity halt:** The Quiet Period halts on any Confirmed Transaction initiated by the Account or Contract Account holding the Property Token, not only on a Transfer of the Property Token. For Contract Accounts, a transaction "originating from" the Contract Account includes any transaction executed by its code, regardless of which external party submitted the triggering transaction. If the wallet signs any transaction during the 90 days, it disproves the premise that access to the Account has been lost
- **Section 1.3 clarified:** Ownership may be established through a valid Account (EOA) or a Section 7.3(a) Contract Account, not merely through temporary custody by a Section 7.3(b) functional contract. Aligns Section 1.3 with the ownership model in Section 7.3
- **Section 10.3.3 aligned with Section 10.2:** Estate succession halt and contest conditions now mirror Section 10.2's updated language (Confirmed Transaction from the holding Account or Contract Account, counter-notice or lis pendens in county records)
- **Section 10.2.4 — Sworn certificate:** After the Quiet Period expires, the Beneficiary delivers a sworn certificate to the Trustee confirming no Confirmed Transaction was initiated by the Account and no counter-claim was filed. The Deed of Distribution recites the certificate rather than asserting these facts independently, maintaining consistency with the Trustee reliance safe harbor in Section 8.2
- **Section 10.2.1 — Physical notice delivery:** Within ten days of recording, the claimant must also deliver a copy of the recorded Notice by certified mail to the Property address as shown in county assessor or tax collector records. This provides actual notice to any occupant or passive owner who may not monitor county recordings, and is attested in the sworn certificate under Section 10.2.4
- **Section 10.2.2 — Contest requirements:** Contest during the Quiet Period must appear in county records (counter-notice, lis pendens, or a competing Notice of Lost Token Control filed by a different claimant). Filing a lawsuit alone, without a corresponding recorded instrument, does not constitute a contest. This keeps the entire process verifiable through a single public record source
- **Section 8 header corrected:** Renamed from "Trustee obligations, fees, and indemnification" to "Trustee Obligations and Safe Harbor" to accurately reflect the section's content
- **Independence by design:** The alternative dissolution mechanism operates entirely through county recordings, the passage of time, and (for contested cases) courts. No validator, platform, or service provider is a required participant in the legal process. This preserves the trust's core design principle: the system works even if the platform that created it ceases to exist

IPFS CID: *(to be added upon finalization)*

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
| 4.0     | *(to be added upon finalization)*                | |
| 3.7     | `bafkreielajiqjyqjwofuxaep6heoxx6ag4ifum7u6mafvkkhuif2dcqvc4` | https://ipfs.fabrica.land/ipfs/bafkreielajiqjyqjwofuxaep6heoxx6ag4ifum7u6mafvkkhuif2dcqvc4 |
| 3.6     | `bafkreifiv6x6a77v6gnjxw3tfxo5exzo736x6fvr2inx46qpn3woemgxky` | https://ipfs.fabrica.land/ipfs/bafkreifiv6x6a77v6gnjxw3tfxo5exzo736x6fvr2inx46qpn3woemgxky |
| 3.5     | `QmNxY3ooc4VXbW6ETd1wVAxvajZYWu81U95MmWJiNBQw14` | https://ipfs.fabrica.land/ipfs/QmNxY3ooc4VXbW6ETd1wVAxvajZYWu81U95MmWJiNBQw14 |
| 3.4     | `QmeRZqhU59Vpn4JQvggBVQ97uMfmS68utweUury8n5JLPR` | https://ipfs.fabrica.land/ipfs/QmeRZqhU59Vpn4JQvggBVQ97uMfmS68utweUury8n5JLPR |
| 3.3     | `Qmf6Aia6gJfRgGyGroYft3kjxsLUhJEhMYVKPKj2JwY41Z` | http://ipfs.fabrica.land/ipfs/Qmf6Aia6gJfRgGyGroYft3kjxsLUhJEhMYVKPKj2JwY41Z |
| 3.2     | `QmcgEJkgCwizvs6Tu12jCaNMGciRNtH8dLA2TRS3aYWStX` | https://ipfs.fabrica.land/ipfs/QmcgEJkgCwizvs6Tu12jCaNMGciRNtH8dLA2TRS3aYWStX |
| 3.1     | `QmXRQx7wPxSwQDVVr1pTkiwvBHBUd1SYLbLgSn1Bvirqpc` | https://ipfs.fabrica.land/ipfs/QmXRQx7wPxSwQDVVr1pTkiwvBHBUd1SYLbLgSn1Bvirqpc |
| 3.0     | `QmRH7d7TGJ3DymLSRimjnH5cNGHzYfcvUTUA1tM9gizFY8` | http://ipfs.fabrica.land/ipfs/QmRH7d7TGJ3DymLSRimjnH5cNGHzYfcvUTUA1tM9gizFY8 |

