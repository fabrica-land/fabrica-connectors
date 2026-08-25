# Style Guide

## Terminology

- **onchain** — one word, no hyphen. Not "on-chain."
- **offchain** — one word, no hyphen. Not "off-chain."

## Trust Agreement: Key Design Concepts

The Fabrica trust agreement (currently v4.4, adopted 2026-08-24; IPFS CID `bafkreih72odii5wcwluejt67is5q4zgdqiwqabzkg4pr5vys6o77pgujw4`) is the legal instrument that governs the relationship between a real property and its token. Versions are prospective: each trust is governed by the agreement version referenced by its Property Token at mint, so earlier-version trusts coexist with v4.4 trusts. Key design principles:

### The Keystone: Beneficial Interest as Personal Property (Section 1.4)

The entire beneficial interest in the trust is declared **personal property** in the American land-trust tradition — an interest in the trust, not an estate in land. It passes by assignment under Section 7 upon each token transfer, without a deed and free of real-property conveyancing formalities; the token is its authoritative record and instrument of transfer. The Property itself remains real property governed only by real-property law (Section 11.6). This characterization underpins the transfer, lending, succession, and disclaimer rules.

- **Corpus sealed at creation (Section 1.5):** the trust holds the described Property plus its appurtenances, accessions, and proceeds, and nothing else. The Trustee must refuse any standalone addition, so a stranger cannot deed an unwanted, liability-laden asset into the trust.

### Transfers, Custody, and Financed Purchases (Section 7)

- **7.3(a) Smart Wallet:** multi-sig, account-abstraction, or other custody solution directly controlled by specific persons — transfer to it transfers beneficial ownership to its controllers.
- **7.3(b) Functional Contract:** escrow, bridge, lending protocol, collateral, fractionalization — custody does not confer beneficial ownership; the depositor stays Beneficiary.
- **7.3(c) Qualified Designation:** beneficial ownership can change hands *while the token sits inside a Functional Contract*, so a financed purchase vests the buyer at settlement, not at loan payoff. Requires a designation of the buyer as owner of record plus "Qualifying Assent Evidence" (initiation, a signed record — with a four-element conclusive safe harbor and a cryptographic-anchoring presumption — or acceptance by conduct). A bare naming of someone without assent is legally inert: it transfers nothing and imposes no tax, debt, or liability.
- **7.5 Unauthorized transfers:** a transfer not made or authorized by the Beneficiary — key theft, and also misuse of a previously granted operator approval or delegation (7.5.1) — moves no beneficial ownership. Cut off only by the Section 11.4 protections.
- **7.6 Succession follows lawful control:** on a Beneficiary's death the interest passes as intangible personal property under the law of the holder's estate, and the **Key Successor** (Section 2.28 — whoever lawfully succeeds to wallet control) operates immediately, no court order required as a condition of continuity. No ancillary situs probate (7.6.2); the agreement does not claim automatic probate avoidance.
- **7.7 Unsolicited transfers:** an unsolicited token vests beneficial ownership presumptively and immediately (every right usable at once) but defeasibly. The recipient can refuse by **Onchain Disclaimer** — return, an irrevocable Disclaimer Burn, or (fallback) recorded onchain refusal — which relates back to receipt. Any voluntary exercise of Owner Rights is conclusive acceptance, retroactive to receipt (a cancelled or expired listing is not acceptance). The disclaimer right has no time bar under the agreement, though mandatory law (e.g., Cal. Prob. Code § 279 timing, tax law) can limit its external effect. Solicited acquisitions carry no disclaimer right at all.

### Recovery Mechanism (Sections 10.2–10.4)

Two-tier recovery for lost token control (lost keys, stuck contracts, death without key access):

