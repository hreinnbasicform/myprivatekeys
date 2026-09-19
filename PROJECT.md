# myprivatekeys.com — project, ops, and status

Internal ops / ownership doc. **Do not put this file on the public site** (no footer link, no deploy of markdown). Editorial voice lives in [CONTENT-BRIEF.md](CONTENT-BRIEF.md). The public front door is [README.md](README.md).

## Ownership

- **Product owner agent:** MyPrivateKeys (this site’s owner bot).
- **Coordinate DNS / deploy** with **DNSbot** and **Chief of Staff** before changing apex DNS.
- **Ask Hreinn** before Amazon affiliate codes, ads, or domain / ads purchases.

Do not merge this PR, change DNS, or deploy as a side effect of a docs or content task unless that work is explicitly requested.

## Domains

- **Production domain:** [myprivatekeys.com](https://myprivatekeys.com)
- **Cloudflare zone:** active since **2026-08-09**, Free plan.
- **Cloudflare nameservers:** `javier.ns.cloudflare.com`, `marge.ns.cloudflare.com`

### Apex (do not switch yet)

The apex currently still serves a **placeholder**: the basicform.org homepage, via a **proxied A** record → **46.224.104.64**.

**Do not point the apex at the new educational site until Hreinn + DNSbot / Chief of Staff agree.**

### Mail (preserve)

Fastmail is already configured on the zone. When changing web DNS, **preserve mail records**:

- **MX:** `eu1-smtp.messagingengine.com`, `eu2-smtp.messagingengine.com`
- **DKIM:** `fm1`, `fm2`, `fm3` CNAMEs
- **SPF:** `include:spf.messagingengine.com`
- **DMARC:** `p=reject`

### www

No `www` record yet. Optional later.

### Review deploy

- **URL:** [https://mpk.basicform.org/](https://mpk.basicform.org/)
- Static files on Hetzner **hez-catlinkprod** at `/var/www/mpk`
- Cloudflare **A** `mpk` on basicform.org → **178.104.4.201** (proxied)

## Repo

- **Public GitHub:** https://github.com/hreinnbasicform/myprivatekeys
- Site work lives on branch **`cursor/educational-static-site-a98e`** / **[PR #1](https://github.com/hreinnbasicform/myprivatekeys/pull/1)** until merged.
- **Stack:** static HTML / CSS + tiny `js/nav.js`. No backend. **No Workers required for v1.**

## Deploy review site (mpk)

Host: **root@178.104.4.201** (hez-catlinkprod). SSH key: `/home/box/.ssh/id_ed25519`.

If SSH times out: open this computer’s public IPv4 on Hetzner **firewall-1** via API (`hauth.json`), or ask **Chief of Staff** / **Basicform.org Webmaster**.

Sync static files into `/var/www/mpk`. Exclude README / CONTENT-BRIEF / PROJECT markdown if desired. Ownership is often `1000:1000`.

Example (from a checkout of the site branch; **do not run this unless you were asked to deploy**):

```bash
rsync -av --delete \
  --exclude '.git' \
  --exclude '*.md' \
  ./ root@178.104.4.201:/var/www/mpk/
```

Then, if needed: `chown -R 1000:1000 /var/www/mpk` on the host.

This is the review host only. Apex cutover is a separate, coordinated DNS change.

## Safety / product rules (short)

- **Never generate or display** real or realistic seeds, private keys, WIF, hex keys, or BIP39 example phrases. Process-only education.
- **No affiliate** unless Hreinn explicitly approves.
- **No Google Fonts** / third-party trackers / analytics cookies on the site.

Full safety language and locked GSE / SOU numbers: [README.md](README.md). Copy guidance: [CONTENT-BRIEF.md](CONTENT-BRIEF.md).

## Status as of 2026-09

- **PR #1** open with the v1 site + photorealistic GSE / SOU scale graphic.
- Review live at [https://mpk.basicform.org/](https://mpk.basicform.org/).
- Apex **myprivatekeys.com** is **not yet switched**.
