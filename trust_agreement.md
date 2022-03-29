# Fabrica Trust Agreement

This Trust Agreement (*“Agreement”*) is entered into via issuing a Digital Asset (*"NFT"*) through the `mint()` function on the Fabrica Smart Contract (*"Smart Contract"*) by the Grantor using their private key on the Ethereum Blockchain. The Trust Name, Agreement and other identifiers are available in the metadata linked to the NFT that can be retrieved by calling the function `tokenURI()` of the Smart Contract. The Trust is entered into at the time the mint transaction has been confirmed on the Ethereum Blockchain.

## Recitals

- Whereas blockchain smart contracts allow for a secure and interoperable way of tracking ownership of digital assets through use of an electronic legdger to immutably track, document and verify all transactions. As a consequence, new platforms and methods are being developed to store and transact on real assets.
- Whereas the grantor wants to connect/tie ownership of the real property to the NFT so as to benefit from fully digital operations.
- Whereas on issuance of the NFT, the grantor has attached this Agreement to act as the operating agreement of the entity holding the real property. For the purpose of standardization, the grantor and any subsequent party to this agreement intend to keep all the identifing information of this Agreement stored in the NFT to which this contract has been attached. All the operations, definitions and procedures related to the NFT and this Agreement will be stored in this Agreement.
- Whereas the nature of this Trust is to allow the Beneficial Owner to utilize blockchain technology to manage their ownership of the subject property and facilitate any future transfer of beneficial ownership. The Trustee has the power and authority to deal with the subject property only to the extent directed by the Beneficial Owner, who otherwise holds all economic and beneficial rights to the subject property. The Beneficial Owner (who may change from time to time and is at all times defined as the person/entity presently in possession of the NFT) is entitled to income, maintains the sole right of termination, and is treated as the owner of the subject property for all federal, state and local tax purposes. 
- Whereas the parties intend to treat all operations done via blockchain as final, similarly to those performed in traditional real estate transactions. Further, the parties intend and agree to treat digital signatures with the same legal consequence of wet signatures.
- Now, therefore, in consideration of the agreements and obligations set forth herein and for other good and valuable consideration, the receipt and sufficiency of which are hereby acknowledged, the parties agree as follows:

## 1. Trust Purpose ##

1. The purpose of the trust is to create and maintain a link between ownership of the Property and the NFT on the Ethereum Blockchain, so as to allow for the time efficient, cost effective, accurate, and secure ownership, transfer, use and enjoyment of real property title in the digital environment. On creation, the Trust will take and hold title to the Property, and ownership of the Trust will be represented by ownership of the NFT. Regardless of the sale, hypothecation, or other transfer of the NFT, title to the Property will remain in the Trust until such time as the then-present Beneficiary (or another authorized third party) executes the `burn` function and, by doing so, removes the property from the Trust.
2. The owner(s) of the Account holding the NFT shall be the Beneficiary of the Trust, and have the right to appoint the Trustee. All rights and obligations in this agreement shall at all times be linked to the holder of the NFT, such that rightful possession of the NFT gives the holder full and total beneficial ownership.

## 2. Definitions ##