- **Tier 1 (Uncontested, 10.2):** record a Notice of Lost Token Control at the county, deliver copies (property address, recorded lienholders, UCC secured parties) plus an onchain notice leg, wait out the 90-day Quiet Period, deliver a sworn certificate, Trustee executes a Deed of Distribution. Self-service, no gatekeeper.
- **Tier 2 (Contested, 10.4):** court order. For theft, disputes, competing claims, or when the token moves during the Quiet Period.
- **Eligibility gate:** Tier 1 requires the token in an Account (EOA) or Smart Wallet, not a Functional Contract — a borrower must clear the lending contract first. 10.2.7 extends Tier 1 to recovery after a Disclaimer Burn (the transferor of the disclaimed token is the claimant).
- **Estate path (10.3):** now a fallback that applies only when **no Key Successor has lawful key access** (or one exists but refuses to act) — otherwise Section 7.6 handles death without any dissolution. Legal successor records proof of succession with the Notice (10.3.2) and steps into the Beneficiary's position for the Deed of Distribution (10.3.3). Heirs who inherit key access simply exercise Owner Rights directly (10.3.4).

### Involuntary Loss of Title (Section 10.5)

Covers record title leaving the Trust by external operation of law — tax sale, judicial or nonjudicial foreclosure, eminent domain, escheat, court-confirmed adverse possession, or a recorded determination that the conveyance into the trust was void.

- **Trigger:** automatic dissolution upon recording of the Operative Instrument. No Trustee action required.
- **Effect:** the Property Token becomes a Void Token; the Trust survives only for wind-up (collecting tax-sale surplus, condemnation awards, refunds, insurance recoveries).
- **Wind-up (10.5.2):** bearer-token mechanic — whoever holds the Property Token from time to time has wind-up authority and proceeds entitlement (as representative, not successor Trustee); transfer of the token passes both. Pre-dissolution security interests continue in the proceeds.
- **Reinstatement (10.5.4):** if a court sets aside the Operative Instrument and title is restored, the Trust is reinstated as of the original recording date; transfers during the void period get full effect and the then-current onchain holder becomes Beneficiary (last identifiable holder if the token was destroyed).
- **Partial transfers (10.5.1):** an Operative Instrument affecting less than the entire Property does not dissolve the Trust.

### UCC Layer (Section 11)

- **11.1:** the Property Token is a controllable electronic record (CER) under UCC Article 12; the agreement expressly designates **California** as the token's Article 12 jurisdiction via § 12-107(c)(1).
- **11.2:** token lending is Article 9 personal-property secured lending — the collateral is the token and, where expressly granted, the Beneficial Interest, **never the land**; § 9-623 redemption preserved, no mortgage created.
- **11.3:** custodial holding — a custodian acquires no beneficial interest; it vests in the person ultimately held for. Technology-agnostic (no Article 8 machinery).
- **11.4:** qualifying-purchaser take-free stack — a good-faith purchaser for value who obtains control without notice of an Adverse Claim takes free via three cumulative layers: § 12-104(e) as to the token itself, a trust-term power to transfer the Beneficial Interest ("law other than this article" under § 12-104(f)), and born-defeasible prior interests. Loss falls on the key-compromised holder, whose remedy is against the wrongdoer.
- **11.6:** real-property law preservation — token control never transfers or encumbers record title; land moves only by deed.
- **11.7:** the Beneficial Interest is a § 9-102(a)(42) **general intangible**, not itself a CER; Article 12 protects the token, the agreement's own assignment mechanics move the interest.
- **11.8:** **two-lane priority framework** — the land lane (situs real-property law: recording acts, liens, tax sales) always governs the Property; the token lane (this agreement, trust law, Articles 9/12) governs the token and Beneficial Interest. "The token lane controls everything the Trust has; the land lane determines what the Trust has." A recorded instrument is the crossing gate (via 10.5).
- **11.9:** fallback where Article 12 is not enacted — assignment mechanics work as trust law and contract; only the third-party negotiability layer varies.

### Validity Hardening (Sections 8.1, 12.5–12.6)

- **8.1 Trustee Duties:** enumerated affirmative duties (hold/preserve/defend title, execute and record, verify conditions precedent, convey only on direction) make the trust demonstrably **active** — a defense against passive-trust execution statutes like Tex. Prop. Code § 112.032(b).
- **8.3:** persons dealing with the Trustee — a good-faith purchaser or lender under a facially compliant Trustee deed need not inquire into chain state or token provenance; remedies for defects run against the wrongdoer and proceeds.
- **12.5 anti-merger + perpetuities savings:** the contingent interests of the Beneficial Interest Holders class (Section 2.26) arise at formation, so legal and equitable title never merge even when the sole Beneficiary is also Trustee; includes a relation-back reformation rule and a perpetuities savings clause with its own termination-and-deed mechanism.
- **12.6 Continuity Trustee:** if a court nonetheless finds merger, the Beneficiary-Trustee is suspended (ministerial preservation only) and a temporary Continuity Trustee preserves the res. No standing professional trustee, no fees, no platform approval rights.

