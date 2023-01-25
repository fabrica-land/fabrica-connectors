# Fabrica Trust Agreement

This Trust Agreement (this "**Agreement**") is entered into by the Grantor through the creation of a Fabrica NFT. The identifying information of this trust (the "**Trust**") may be found in the Fabrica NFT to which this Agreement is attached.

### Recitals

- Whereas blockchain Smart Contracts provide a secure and interoperable way of representing ownership of digital assets through use of an electronic ledger to immutably track, document and verify all transactions. As a consequence, new systems and methods are emerging to store, interact with and transact on real and digital assets.
- Whereas the grantor wants to link ownership of real property to an NFT so as to benefit from digital operations and services.
- Whereas on issuance of the NFT, the grantor will attach this Agreement to the NFT, and intends for this Agreement to act as the operating agreement of the entity holding real property. For the purposes of interoperability and standardization, the grantor and any subsequent party to this agreement intend to keep all the identifying information of this Agreement stored in the NFT to which this contract has been attached. All the operations, definitions and procedures related to the NFT and the Trust will be stored in this Agreement.
- Whereas the purpose and design of this Trust allow the beneficiary to use blockchain technology to facilitate transfer and utilization of property ownership. To the extent provided in this Agreement, the trustee's power and authority to deal with the property are subject to direction by the beneficiary, who holds all economic and beneficial rights to the property. The beneficiary (who may change from time to time and is at all times defined as the party presently holding ultimate control over the NFT) is entitled to income, maintains the sole right of termination, and is treated as the owner of the property for all federal, state and local tax purposes. 
- Whereas the parties intend to treat all valid operations done via blockchain on the NFT as final, with the same force and effect of a fully executed agreement. Further, the parties intend to treat digital signatures with the same legal consequence as wet signatures.
- Now, therefore, in consideration of the agreements and obligations set forth herein and for other good and valuable consideration, the receipt and sufficiency of which are hereby acknowledged, the parties agree as follows:

### 1. Trust Purpose ###

1. The purpose of the Trust is to create a legally enforceable link such that ownership of the NFT on Ethereum determines ownership of the property, so as to allow for the time efficient, cost effective, accurate, and secure ownership, transfer, use and enjoyment of real property title in the digital environment (the "**Trust Purpose**"). 
2. On creation, the Trust will take and hold title to the Property, and ownership of the Trust will be represented by ownership of the NFT. Regardless of the sale, hypothecation, or other transfer of the NFT, title to the Property will remain in the Trust until such time as the then-present Beneficiary (or another authorized party) distributes the property out of the Trust. In order to facilitate the Trust Purpose, the Trustee and Beneficiary agree that no deed or other agreement transferring the Property out of the Trust will be valid unless the Beneficiary has first ensured that the NFT has been successfully destroyed (Burned).
3. Subject to **Section 7**, the owner(s) of the Account holding the NFT shall be the Beneficiary of the Trust, and have the right to appoint the Trustee. All rights and obligations in this agreement shall at all times be linked to the owner of the NFT, such that rightful possession of the NFT gives the holder full and total beneficial ownership.

### 2. Definitions ###

