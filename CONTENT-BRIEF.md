# myprivatekeys.com — site brief

Educational SEO site. Pleasant sage / cream vibes. Teach process only.

**Never generate or display** real or realistic SSH private keys, Bitcoin seeds, WIF, hex keys, or BIP39 example phrases — not even as placeholders. No converters.

Ops, DNS, and deploy live in [PROJECT.md](PROJECT.md), not in this brief and not on the public site.

## Sections

1. **Home / why entropy matters** — GSE, SOU, 12 vs 24, photorealistic three-panel scale figure.
2. **SSH & systems private keys** — Ed25519 best practices, passphrase, never share the private key, `authorized_keys`.
3. **Bitcoin / BIP39** — dice / offline entropy, 12 vs 24 words, checksum at a high level, write offline, never type into a website.
4. **Multisig** — 2-of-3 explained as layered control.
5. **Dice / gear** — offline dice process, SeedSigner as an air-gapped example (not an endorsement), casino-style 5-pack shopping links without affiliate tags.

## Odds language (use these magnitudes; keep plain English)

- BIP39 wordlist size: **2048** words.
- **GSE** (all grains of sand on Earth) = **10^18** (show 1 + 18 zeros).
- **SOU** (stars in the observable universe, teaching estimate) = **10^22** (show 1 + 22 zeros).
- **GSE × SOU = 10^40** — about the same ballpark as a 12-word seed.
- 12-word seed ≈ **128 bits** → about **2^128 ≈ 3.4×10^38** possibilities.
- 24-word seed ≈ **256 bits** → about **2^256 ≈ 1.2×10^77** possibilities.
- Going from 12 → 24 words is not “twice as strong”; each extra bit **doubles** the search space. +128 bits ≈ **2^128 times** more possibilities (~10^38×).

### Metaphor (sandbox → cosmos)

Locked teaching numbers (order-of-magnitude, not lab measurements):

- GSE alone is tiny next to 2^128.
- SOU alone is still far short of 2^128.
- **GSE × SOU = 10^40** is only about the same ballpark as a 12-word seed (~3.4×10^38) — slightly larger, not a different universe.
- Then: **24 words (~10^77)** is roughly **another full 12-word universe** larger than 12 words — not double, but ~10^38 times larger again.

Drop cells from the main comparison. Prefer the numbers in the HTML if a graphic’s tile count looks short.

### Home figure (photorealistic scale panels)

`assets/entropy-sand-scale.png` is a full, uncropped three-panel figure used on the home page (and as the default `og:image` on several pages):

1. **Left:** a grain of sand under a magnifying glass next to a phone, plus a **tiny grain of salt on the iPhone screen** (the salt is not under the glass).
2. **Middle:** Earth from space = **GSE**.
3. **Right:** galaxy / deep-field = **SOU**.

Keep alt text and captions aligned with that scene. Do not recrop the figure so the salt grain or the glass disappears.

### Multisig odds (intuition, not a single formula)

Multisig does not replace seed strength; it changes **who must cooperate**. Example 2-of-3: an attacker needs **two** independent keys (or to compromise two devices / people), not one. Explain as layered control, with calm copy.

## Dice process and SeedSigner

Teach the offline process on `dice.html`:

- Roll in private, record faces on paper, never photograph into a cloud album, never type rolls into a website.
- Mapping dice entropy to BIP39 words must happen on an offline / air-gapped tool the reader already trusts.
- **[SeedSigner](https://seedsigner.com/)** is one educational example of air-gapped Bitcoin signing / seed tooling that can include dice-to-mnemonic flows — **not an endorsement** and not an affiliate.
- Warn against random websites, browser extensions, and online “dice to seed” tools.
- Never add a converter on this site.

### Amazon dice (ordinary product links)

No affiliate tags. No “affiliate-ready” copy. No claim of endorsement.

- 5-pack example: https://www.amazon.com/dp/B00CKXGBE4 (Brybelly professional casino dice set of 5)
- Alternate 5-pack: https://www.amazon.com/dp/B005OLV568

Prefer linking a set of **5** (enough for base-6 entropy workflows) and note people often buy **two sets (10 dice)** for faster rolling. Do not invent other product claims. Ask Hreinn before adding affiliate codes.

## Images

Use as hero / section art:

- `entropy-sand-scale.png` — photorealistic GSE / SOU scale panels (home)
- `bip39-12-vs-24.png` — 12 vs 24 (if tile count looks wrong, prefer correct copy in HTML over the graphic’s tile count)
- `multisig-2of3.png`
- `ssh-vs-bitcoin.png`

## Tone and tech

- Pleasant, trustworthy, non-alarmist. Sage / cream. System fonts only. No analytics cookies.
- Static site (HTML / CSS, optional light vanilla JS for nav). SEO meta, multipage (`index.html`, `ssh.html`, `bitcoin.html`, `multisig.html`, `dice.html`, `404.html`).
- No backend. No scripts that generate keys. No Workers required for v1.

## Success

PR (or main commit) with a pleasant static site, images wired, odds section readable, ordinary Amazon dice links present, strong process-only disclaimers, and repo docs that match the live copy.