### Key Sections to Know

| Section | What it covers |
|---|---|
| 1.4 | Keystone: Beneficial Interest declared personal property; passes by assignment under §7 without a deed |
| 1.5 | Trust corpus fixed at creation; Trustee must refuse standalone additions |
| 2.3 | Beneficiary definition — determined under §7 (may differ from the onchain holder due to Functional Contract custody, Qualified Designation, custodial holding, succession, disclaimer, or unauthorized transfer) |
| 2.25 | Void Token definition |
| 2.26 | Beneficial Interest Holders — the contingent-interest class underpinning the anti-merger design |
| 2.28 | Key Successor definition (lawful successor to wallet control; thieves excluded) |
| 4.1 | Digital execution — electronic signatures and records valid under E-SIGN/UETA |
| 4.3 | Onchain determinability principle + good-faith reliance protection (4.3.2) |
| 6.2 | Owner Rights absolute; Beneficial Interest freely alienable, no spendthrift restraint |
| 6.4 | Occupancy right (homestead-through-trust, Garn-St Germain) — permissive, travels with the interest |
| 7.3(a) | Smart Wallets (multi-sig, account abstraction — control confers beneficial ownership) |
| 7.3(b) | Functional Contracts (lending, escrow, bridges — custody does not confer ownership) |
| 7.3(c) | Qualified Designation — financed-purchase ownership transfer during Functional Contract custody |
| 7.5.1 | Unauthorized transfers (key theft and operator-approval misuse) move no beneficial ownership |
| 7.6 | Succession on death — Key Successor operates immediately; interest passes as personalty under domicile law |
| 7.7 | Unsolicited transfers — presumptive defeasible vesting, Onchain Disclaimer (return/burn/recorded refusal), acceptance conclusive and retroactive |
| 8.1 | Trustee Duties (enumerated; active-trust defense) |
| 8.2 | Trustee reliance safe harbor (recorded documents, death certificate + Key Successor evidence; no blockchain investigation) |
| 8.3 | Protection of persons dealing with the Trustee |
| 9 | Record-title construction ("in the Trust" = Trustee in fiduciary capacity where local law requires) |
| 10.1 | Standard dissolution (burn token, get deed) |
| 10.2 | Alternative dissolution (recovery). Eligibility gate: token in EOA or 7.3(a) Smart Wallet, not 7.3(b) |
| 10.2.3 | Token movement during Quiet Period halts the process |
| 10.2.4 | Sworn certificate delivered to Trustee after Quiet Period |
| 10.2.7 | Recovery after a Disclaimer Burn (transferor is claimant) |
| 10.3 | Estate fallback — only where no Key Successor has lawful key access |
| 10.3.2 | Legal successor records proof of succession with the Notice |
| 10.3.3 | Legal successor steps into Beneficiary position for the Deed of Distribution |
| 10.3.4 | Heirs who inherit key access exercise Owner Rights directly |
| 10.4 | Court-ordered dissolution (residual path for contested cases) |
| 10.5 | Involuntary loss of Property title — automatic dissolution on recording of an Operative Instrument |
| 10.5.1 | Partial transfers do not dissolve the Trust |
| 10.5.2 | Bearer-token wind-up authority and proceeds entitlement |
| 10.5.4 | Reinstatement if the Operative Instrument is set aside; current onchain holder becomes Beneficiary |
| 10.6 | Common provisions for all Alternative Dissolution Events (Void Token consequences, offchain-records authorization, UCC Article 12 treatment) |
| 10.6.2 | Offchain records (confidence scores) are administrative convenience, not legally required |
| 11.1 | CER status; California designated as the token's Article 12 jurisdiction |
| 11.2 | Collateral is the token/Beneficial Interest, never the land; § 9-623 redemption preserved |
| 11.3 | Custodial holding (technology-agnostic; custodian acquires no beneficial interest) |
| 11.4 | Qualifying purchaser / protected secured party take-free stack |
| 11.6 | Real-property law preservation |
| 11.7 | Beneficial Interest = general intangible; token is its authoritative record |
| 11.8 | Two-lane priority framework (land lane vs token lane; recorded instrument as crossing gate) |
| 11.9 | Fallback where UCC Article 12 is not enacted |
| 12.5 | No merger of interests + perpetuities savings |
| 12.6 | Springing Continuity Trustee |
| 12.7 | Tax: Beneficiary treated as owner (IRC § 678(a)(1), Treas. Reg. § 1.671-2(e)(3)), with stated limits |
| 12.8 | Digital execution and acceptance (binding without paper counterpart) |