1. **Account** means an Address owned by a person and controlled through a private key.
2. **Address** means a public key address on Ethereum.
3. **Beneficiary** means the individual or entity that is in control of the most recent Account owning the NFT. In the event the NFT has not yet been minted, or has been minted but has never yet been owned by any Account, the Beneficiary shall be the original Grantor.
4. **Burn** is the result of a Confirmed Transaction of the `burn` or `burnBatch` functions on the Fabrica Smart Contract that results in the removal of the association between a Token ID and an Address, effectively locking the NFT.
5. **Confirmed Transaction** means a transaction that has been recorded on Ethereum in accordance with the Consensus Rules (as defined below) in a valid block whose hashed header is referenced by a commercially reasonable number of subsequent valid blocks on Ethereum. The initial number of such blocks shall be 12.
6. **Consensus Rules** means the rules for transaction validity, block validity and determination of the canonical blockchain that are embodied in Ethereum.
7. **Contract Account** means an Address controlled by a Smart Contract.
8. **Creation Date** means the date and time at which the Trust was created by the Grantor.
9. **Ethereum** means the Ethereum mainnet and the consensus blockchain for such mainnet (networkID:1, chainID:1) as recognized by the official Go Ethereum Client implemented at https://github.com/ethereum/go-ethereum as of the Creation Date.
10. **Fabrica Smart Contract** means the Smart Contract used to maintain records of ownership and management of the Fabrica NFT to which this Agreement is attached.
11. **Fabrica NFT** means an NFT issued using the Fabrica Smart Contract.
12. **Grantor** is the individual or entity who creates the Trust and grants the Property to the Trust.
13. **Mint** means a Confirmed Transaction `mint()` or `mintBatch()` function on the Fabrica Smart Contract that results in the association of a Token ID to an Address.
14. **Non Fungible Token (NFT)** means the digital asset stored on Ethereum with a unique identification code (Token ID) adhering to the ERC-1155 standards.
15. **NFT Metadata** means the data directly stored within the NFT as well as external data stored on IPFS and linked within the NFT itself (using the fields `definition` and `configuration`). These will always include Token ID, Trust Name (stored as `definition.holdingEntity`), and Property legal description (`definition.claim`). Other additional information may be included to simplify property identification, verify past ownership and other activities.
16. **Property** is the bundle of rights identified in the legal description stored in the NFT Metadata under the field `definition.claim`. The Property so described is the bundle of rights which is to be deeded into the Trust and held throughout the life of the Trust.
17. **Smart Contract** means the bytecode deployed on a specific Ethereum Address which acts as a program to execute and run a series of processes or interactions.
18. **Token ID** means the unique and immutable identifier determined on Trust creation and assigned to the corresponding Fabrica NFT. The Token ID is created based on the digital signature of mutiple fields combined, including this Agreement.
19. **Transfer** means any operation performed through the Smart Contract that assigns the NFT to a new non null Address.
20. **Trustee** means the individual or entity appointed by the Beneficiary as the Trustee of the Trust.
21. **Trust Name** means the name of the Trust, more particularly defined in the NFT Metadata (in `definition.holdingEntity`).


### 3. Establishing the Trust

1. The process for entering into this Agreement is as follows:
   1. The Grantor, or a third party instructed by the Grantor, creates the Trust by generating a Token ID using the function `generateId` on the Fabrica Smart Contract;
   2. the Grantor transfers the Property into the Trust by deed, or instructs a third party owner to do so, and records the deed with the relevant authority or recorder. The deed language shall specify both the Fabrica Smart Contract address and the Token ID;
   3. the Grantor Mints the Fabrica NFT through the Fabrica Smart Contract, attaching this Agreement and a copy of the conveyance deed to the NFT Metadata;
   4. Upon a Confirmed Transaction, the Beneficiary will be entitled to the Owner Rights (described below). Ownership records for the NFT will be kept by the Fabrica Smart Contract. 
2. The Trust is not intended to be, shall not be deemed to be, and shall not be treated as a general partnership, limited partnership, joint venture, corporation or joint stock company. Prior to a Transfer, the trust should for all purposes be considered revocable by the Grantor, up to and until the specification of a Beneficiary. At the point a Beneficiary is specified, the trust is no longer revocable by the Grantor, and the Beneficiary then retains the sole right to distribute the Property and dissolve the Trust.
3. In the event that the Fabrica NFT is minted by a Contract Account, then the Grantor shall be considered the Beneficiary of the Trust, unless otherwise specified.
4. In the event that the Property has been transferred into the Trust, but the Fabrica NFT has not yet been minted and no Beneficiary has been specified, the Grantor shall be considered the Beneficiary of the Trust, unless otherwise specified.

### 4. Transactions and Interactions with Fabrica Smart Contract