1. **Blockchain / Ethereum** means the Ethereum mainnet and the consensus blockchain for such mainnet (networkID:1, chainID:1) as recognized by the official Go Ethereum Client implemented at https://github.com/ethereum/go-ethereum as of the Creation Date.
2. **Address** means a public key address on Ethereum.
3. **Account** means an Address owned by a person and controlled through a private keys
4. **Smart Contract** means [_______]
5. **Fabrica Smart Contract** means the bytecode deployed on Ethereum used to maintain records of ownership of the NFT, to which this Agreement is attached.
6. **Contract Account** means an Address controlled by a Smart Contract.
7. **Token ID** means the value returned by the `mint()` function, used to uniquely identify a newly issued NFT.
8. **Transfer** means any operation performed thorugh the Smart Contract that assigns the NFT to a new Address.
9. **Burn** means any operation performed using the Smart Contract that results in the removal of the association between a Token ID and an Address, effectively destroying the NFT.
10. **Beneficiary / Beneficial Owner** means the Externally-Owned Account specified as owning the NFT at any given moment.
11. **Trustee** is the individual or entity appointed by the Beneficial Owner as the Trustee of the Trust.
12. **Grantor** is the individual or entity who creates the Trust and NFT by calling the `mint()` function on the Fabrica Smart Contract and deeding the Property into the Trust.
13. **Property** is the bundle of rights identified in the NFT Metadata which has been deeded into the Trust.
14. **Creation Date** is the time
15. **Trust Name** is the name of the Trust identified in the NFT Metadata.
16. **NFT Metadata** means the specifying data linked to the NFT, including Token ID, Trust Name, Property Legal Description, Property Address/APN, as well as links to the Operating Agreement, proof of title document, geohash, registry name, country name and sub territory.
17. [Confirmed transaction] --> [pulled from ricardian LLC] means a transaction that has been recorded on Ethereum (as defined above) in accordance with the Consensus Rules (as defined below) in a valid block whose hashed header is referenced by a commercially reasonable number of subsequent valid blocks on Ethereum. The initial number of such blocks shall be 12.
18. [Consensus rules] --> [pulled from ricardian LLC] means the rules for transaction validity, block validity and determination of the canonical blockchain that are embodied in Ethereum.

1. The NFT is minted via the Fabrica Smart Contract, and ownership records are maintained there
2. Any action that the owner of the trust wants to commit re: the digital title/the property/the trust shall only be valid and fully sufficient if instructed on Ethereum through the Smart Contract and under the conditions of this Agreement. 
3. Signature validity/consequence - Any signature or execution made through the use of private keys on Ethereum for any matters relating to the NFT, the Trust, the Token Mint, etc. shall be valid and fully sufficient, as if signed in writing.
4. Explanation of token contract options/actions
   1. Discuss above defined terms further


### 3. Trust Declaration

1. At creation, the Grantor mints the NFT and attaches this Agreement to the NFT Metadata. Once minted, ownership records for the NFT will be kept by the Fabrica Smart Contract. After creation of the NFT, the Grantor deeds the Property into the Trust. At that point, legal and beneficial ownership of the Property will remain in the Trust, despite transfer of the NFT, until such time as the Trust is dissolved. The Beneficiary will be entitled to all rights related to the Property, as described more fully in [**section**]. 
2. The Trustee and Beneficiary are authorized to execute any amendment or restatement of this Agreement in the manner provided in [**section**] so long as such amendment or restatement is not inconsistent with the provisions of this Agreement. 
3. Title to all of the assets of the Trust shall be vested in the Trust until the Trust dissolves; provided, however, that if the applicable laws of any jurisdiction require that title to any part of the assets of the Trust be vested in a party to the Trust, then title to that part of the assets of the Trust shall be vested in the Beneficiary to the extent so required, with such vested title remaining subject, however, to the assignment and transfer provisions of [**section**].
4. The Trust is not intended to be, shall not be deemed to be, and shall not be treated as a general partnership, limited partnership, joint venture, corporation or joint stock company, and should for all purposes be considered revocable by the Beneficiary.

### 4. Contribution into trust / trust creation

1. Discuss mechanism for trust creation + granting property into the trust
2. Need clarity here on lazy mint mechanism

### 5. Grantor rights and representations