### Design Principles

- **Walk-away independence:** Everything must work if Fabrica disappears. No gatekeeper, no admin key, no trust protector, no platform approval rights, no record-keeping duty on any platform.
- **Personal property is the keystone:** The token moves a trust interest (personalty), never land. That is why transfers need no deed, lending is Article 9 not mortgage law, succession follows domicile law, and no marital-joinder rule attaches to token transfers.
- **Separation of concerns:** The trust agreement governs the property-token relationship. Wallet security is a wallet-layer concern. Lending-protocol risk management is a protocol-layer concern. The trust agreement is the wrong layer for any of these.
- **Eligibility gate protects lenders structurally:** A token in a 7.3(b) lending contract cannot enter Tier 1 recovery. The borrower must pay off the loan first. Works with any lending protocol because it is based on onchain token location.
- **Functional, not vendor-specific:** 7.3(c) and 11.3 are defined by function — any contract or record satisfying their terms qualifies, under any technical standard, without amendment. No provision names or depends on a particular platform, protocol, or vendor.
- **Onchain determinability (4.3):** Beneficial ownership is determinable from the blockchain record read with the agreement, subject to mandatory law, recorded instruments, and the specific records the agreement itself makes relevant; operations valid on the record are conclusive in favor of good-faith reliant parties.
- **Void token = confidence score at 1:** Onchain, a token is just a token. "Void" is a legal concept communicated via the confidence score. Validators see the recorded Deed of Distribution (or, under Section 10.5, the Operative Instrument) and set the recovery digit accordingly. In Sections 10.2–10.4 cases the Void status is permanent. Under Section 10.5, the Void Token additionally carries the wind-up authority and reinstatement eligibility of 10.5.2 and 10.5.4 — these travel with the token through subsequent transfers.
- **Confidence score is a risk signal, not a legal determination:** Computed by independent validators, exposed offchain (APIs) and sometimes onchain (oracles). The trust agreement does not depend on any specific validator.

### Writing About the Trust Agreement

- Reference specific section numbers when discussing provisions.
- The token is not the land and not the deed — never write "the token is the property." The holder owns the beneficial interest (personal property) in a trust that owns the land.
- The Beneficiary is determined under Section 7, not by wallet address alone: Functional Contract custody, Qualified Designations, custodial holding, succession, disclaimers, and unauthorized transfers can all make the Beneficiary differ from the current onchain holder.
- Use "Smart Wallet" (7.3(a)) and "Functional Contract" (7.3(b)) — these are the defined terms; do not write "custody contract account."
- "Notice of Lost Token Control" is the formal name for the Tier 1 filing: a sworn affidavit recorded at the county. The 90-day Quiet Period starts from recording, not from filing.
- Disclaimers: "Onchain Disclaimer" and "Disclaimer Burn" are defined terms (7.7.2). A disclaimer is a refusal, not a transfer — the disclaimant cannot direct its destination.
- The agreement uses "Property Token," "Beneficiary," "Beneficial Interest," "Beneficial Interest Holders," "Key Successor," "Trustee," "Account," "Contract Account," "Smart Wallet," "Functional Contract," "Qualified Designation," "Owner Rights" as defined terms. Use them consistently.
- Describe expert input as "pressure-tested" or "challenged," never "reviewed" or "endorsed," unless the person has explicitly endorsed.
