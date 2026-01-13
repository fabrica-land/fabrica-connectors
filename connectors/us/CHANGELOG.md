# Changelog
### Fabrica Trust

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
| 3.7     | `bafkreielajiqjyqjwofuxaep6heoxx6ag4ifum7u6mafvkkhuif2dcqvc4` | https://ipfs.fabrica.land/ipfs/bafkreielajiqjyqjwofuxaep6heoxx6ag4ifum7u6mafvkkhuif2dcqvc4 |
| 3.6     | `bafkreifiv6x6a77v6gnjxw3tfxo5exzo736x6fvr2inx46qpn3woemgxky` | https://ipfs.fabrica.land/ipfs/bafkreifiv6x6a77v6gnjxw3tfxo5exzo736x6fvr2inx46qpn3woemgxky |
| 3.5     | `QmNxY3ooc4VXbW6ETd1wVAxvajZYWu81U95MmWJiNBQw14` | https://ipfs.fabrica.land/ipfs/QmNxY3ooc4VXbW6ETd1wVAxvajZYWu81U95MmWJiNBQw14 |
| 3.4     | `QmeRZqhU59Vpn4JQvggBVQ97uMfmS68utweUury8n5JLPR` | https://ipfs.fabrica.land/ipfs/QmeRZqhU59Vpn4JQvggBVQ97uMfmS68utweUury8n5JLPR |
| 3.3     | `Qmf6Aia6gJfRgGyGroYft3kjxsLUhJEhMYVKPKj2JwY41Z` | http://ipfs.fabrica.land/ipfs/Qmf6Aia6gJfRgGyGroYft3kjxsLUhJEhMYVKPKj2JwY41Z |
| 3.2     | `QmcgEJkgCwizvs6Tu12jCaNMGciRNtH8dLA2TRS3aYWStX` | https://ipfs.fabrica.land/ipfs/QmcgEJkgCwizvs6Tu12jCaNMGciRNtH8dLA2TRS3aYWStX |
| 3.1     | `QmXRQx7wPxSwQDVVr1pTkiwvBHBUd1SYLbLgSn1Bvirqpc` | https://ipfs.fabrica.land/ipfs/QmXRQx7wPxSwQDVVr1pTkiwvBHBUd1SYLbLgSn1Bvirqpc |
| 3.0     | `QmRH7d7TGJ3DymLSRimjnH5cNGHzYfcvUTUA1tM9gizFY8` | http://ipfs.fabrica.land/ipfs/QmRH7d7TGJ3DymLSRimjnH5cNGHzYfcvUTUA1tM9gizFY8 |