1. Any signature or execution made through the use of private keys on Ethereum for any matters relating to the NFT or the Trust shall be valid, sufficient and final, as if signed in writing.
1. Any action that the Beneficiary or Trustee takes with respect to the Property or the Trust shall be invalid unless first instructed through a Confirmed Transaction on interaction with the Fabrica Smart Contract and under the conditions of this Agreement.

### 5. Grantor rights and representations

1. The Grantor is responsible for funding of the Property into the Trust on creation. Following funding of the Trust, the Grantor (except in his capacity as Trustee and/or Beneficiary) will have no rights regarding the Property, the NFT, or the management of the Trust, and will not retain any voting, director appointment, consent, approval, management or revocation rights with respect to the Property or the Trust. Further, Grantor will not have any right to require the Beneficiary or Trustee to consult with Grantor with respect to the exercise of such rights and neither the Beneficiary nor the Trustee is required to consult with Grantor with respect to such rights, and the Grantor will have no right to remove or to replace the Beneficiary or Trustee. For purposes of this Agreement, the Trust is not deemed to be an affiliate of Grantor or of any of Grantor’s affiliates.
2. Immediately Prior to Grantor’s conveyance of the Property into the Trust, Grantor represents and warrants:
   1. That Grantor has the full right, power and authority to enter into and deliver this Agreement and to perform all covenants and agreements of Grantor hereunder.
   2. That to the best of Grantor’s knowledge at the time of creation of the Trust, Grantor owns fee simple record title to the Property as described in the Property legal description attached to the NFT Metadata; or, if Grantor does not own fee simple record title to the Property, then Grantor has attached to the NFT Metadata the full expression of Grantor's title interest in the Property being granted into the Trust, and a description of any other outstanding interests in the Property at the time of Trust creation.

### 6. Beneficiary Rights

1. The Beneficiary, or an authorized third party, is authorized: (1) to execute any function via the Fabrica Smart Contract regarding any decision made by the Beneficiary with respect to the NFT, the Property, and the Trust, including but not limited to transfer, lease, encumbrance, or partial or total sale of the NFT, transfer, lock or utilization of the NFT within any Contract Account, or any other legal and available activity with respect to ownership of property represented by a digital token; and, (2) to dissolve the Trust and instruct the Trustee to distribute the Property as more fully described in **Section 11**. The Beneficiary shall possess beneficial enjoyment to and from the Property, including the right of possession, right of control, right of exclusion, right of enjoyment and right of disposition, as well as the right to transfer, lend or dispose of such, and any other rights traditionally or typically associated with property ownership, subject to the provisions of the Trust. The Beneficiary shall have the right to borrow against the NFT . The Beneficiary is entitled to all net income and receipts from the Property regardless of source, and is responsible for any debts, taxes or other liabilities arising out of the Property or ownership of the NFT. All net income accrued or undistributed at the termination of any interest shall be treated as if it had accrued or been received immediately after that termination. All of the above Beneficiary rights and entitlements are referred to herein as the "**Owner Rights**."
2. The Owner Rights should be considered absolute, sole and uncontrolled, except to the extent that such Owner Rights are in conflict with the other provisions of this Agreement.

### 7. NFT Transfer

1. The Beneficiary may transfer the Owner Rights by transferring the NFT to another Account through the execution of any code or function that results in the assignment of the Token ID to a different account. On a Confirmed Transaction, the owner of that Account shall become the new beneficiary of the Trust, and will also either become the new trustee or appoint the new trustee. The Trustee shall only serve as long as the Beneficiary is the Beneficiary of the Trust, and on transfer of the NFT, the prior trustee is replaced by the transferee trustee. 
2. Transfer of the NFT shall effectuate the full assignment of all interests, rights, duties, liabilities and obligations under the Trust. Therefore, use of the terms “Trustee” and “Beneficiary” within this Agreement shall reference the present interest trustee and present interest beneficiary, as such are identified by the record of the NFT as maintained by the Fabrica Smart Contract. 
3. The Beneficiary may transfer the NFT to a Contract Account, for example for the purpose of, among other things, placing the NFT in escrow to collateralize or fractionalize the NFT. The NFT may transfer to multiple Contract Addresses, prior to being returned to the Beneficiary’s Ethereum Address or to an alternative User Address. Such transfers do not necessarily cause an assignment of the Trust. Instead, the Beneficiary and Trustee will remain in their position until such time, if ever, that ownership of the NFT transfers to an Account with a new owner, or the Beneficiary effectuates an assignment of the Owner Rights in some other fashion.
4. All identifying information about the chain of Accounts and Contract Addresses that have interacted with the NFT, as well as the present owner Account, are immutably recorded on Ethereum.

