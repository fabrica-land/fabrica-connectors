# Fabrica Trust Agreement

This Trust Agreement (*“Agreement”*) is entered into via issuing a Digital Asset (*"NFT"*) through the `mint()` function on the Fabrica Smart Contract (*"Smart Contract"*) by the Grantor using their private key on the Ethereum Blockchain. The Trust Name, Agreement and other identifiers are available in the metadata linked to the NFT that can be retrieved by calling the function `tokenURI()` of the Smart Contract. The Trust is entered into at the time the mint transaction has been confirmed on the Ethereum Blockchain.

## Recitals

- *Whereas* the grantor, trustee and beneficial owners want to digitize the title of the property to benefit from fully digital operations
- *Whereas* blockchain smart contracts allow for a secure and interoperable way of tracking ownership of digital assets via the use of an electronic legdger to immutably track, document and verify all transactions
- *Whereas* the parties agree to accept digital signature with the same legal consequence of wet signatures
- *Whereas* the parties intend to treat all operations done via blockchain as final, similarly to those performed through deeds
- Whereas on issuance of the digital asset, the parties agree to attach this Operating Agreement 
- *Whereas* the parties, for the purpose of standardization, intend to keep all the identifing information stored in the NFT this contract is attached to, while defining all the oeprations, definitions and procedures in the Agreement

## 1. Trust Purpose ##

1. The purpose of the trust is to create and maintain a link between ownership of the Property and its digital representation as a Digital Asset (*"NFT"*) on the Ethereum Blockchain, so as to allow for the time efficient, cost effective, accurate, and secure ownership, transfer, use and enjoyment of real property title in the digital environment. On creation, the Trust will take and hold title to the Property, and ownership of the Trust will be represented by ownership of the NFT. Regardless of the sale, hypothecation, or other transfer of the Digital Title, title to the Property will remain in the Trust until such time as the rightful owner of the NFT executes the `burn` function and removes the property from the Trust.
2. The owner(s) of the wallet holding the NFT shall be the beneficial owner(s) of the trust, and have the right to name the trustee. All rights and obligations in this agreement shall at all times be linked to the holder of the NFT, such that rightful possession of the NFT gives the holder full and total beneficial ownership.

## 2. Smart Contract ##

1. Definitions:
   1. *"Blockchain / Ethereum"* means the Ethereum mainnet and the consensus blockchain for such mainnet (networkID:1, chainID:1) as recognized by the official Go Ethereum Client implemented at https://github.com/ethereum/go-ethereum on the Effective Date.
   2. *"Address / wallet"* means a public key address on Ethereum.
   3. *"Smart Contract"* means the bytecode deployed on Ethereum used to maintain records of ownership of the NFT, to which this Agreement is attached.
   4. *"Token ID"* means the value returned by the `mint()` function, used to uniquely identify a newly issued NFT.
   5. *"Transfer"* means any operation performed thorugh the Smart Contract that assigns the NFT to a new Address.
   6. *"Burn"* means any operation performed using the Smart Contract that results in the removal of the association between a Token Id and an Address, effectively destroying the NFT.
   7. [Confirmed transaction] --> good idea to define it well, more importantly in the context of legal consequence of a function. Probably the execution of any operation (Such as "mint") should be considered effective only after a certain number of confirmations?
   8. [Consensus rules] --> not sure we need it
   9. [token updates] --> not sure we need it





b.   The NFT is minted via the Fabrica Smart Contract, and ownership records are maintained there

c.   Any action that the owner of the trust wants to commit re: the digital title/the property/the trust shall only be valid if first made on Ethereum and under the conditions of this Agreement. 

d.   Signature validity/consequence

​                        i.    Any signature or execution made through the use of private keys on Ethereum for any matters relating to the NFT, the Trust, the Token Mint, etc. shall be valid, as if signed in writing.

e.   Explanation of token contract options/actions

​                        i.   Discuss above defined terms further

\4.   Trust Defined Terms

a.   Beneficial Owner

b.   Trustee

c.   Grantor

d.   NFT metadata

​                        i.   Token ID

​                       ii.   Token Name

​                      iii.   Legal Description

​                      iv.   Property address / APN

​                       v.   Operating Agreement

​                      vi.   Deed / Proof of Title

​                      vii.   Geohash

​                     viii.   Registry

​                      ix.   Country

​                       x.   Subterritory

​                      xi.   [loader/grantor name or wallet?]

​                      xii.   [trustee name]

​                     xiii.   [beneficiary name]

\5.   Trust Declaration

a.   Trustee (or beneficiary?) declares trust

​                        i.   Need to figure out if this statement is necessary

b.   Contribution into trust / trust creation

​                        i.   Discuss mechanism for trust creation + granting property into the trust

​                       ii.   Need clarity here around lazy mint and how it interplays with trust

c.   Limiting grantor rights

​                        i.   Grantor reps/warranties?

d.   Trustee obligations, fees and indemnification

e.   Beneficiary/token owner rights

f.   statement on estate planning + personal responsibility of beneficiary to pay all taxes etc.

g.   No individual ownership

​                        i.   Trust property is in name of trust, and if not, then in name of beneficial owner

h.   Trust proceeds

​                        i.   More beneficiary rights (maybe can be collapsed into above)

i.   Trust modifications/amendments

j.   Trust termination

​                        i.   Process for termination

​                       ii.   Grantor holds no right of termination, nor is any termination subject to grantor’s will/impact/influence

\6.   