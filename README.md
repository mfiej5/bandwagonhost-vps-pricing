# cheapest VPS hosting: what a rock-bottom VPS actually costs in practice, with the full BandwagonHost plan and price breakdown

Anyone who types "cheapest VPS hosting" into a search box is usually trying to answer one deceptively simple question: how little money does a VPS actually cost before it becomes a waste of money? The advertised numbers are all over the place — some providers shout about $3 plans, others quietly bury renewal pricing two clicks deep. This article looks at what the real bottom of the market looks like, what you get (and don't get) at each price point, and then walks through one specific case study: BandwagonHost, a budget provider whose cheapest plan has been one of the most-discussed deals in the self-hosting world for years.

## What "cheapest" actually means in the VPS market

The entry level of the VPS market currently sits somewhere between $4 and $10 per month for a small cloud instance. DigitalOcean's cheapest shared-CPU droplet starts at $4 per month. Contabo's entry Cloud VPS 4 is listed at $9.25. A comparison site that aggregates pricing across dozens of providers puts the median entry price around $9–10 per month, with only a minority of providers going below $5.

Against that backdrop, BandwagonHost's 20G KVM plan at $49.99 per year works out to roughly **$4.17 per month** — which is why it keeps showing up in every "cheapest VPS" thread on Reddit and in nearly every budget VPS comparison. The interesting part isn't just the number. It's what the number includes, and what it doesn't.

Before going deeper into that plan, it helps to be clear about the three things that separate genuinely cheap-but-usable VPS hosting from the $1-a-month stuff that gives cheap hosting a bad name:

- **Virtualization type.** KVM gives you a real virtual machine with full root access and your own kernel. Some of the very cheapest offers use OpenVZ/LXC-style containers, where you share the host kernel and some software (Docker, certain VPN setups, custom kernels) simply won't run. All of BandwagonHost's current plans are KVM.
- **What the price includes.** At this end of the market, backups and snapshots are often paid extras. BandwagonHost includes free automatic backups and free snapshots on its KVM plans, which is unusual at the $4/month tier.
- **Traffic and port speed.** A 1 TB monthly transfer allowance on a 1 Gbps port is a meaningfully different product from "unlimited" traffic throttled to 100 Mbps.

## BandwagonHost's current lineup: the full price list

BandwagonHost (operated by IT7 Networks, and known as 搬瓦工 in Chinese communities) sells self-managed KVM VPS. Its catalog currently has three lines: the general-purpose KVM PROMO plans, the CN2 GIA "SPECIAL" plans aimed at China-optimized routing, and the E-Commerce SLA line in Los Angeles. Here's everything currently shown on the official order pages.

### KVM PROMO plans — the budget tier

These plans can be deployed in multiple datacenter locations (Fremont, Los Angeles, New York, Vancouver and others), and you can migrate between locations for free from the KiwiVM control panel.

| Plan | SSD (RAID-10) | RAM | CPU | Transfer | Port | Available billing cycles | Price (lowest cycle) | Purchase link |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 20G KVM | 20 GB | 1 GB | 2x Intel Xeon | 1 TB/mo | 1 Gbps | Yearly only | $49.99/year | [ View the 20G KVM plan](https://bit.ly/BandwagonHost) |
| 40G KVM | 40 GB | 2 GB | 3x Intel Xeon | 2 TB/mo | 1 Gbps | Semi-annual / annual | $52.99 per half year ($99.99/year) | [ Check 40G KVM pricing](https://bit.ly/BandwagonHost) |
| 80G KVM | 80 GB | 4 GB | 4x Intel Xeon | 3 TB/mo | 1 Gbps | Monthly to annual | $19.99/month ($199.99/year) | [ See the 80G KVM plan](https://bit.ly/BandwagonHost) |
| 160G KVM | 160 GB | 8 GB | 5x Intel Xeon | 4 TB/mo | 1 Gbps | Monthly to annual | $39.99/month ($399.99/year) | [ View 160G KVM details](https://bit.ly/BandwagonHost) |
| 320G KVM | 320 GB | 16 GB | 6x Intel Xeon | 5 TB/mo | 1 Gbps | Monthly to annual | $79.99/month ($799.99/year) | [ Check 320G KVM pricing](https://bit.ly/BandwagonHost) |
| 480G KVM | 480 GB | 24 GB | 7x Intel Xeon | 6 TB/mo | 1 Gbps | Monthly to annual | $119.99/month ($1,199.99/year) | [ See the 480G KVM plan](https://bit.ly/BandwagonHost) |

Every plan in this table also includes: 1 dedicated IPv4 address, a routed /64 IPv6 subnet, full root access, instant OS reload, manual ISO installs, instant rDNS editing, free automatic backups, free snapshots, and a 99.95% uptime guarantee. Supported operating systems cover AlmaLinux, Rocky Linux, CentOS, CentOS Stream, Debian, Ubuntu and Fedora, plus bootable ISOs you can attach yourself.

### CN2 GIA SPECIAL plans — the China-optimized tier

This is the line BandwagonHost is best known for. These plans run in premium Equinix facilities in Singapore, Osaka, Hong Kong and Tokyo, with direct routing via China Telecom CN2 GIA/CTG, China Unicom and China Mobile. BandwagonHost itself is blunt about the economics: CN2 GIA transit is expensive, which is why these plans cost several times more than the budget tier.

| Spec | Singapore (SG1) | Osaka | Hong Kong (HK2) | Tokyo (TY8) |
| --- | --- | --- | --- | --- |
| 40G: 2 GB RAM / 2 cores / 500 GB | $49.99/mo · $499.99/yr | $49.99/mo · $499.99/yr | $89.99/mo · $899.99/yr | $89.99/mo · $899.99/yr |
| 80G: 4 GB / 4 cores / 1 TB | $86.99/mo · $869.99/yr | $86.99/mo · $869.99/yr | $155.99/mo · $1,559.99/yr | $155.99/mo · $1,559.99/yr |
| 160G: 8 GB / 6 cores / 2 TB | $165.99/mo · $1,665.99/yr | $165.99/mo · $1,665.99/yr | $299.99/mo · $2,999.99/yr | $299.99/mo · $2,999.99/yr |
| 320G: 16 GB / 8 cores / 4 TB | $329.99/mo · $3,199/yr | $329.99/mo · $3,199/yr | $589.99/mo · $5,899.99/yr | $589.99/mo · $5,899.99/yr |
| 640G: 32 GB / 10 cores / 6 TB | $549.99/mo · $5,549.99/yr | $549.99/mo · $5,549.99/yr | $989.99/mo · $9,989.99/yr | $989.99/mo · $9,989.99/yr |
| 1280G: 64 GB / 12 cores / 8 TB | $1,059.99/mo · $10,559.99/yr | $1,059.99/mo · $10,559.99/yr | $1,889.99/mo · $18,989.99/yr | $1,889.99/mo · $18,989.99/yr |

Ports range from 1 Gbps (Hong Kong) to 5 Gbps (Singapore's larger plans). If your traffic isn't China-related, this tier makes little sense for you — the budget plans above are the same virtualization platform at a third of the price.

### E-Commerce SLA plans — Los Angeles, AMD EPYC, 99.99% SLA

The newest line, hosted in Los Angeles on AMD EPYC hardware with local NVMe RAID-10 storage, a 2.5 Gbps port (5 Gbps on the 160G plan), and a contractual 99.99% SLA. The network pages describe direct peering with Apple, Google, Facebook and ByteDance, alongside the same China Telecom/Unicom/Mobile routing.

| Plan | RAM (ECC) | CPU (AMD dedicated) | Storage | Transfer | Quarterly | Semi-annual | Annual | Purchase link |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 20G | 1 GB | 2 cores | 20 GB NVMe | 1 TB/mo | $65.89 | $125.99 | $239.99 | [ View the 20G E-Commerce plan](https://bit.ly/BandwagonHost) |
| 40G | 2 GB | 3 cores | 40 GB NVMe | 2 TB/mo | $116.99 | $219.99 | $399.99 | [ Check 40G E-Commerce pricing](https://bit.ly/BandwagonHost) |
| 80G | 4 GB | 4 cores | 80 GB NVMe | 3 TB/mo | $69.99/mo | $199.99 | $379.99 | $699.99 — [ See the 80G E-Commerce plan](https://bit.ly/BandwagonHost) |
| 160G | 8 GB | 6 cores | 160 GB NVMe | 5 TB/mo | $109.99/mo | $299.99 | $569.99 | $1,099.99 — [ View 160G E-Commerce details](https://bit.ly/BandwagonHost) |

## The $49.99/year plan, taken apart

Since this is the plan most people mean when they ask about the cheapest VPS hosting that's still worth running, it deserves its own section. Here's what $49.99 per year buys on the 20G KVM PROMO:

- **20 GB of RAID-10 SSD storage and 1 GB RAM.** Enough for a personal website, a small blog, a WireGuard/tailscale-style tunnel, a couple of lightweight services, or a learning sandbox. Not enough for a busy database server or a Kotlin-heavy application stack — 1 GB fills up fast once Java enters the picture.
- **2x Intel Xeon vCPU cores.** Shared, fair-use cores, not dedicated ones. Fine for bursty light workloads.
- **1 TB of transfer per month on a 1 Gbps port.** That's roughly 30+ GB per day of headroom, which covers the overwhelming majority of personal projects.
- **The full KiwiVM feature set.** BandwagonHost's in-house control panel handles start/stop, OS reload, an emergency VNC console, rDNS management, one-click datacenter migration, snapshots, usage statistics and an API. Migration between datacenters is free and doesn't touch your data.

The honest way to frame this plan: it's not the most powerful $4 you can spend, but it's one of the few places where $4 per month gets you a proper KVM virtual machine with included backups, snapshots, a 1 Gbps port and a 1 TB allowance. Third-party reviews land in roughly the same place — one recent review called it "one of the better deals in budget VPS" while being careful to note that the value is in the package, not raw performance.

There's one practical catch worth knowing before you order: BandwagonHost also periodically releases limited-edition plans (THE PLAN series, MINICHICKEN, Box series) with better specs at oddly low prices, and these sell out and restock unpredictably. If you catch one in stock, the math can be even better than the standard 20G plan. If you don't, the regular catalog above is what's actually available.

## How the budget tier compares when "cheapest" isn't the only question

A bare price comparison flatters BandwagonHost a bit and understates it at the same time. Here's the fair version.

**Where the 20G KVM wins:** it's annually billed at roughly $4.17/month, with included backups and snapshots that competitors at that price usually charge extra for, plus free location migration. DigitalOcean's $4 droplet, for instance, is hourly-billed and has excellent API and docs, but backups cost extra and there's no China-optimized routing anywhere in the lineup.

**Where it loses:** the CPU cores are shared Xeon vCores with fair-use limits defined in the terms of service, so sustained CPU-heavy workloads will be throttled; it's strictly self-managed, meaning no one will fix your misconfigured nginx for you; and you pay a full year up front, where hourly-billed clouds let you destroy a server after a day and pay pennies.

**Where Contabo fits:** if you need lots of RAM and storage for the money (8 GB-class instances), Contabo's $9–13 tiers give you far more raw resources than anything in BandwagonHost's budget line. The trade-off is different again: Contabo plans historically come with higher setup fees on short terms and a very different network profile.

If your actual requirement is "cheap box for a personal project in North America or Europe," all three are rational choices. If your requirement involves real users in mainland China reaching your server without the connection falling apart at peak hours, BandwagonHost's CN2 GIA plans are close to the only game in town at any price — which is the actual reason the brand has the reputation it has.

## What to check before you buy any cheap VPS

Whether you end up with BandwagonHost or someone else, these are the four checks that catch most regrets:

1. **Renewal price.** Some budget hosts use teaser first-term pricing. BandwagonHost's listed prices are the renewal prices, which is part of why the $49.99/year plan keeps its reputation — the second year costs the same as the first.
2. **Refund terms.** BandwagonHost offers a 30-day money-back guarantee and a 99.9% uptime guarantee, both spelled out in its terms of service and refund page. Check equivalents before buying anywhere, because several ultra-cheap providers are strictly non-refundable.
3. **Backup reality.** "Backups included" should mean automatic and free. On BandwagonHost's KVM plans it does — the order page lists free automatic backups and free snapshots explicitly.
4. **Support expectations.** Self-managed means you're the sysadmin. If you need someone to answer tickets about your application stack, that's not this category of product, at any price.

## Quick answers to the questions people actually search

**Is the cheapest VPS hosting reliable enough for a real website?** A well-run budget VPS from an established operator is fine for low-traffic production sites. BandwagonHost's uptime guarantee is 99.95% on its KVM plans, and the E-Commerce line raises that to a contractual 99.99% with service credits. Reliability at this tier depends more on your own configuration and backups than on the provider's marketing.

**What's the cheapest VPS with good China connectivity?** On BandwagonHost's current catalog, the cheapest CN2 GIA-routed plans are the 40G SPECIAL plans in Singapore or Osaka at $49.99/month (or $499.99/year). The budget KVM plans include some China-directed peering at certain locations, but the premium routes are what the brand is actually known for.

**Can I get a discount code?** Third-party coupon sites list various BandwagonHost codes with small sitewide discounts, and the company has historically run seasonal sitewide promos (past Black Friday and 11.11 events used recurring percentage codes). Nothing is permanently active, so treat any code you find as a nice-to-have rather than planning your budget around it — the standard catalog prices above are what you'll actually pay.

**Is monthly billing available?** Yes, from the 80G KVM plan upward. The 20G plan is annual-only; the 40G plan starts at semi-annual billing.

## The short version

If you just want the cheapest VPS hosting that won't waste your weekend, the decision tree is short. Learning, tunnels, a personal site, a small bot: the 20G KVM plan at $49.99/year is one of the most defensible $4-per-month purchases in hosting right now, and you can grab it here: [👉 Check current BandwagonHost stock and pricing](https://bit.ly/BandwagonHost). Growing project that needs more RAM: step up to the 80G KVM at $19.99/month. Production site with real users and a need for contractual uptime: the Los Angeles E-Commerce SLA line starts at $239.99/year. And if the whole point is serving users in China over a premium route, that's what the CN2 GIA tier is for — expensive, and for good reason.