### 8. Trustee obligations, fees and indemnification

1. The Trustee shall:
   1. act as the representative of the Trust at the behest of the Beneficiary, and manage the Property of the Trust consistent with the terms of this Agreement;
   2. prepare, execute, and deliver any documents related to the continued existence of the Trust as well as in connection with any transfer of the NFT or any termination event as defined in **Section 11**;
   3. have no duty or liability to the Grantor or Beneficiary with respect to any change in value of any of the Property during the life of the Trust, nor shall the Trustee be liable to any prior or subsequent beneficiary or trustee, except to the extent such liability is created by any private agreement or by the willful actions of the Trustee; and,
   4. not be required to furnish a bond or other security in any jurisdiction for the faithful performance of its duties.


### 9. No individual ownership; Trust Proceeds

1. Title to all of the assets of the Trust shall be vested in the Trust until the Trust dissolves; provided, however, that if the applicable laws of any jurisdiction require that title to any part of the assets of the Trust be vested in a party to the Trust, then title to that part of the assets of the Trust shall be vested in the Beneficiary to the extent so required, with such vested title remaining subject, however, to the assignment and transfer provisions of **Section 7**. Ownership of the Property will remain in the Trust, despite transfer of the NFT, until such time as the Trust is dissolved.

### 10. Trust termination

1. The process for dissolving the Trust is as follows ("**Dissolution Event**"):
   1. first, the Beneficiary will instruct the Fabrica Smart Contract by calling the `burn` or `burnBatch` functions; 
   2. second, after a Confirmed Transaction, the Beneficiary will digitally sign a deed with their private key, and instruct the Trustee to sign the deed transferring the Property and any other additional remaining Property from the Trust; and, 
   3. the Trustee will transfer the property out of the Trust.
2. In the event of any disposition involving all or part of the Property, the proceeds of such distribution, whether in the form of cash, property, digital assets, or other assets or securities, will be distributed to the Beneficiary, or any other person or entity designated by the Beneficiary to receive such distribution. In the event that dividends or distributions are paid in respect of any portion of the Trust Property, all of such dividends or distributions shall be distributed to the Beneficiary as soon as practicable following receipt of any such dividends or distributions, whether in the form of cash, property or securities
3. Once the Trust has been fully established, as per the steps in **Section 3**, and throughout the life of the Trust, the Grantor holds no right of termination, nor is any termination subject to the life of Grantor or any decision or action taken by the Grantor. 

### 11. Miscellaneous

1. If any part of any provision of this Agreement or any other agreement, document or writing given pursuant to or in connection with this Agreement shall be invalid or unenforceable under applicable law, said part shall be ineffective to the extent of such invalidity only, without in any way affecting the remaining part of said provision or the remaining provisions of this Agreement.
2. The headings of the sections and subsections of this Agreement are inserted for convenience of reference only and do not form a part or affect the meaning hereof. Wherever used herein, a pronoun in any gender shall be considered as including any other gender pronoun. References to the singular include the plural, and vice versa.
3. To the extent it is not contrary to a strong public policy of the jurisdiction, if any, having a more significant relationship to this Agreement, this Agreement, the rights and obligations of the parties hereto, and any claims and disputes relating thereto, shall be governed by and construed in accordance with the laws of the State of California (not including the choice of law rules thereof).
4. The parties to this Agreement hereby consent to the non-exclusive jurisdiction of any State or Federal Court of competent jurisdiction located within the State of California, in the County of San Francisco, in connection with any actions or proceedings arising directly or indirectly from this Agreement.

