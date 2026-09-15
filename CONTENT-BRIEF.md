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
Order-of-magnitude anchors (approximate, for intuition):
- Grains of sand on Earth: ~10^18–10^20
- Stars in the observable universe: ~10^22–10^24
- Human cells across all living people (ballpark): ~10^30

So **2^128 (~10^38)** is already far beyond “all the sand on Earth,” and even beyond “sand × stars × a huge pile of cells” in casual storytelling — say it carefully: *if you multiplied all the sand on Earth by all known stars and still multiplied by a generous estimate of all human cells on the planet, you’d still be short of the size of a 12-word seed space.* Then: **24 words (~10^77)** is roughly **another full 12-word universe** larger than that — not double, but ~10^38 times larger again.

### Multisig odds (intuition, not a single formula)
Multisig does not replace seed strength; it changes **who must cooperate**. Example 2-of-3: an attacker needs **two** independent keys (or to compromise two devices/people), not one. Explain as layered control, with calm copy.

## Amazon dice (affiliate-ready links; no claim of endorsement)
- 5-pack example: https://www.amazon.com/dp/B00CKXGBE4 (Brybelly professional casino dice set of 5)
- Alternate 5-pack: https://www.amazon.com/dp/B005OLV568
Prefer linking a set of **5** (enough for base-6 entropy workflows) and note people often buy **two sets (10 dice)** for faster rolling. Do not invent other product claims.

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