1. The Grantor is the creator of the Trust and is responsible for funding of the Property into the Trust following creation. Following creation and funding of the Trust, the Grantor (except in his capacity as Trustee/Beneficiary) will have no rights regarding the Trust Property, the Digital Title, or the management of the Trust, and will not retain any voting, director appointment, consent, approval or management rights with respect to the Trust Property or the Trust. Further, Grantor will not have any right to require the Beneficiary or Trustee to consult with Grantor with respect to the exercise of such rights and neither the Beneficiary nor the Trustee is required to consult with Grantor with respect to such rights, and the Grantor will have no right to remove or to replace the Beneficiary or Trustee. For purposes of this Agreement, the Trust is not deemed to be an affiliate of Grantor or of any of Grantor’s affiliates.
2. [**need to think through the consequences of this. properties can be loaded with an easement (think right of entry easement by the utility co.) and that shouldn't be a default under the trust agreement. also need to understand better WHO is being rep'd to here**] Immediately Prior to Grantor’s conveyance of the Property into the Trust, Grantor represents and warrants:
   1. That to the best of Grantor’s knowledge, Grantor owns fee simple record title to the Property, free and clear of all liens, special assessments, easements, reservations, restrictions and encumbrances, and there are no tenancy, rental, leases, licenses, parties in possession, or other occupancy rights or agreements affecting the Property. 
   2. That Grantor has not received any notice, and has no knowledge, that the Property or any portion or portions thereof is or will be subject to or affected by:
      1.  any special assessments, whether or not presently a lien thereon; or
      2. any condemnation, eminent domain, change in grade of public streets, or similar proceeding.
   3. That there are no actions, suits or proceedings of any kind or nature whatsoever, legal or equitable, affecting the Property or any portion or portions thereof or relating to or arising out of the ownership of the Property, in any court or before or by any federal, state, county or municipal department, commission, board, bureau, or agency or other governmental instrumentality.
   4. That Grantor has the full right, power and authority to enter into and deliver this Agreement and to perform all covenants and agreements of Grantor hereunder.
   5. That Grantor has not received any notice and has no actual knowledge that the Property has ever been used by previous owners and/or operators or Grantor to generate, manufacture, refine, transport, treat, store, handle or dispose of Hazardous Substance. Grantor has no actual knowledge of the Property having ever contained asbestos, PCB or other toxic materials.
   6. To the best of Grantor’s actual knowledge, there are no pollutants, contaminants, petroleum products or by-products, asbestos or other substances, whether hazardous or not, on or beneath the surface of the Property.
   7. There are no service contracts, maintenance or management agreements, commission or brokerage agreements, or other similar agreements affecting the Property.

### 6. Trustee obligations, fees and indemnification

### 7. Beneficiary/token owner rights

1. statement on estate planning + personal responsibility of beneficiary to pay all taxes etc.

### 8. No individual ownership

1. Trust property is in name of trust, and if not, then in name of beneficial owner

### 9. Trust proceeds

1. More beneficiary rights (maybe can be collapsed into above)

### 10. Trust modifications/amendments

1. This Agreement may be modified by the Beneficial Owner at any time by [running the update function or] attaching the updated agreement to the NFT. While the NFT metadata will only display the most current operating agreement, the history of the Agreement is stored on Ethereum, and is publicly available. [fede note: I'm still undecided on this. it's potentially quite risky and a possible vector to rug ppl. on the other hand, not allowing upgradability would froze the property in the agreement version used at minting time, and updates would require an unconvenient tranfer to a new NFT]

### 11. Trust termination

1. Process for termination
2. Grantor holds no right of termination, nor is any termination subject to grantor’s will/impact/influence

### 12. Miscellaneous

1. If any part of any provision of this Agreement or any other agreement, document or writing given pursuant to or in connection with this Agreement shall be invalid or unenforceable under applicable law, said part shall be ineffective to the extent of such invalidity only, without in any way affecting the remaining part of said provision or the remaining provisions of this Agreement.
2. The headings of the sections and subsections of this Agreement are inserted for convenience of reference only and do not form a part or affect the meaning hereof. Wherever used herein, a pronoun in any gender shall be considered as including any other gender pronoun. References to the singular include the plural, and vice versa.
3. To the extent it is not contrary to a strong public policy of the jurisdiction, if any, having a more significant relationship to this Agreement, this Agreement, the rights and obligations of the parties hereto, and any claims and disputes relating thereto, shall be governed by and construed in accordance with the laws of the State of California (not including the choice of law rules thereof).
4. The parties to this Agreement hereby consent to the non-exclusive jurisdiction of any State or Federal Court of competent jurisdiction located within the State of California, in the County of San Francisco, in connection with any actions or proceedings arising directly or indirectly from this Agreement.

