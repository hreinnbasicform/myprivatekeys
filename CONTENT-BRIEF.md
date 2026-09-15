# myprivatekeys.com — site brief

Educational SEO site. Pleasant sage/cream vibes. Teach process only — **never generate real SSH private keys, Bitcoin seeds, or recovery phrases**.

## Sections
1. Home / why entropy matters
2. SSH & systems private keys (ed25519 best practices, passphrase, never share private key, authorized_keys)
3. Bitcoin / BIP39 (dice/offline entropy, 12 vs 24 words, checksum concept at high level, write offline, never type into a website)
4. Multisig (2-of-3 explained)
5. Gear: link to casino-grade dice on Amazon

## Odds language (use these magnitudes; keep plain English)
- BIP39 wordlist size: 2048 words.
- 12-word seed ≈ **128 bits** of entropy → about **2^128 ≈ 3.4×10^38** possibilities.
- 24-word seed ≈ **256 bits** → about **2^256 ≈ 1.2×10^77** possibilities.
- Going from 12→24 words is not “twice as strong”; each extra bit **doubles** the search space. +128 bits ≈ **2^128 times** more possibilities (~10^38×).

### Metaphor (sandbox → cosmos)
Locked teaching numbers (order-of-magnitude, not lab measurements):
- **GSE** = all grains of sand on Earth = **10^18** (show 1 + 18 zeros)
- **SOU** = stars in the observable universe = **10^22** (show 1 + 22 zeros)

GSE alone is tiny next to 2^128. SOU alone is still far short of 2^128. **GSE × SOU = 10^40** is only about the same ballpark as a 12-word seed (~3.4×10^38) — slightly larger, not a different universe. Then: **24 words (~10^77)** is roughly **another full 12-word universe** larger than 12 words — not double, but ~10^38 times larger again. Drop cells from the main comparison.

### Multisig odds (intuition, not a single formula)
Multisig does not replace seed strength; it changes **who must cooperate**. Example 2-of-3: an attacker needs **two** independent keys (or to compromise two devices/people), not one. Explain as layered control, with calm copy.

## Amazon dice (ordinary product links; no claim of endorsement)
- 5-pack example: https://www.amazon.com/dp/B00CKXGBE4 (Brybelly professional casino dice set of 5)
- Alternate 5-pack: https://www.amazon.com/dp/B005OLV568
Prefer linking a set of **5** (enough for base-6 entropy workflows) and note people often buy **two sets (10 dice)** for faster rolling. Do not invent other product claims.

Teach the offline process on `dice.html`: roll in private, record faces, never photograph into a cloud album, never type rolls into a website. Mapping dice entropy to BIP39 words must happen on an offline / air-gapped tool the reader already trusts. SeedSigner (https://seedsigner.com/) is one educational example of air-gapped Bitcoin signing / seed tooling that can include dice-to-mnemonic flows — not an endorsement or affiliate. Warn against random websites, browser extensions, and online “dice to seed” tools. Never add a converter on this site.

## Images (attached / in uploads)
Use as hero/section art:
- entropy-sand-scale.png — scales of chance
- bip39-12-vs-24.png — 12 vs 24 (if tile count looks wrong, prefer correct copy in HTML over the graphic’s tile count)
- multisig-2of3.png
- ssh-vs-bitcoin.png

## Tech
Static site (HTML/CSS, optional light vanilla JS for nav). SEO meta, clean URLs or simple multipage (`index.html`, `ssh.html`, `bitcoin.html`, `multisig.html`). README with best-practice notes. No backend. No scripts that generate keys.

## Success
PR (or main commit) with pleasant static site, images wired, odds section readable, Amazon dice links present, strong disclaimers.
