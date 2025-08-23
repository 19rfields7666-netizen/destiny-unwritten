# Hover Email Setup (Forwarding or Mailbox)

You can point **hello@destinyunwritten.com** to your current inbox using Hover. Two routes:

## Option A — Free-ish Forwarding
1. In Hover, open your domain → **Email** → **Forwarding**.
2. Create forwarder: **hello@destinyunwritten.com → yourgmail@gmail.com**.
3. DNS (Hover usually manages automatically):
   - MX: `mx.hover.com.cust.hostedemail.com` (10)
4. SPF (TXT at root): `v=spf1 include:hover.com ~all`

## Option B — Paid Mailbox (later)
- Create a real inbox at Hover (costs monthly).
- Enable DKIM in Hover’s email settings; it will give you CNAME(s).
- Add DMARC (TXT at `_dmarc`):
  - `v=DMARC1; p=quarantine; rua=mailto:dmarc@destinyunwritten.com`

## Site Link
- The contact link already shows Discord first.
- Once forwarding works, the `mailto:hello@destinyunwritten.com` will be live without changing the site.
