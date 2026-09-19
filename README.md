# myprivatekeys.com

Educational static site about **entropy**, **SSH / systems keys**, and **Bitcoin (BIP39)** seed phrases.

Two pillars:

1. **SSH and systems keys** — Ed25519, passphrases, `authorized_keys`, never sharing the private file.
2. **Bitcoin / BIP39** — dice-gathered entropy, 12 vs 24 words, checksum at a high level, writing a seed offline, multisig as layered control.

Teach process and intuition only. This is not a wallet, not a key factory, and not a converter.

**Domain (production):** [myprivatekeys.com](https://myprivatekeys.com) — apex is still a placeholder until Hreinn + DNSbot / Chief of Staff agree to switch it. **Review site:** [https://mpk.basicform.org/](https://mpk.basicform.org/)

Read **[PROJECT.md](PROJECT.md)** for ownership, DNS, hosting, and deploy. Read **[CONTENT-BRIEF.md](CONTENT-BRIEF.md)** for the editorial brief.

## Hard safety rules

These apply to the live site, this repo, screenshots, docs, and any agent working on the project.

- **Never generate or display** real or realistic seeds, private keys, WIF, hex keys, or BIP39 example phrases.
- Teach **process only**. Describe how people gather entropy and store secrets. Do not produce a secret.
- **No converters.** No dice-to-word mapper, no wordlist picker, no “validate my phrase” form, no key-generation script.
- Do not paste, invent, or “for illustration” a 12- or 24-word phrase. If a page needs an example, talk about the process — not the words.
- If a website offers to create or check a recovery phrase, close it. This site will never be that website.

There is no backend and no Workers requirement for v1.

## Tone and look

- Pleasant, trustworthy, **non-alarmist**. Calm copy. Sage / cream palette.
- **System fonts only** (`system-ui` / Georgia). No Google Fonts, no webfont CDNs.
- **No analytics cookies**, no accounts, no third-party trackers.
- Amazon shopping links are ordinary `amazon.com/dp/…` URLs with `rel="nofollow noopener noreferrer"`. **No affiliate tags** unless Hreinn explicitly approves.

## Locked teaching numbers

Order-of-magnitude pictures, not lab measurements. Keep these exact figures in copy.

| Token | Meaning | Value |
| --- | --- | --- |
| **GSE** | All grains of sand on Earth | **10^18** (1 + 18 zeros) |
| **SOU** | Stars in the observable universe (teaching estimate) | **10^22** (1 + 22 zeros) |
| **GSE × SOU** | Sand × stars | **10^40** — about the same ballpark as a 12-word seed |

- BIP39 English wordlist: **2048** words.
- 12-word seed ≈ **128 bits** → about **2^128 ≈ 3.4×10^38** possibilities.
- 24-word seed ≈ **256 bits** → about **2^256 ≈ 1.2×10^77** possibilities.
- GSE alone is tiny next to 2^128. SOU alone is still far short of 2^128. GSE × SOU (10^40) is only slightly larger than a 12-word space — not a different universe.
- 12 → 24 is **not twice as strong**. +128 bits ≈ **2^128 times** more possibilities (~10^38×). Twenty-four is another full 12-word universe, not 2×.

## Home figure (photorealistic scale)

`assets/entropy-sand-scale.png` is a full, uncropped three-panel figure:

1. **Left:** sand under a magnifying glass, next to a phone. A **grain of salt sits on the iPhone screen** (not under the glass).
2. **Middle:** Earth from space = **GSE**.
3. **Right:** galaxy / deep-field = **SOU**.

Prefer the numbers in the HTML if a decorative graphic’s tile count looks short.

## Pages

| File | Topic |
| --- | --- |
| `index.html` | Why entropy matters. GSE / SOU written out. 12 vs 24 magnitudes. Photorealistic scale figure. |
| `ssh.html` | Ed25519, passphrase, never share the private key, `authorized_keys`. |
| `bitcoin.html` | BIP39, dice entropy, checksum at a high level, write offline. |
| `multisig.html` | 2-of-3 as layered control, not a replacement for seed strength. |
| `dice.html` | Offline dice process, SeedSigner as an air-gapped example, casino-style 5-pack links. |
| `404.html` | Minimal not-found page with a home link and the process-only disclaimer. |

Shared styles live in `css/styles.css`. Optional nav toggle is `js/nav.js`. Illustrations are in `assets/`. Also: `robots.txt`, `sitemap.xml`, `favicon.svg`.

## Dice process and SeedSigner

Physical dice are one way people collect randomness away from a keyboard.

- Roll in a **private room**. Record faces on paper. Do not photograph rolls into a cloud album. Do not type faces into a website.
- Mapping dice entropy to BIP39 words must happen on an **offline / air-gapped** tool the reader already trusts.
- **[SeedSigner](https://seedsigner.com/)** is one educational example of air-gapped Bitcoin signing / seed tooling that can include dice-to-mnemonic flows. It is **not an endorsement** and not an affiliate.
- Warn against random websites, browser extensions, and online “dice to seed” tools.
- Example 5-packs (ordinary product links, no affiliate tags):
  - https://www.amazon.com/dp/B00CKXGBE4 (Brybelly professional casino dice set of 5)
  - https://www.amazon.com/dp/B005OLV568 (alternate 5-pack)
- A 5-pack is enough for base-6 workflows; people often buy **two sets (10 dice)** for faster rolling.

This site will not turn rolls into words.

## Open locally

Plain HTML and CSS. From the repo root:

```bash
python3 -m http.server 8080
```

Then visit [http://127.0.0.1:8080/](http://127.0.0.1:8080/).

You can also open `index.html` directly in a browser. A local server is nicer so paths and the mobile menu script behave the same as on the live site.

## What this repo will never include

- Forms that accept a seed, private key, WIF, hex key, or dice faces
- Scripts that generate keys or map dice rolls to words
- Realistic or example BIP39 phrases, even as placeholders
- “Validate my phrase” or “recover my wallet” tools
- Google Fonts, analytics cookies, or third-party trackers
- Affiliate-tagged shopping links (unless Hreinn explicitly approves)
- A Cloudflare Worker or backend for v1

Ops notes, DNS facts, and deploy steps stay in **[PROJECT.md](PROJECT.md)** — not on the public site.
