# myprivatekeys.com

Educational static site about **entropy**, **SSH** keys, and **Bitcoin (BIP39)** seed phrases.

Teach process and intuition only. **Never** generate or paste real private keys or seed phrases in this repo or on the live site. There is no backend and no key-generation script.

Domain: [myprivatekeys.com](https://myprivatekeys.com)

See `CONTENT-BRIEF.md` for the v1 brief.

## Open locally

This is plain HTML and CSS. From the repo root:

```bash
python3 -m http.server 8080
```

Then visit [http://127.0.0.1:8080/](http://127.0.0.1:8080/).

You can also open `index.html` directly in a browser. A local server is nicer so paths and the mobile menu script behave the same as on the live site.

## Pages

| File | Topic |
| --- | --- |
| `index.html` | Why entropy matters (sand × stars × cells; 12 vs 24 magnitudes) |
| `ssh.html` | Ed25519, passphrase, never share the private key, `authorized_keys` |
| `bitcoin.html` | BIP39, dice entropy, checksum at a high level, write offline |
| `multisig.html` | 2-of-3 as layered control, not a replacement for seed strength |
| `dice.html` | Casino-style 5-pack Amazon links; people often buy two sets (10 dice) |

Shared styles live in `css/styles.css`. Optional nav toggle is `js/nav.js`. Illustrations are in `assets/`.

## Magnitudes (plain language)

- BIP39 wordlist: 2048 words
- 12-word seed ≈ **128 bits** → about **2^128 ≈ 3.4×10^38** possibilities
- 24-word seed ≈ **256 bits** → about **2^256 ≈ 1.2×10^77** possibilities
- 12 → 24 is **not twice as strong**. +128 bits ≈ **2^128 times** more possibilities (~10^38×)

## What this repo will not include

- No forms that accept a seed or private key
- No scripts that generate keys or map dice rolls to words
- No “validate my phrase” tools

If a website offers to create or check a recovery phrase for you, close it.
