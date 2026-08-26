# Repository Guide

This repository is the public, CC0-licensed home of the Fabrica Trust Agreement — the legal instrument linking a real property held in trust to the Property Token that controls it. Current version: **v4.4** (adopted 2026-08-24, IPFS CID `bafkreih72odii5wcwluejt67is5q4zgdqiwqabzkg4pr5vys6o77pgujw4`).

## Files

- `connectors/us/us-trust-agreement.md` — the operative instrument (authoritative; read it, don't summarize from memory)
- `connectors/us/CHANGELOG.md` — version history with change-by-change entries and the version/IPFS CID table
- `README.md`, `connectors/us/README.md` — overviews
- `DISCLAIMER.md`, `LICENSE` — legal notices

Everything is hand-edited; there is no build, CI, or generated content.

## The one rule that makes this repo different

**Never edit adopted agreement text in place.** The Token ID of every trust is derived from the exact language of its agreement (Section 2.17), and each trust is governed by the version its Property Token referenced at mint. Any change to the agreement text — including a typo fix — is a new version. The only edits permitted to `us-trust-agreement.md` are those made as part of a proposed version, clearly marked as such.

## How versions ship

New versions are proposed as a single pull request carrying a proposal banner at the top of the agreement text; comment and critique happen on the PR. **Merging the PR is adoption.** At adoption: the banner is removed, the adopted file is pinned to IPFS, the CID is recorded in the changelog entry and version table, and the READMEs and this file are updated. Prior adopted texts remain retrievable via the CIDs in the changelog table.

To verify that the current file matches its published CID:

```bash
python3 -c "import hashlib,base64,sys;d=open(sys.argv[1],'rb').read();print('b'+base64.b32encode(b'\x01\x55\x12\x20'+hashlib.sha256(d).digest()).decode().lower().rstrip('='))" connectors/us/us-trust-agreement.md
```

## Changelog conventions

Reverse-chronological `#### v4.N` entries: a bold lead paragraph stating theme and scope, thematically grouped bullets each with a bold label and section number(s), closing with ``IPFS CID: `<cid>` ``. A version/CID/gateway-link table sits at the bottom of the file.

## Writing rules

- **onchain** and **offchain** — one word, no hyphen.
- Use the agreement's defined terms exactly: "Property Token," "Beneficiary," "Beneficial Interest," "Trustee," "Account," "Contract Account," "Smart Wallet," "Functional Contract," "Owner Rights," "Notice of Lost Token Control," "Quiet Period."
- The agreement is a legal instrument. Do not modify its text without explicit instruction; never invent or approximate a citation; when describing a provision, quote or closely track the operative text rather than paraphrasing — the instrument's own qualifications matter.
- These notes are repository conventions only. They are not legal advice, are not part of the Fabrica Trust Agreement, and are not to be used to construe it; the operative text controls.
