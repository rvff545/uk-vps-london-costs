# Best UK VPS: Do You Need a London Data Centre, What Does Year Two Cost, and Which Plan Fits a Small UK Site? (Full Plan Table, VAT and Add-On Notes)

Start with two numbers for any UK VPS you are considering: the monthly cost with VAT included, and the same figure once any introductory term ends. Those two decide more than the spec sheet does. OVHcloud's VPS-1 is £3.31 a month before VAT and £3.97 with it. Contabo's Cloud VPS 4 is €4.40 a month for the first 24 months, then €5.50. A list that quotes only the first number is telling you half the price.

AkkoCloud sells KVM virtual servers from San Jose, Frankfurt and London, priced in CNY with Alipay checkout. The London location is the part that matters if your visitors are in Britain; the rest of its network is built around a premium return route to mainland China, which is either the reason you want it or a feature you will never use. Below is the full plan table, the annual-versus-quarterly arithmetic, what VAT and add-ons do to the bill at four better-known providers, and a straight answer on who should not buy any of this.

> **Quick answer:** A small UK-facing site (a brochure site, a staging box, one API service) runs comfortably on AkkoCloud's 1 GB annual plan at 699 CNY/year, which includes 20 GB SSD and 1.2 TB of monthly transfer. If you need a GBP invoice with VAT and 4 GB of RAM, OVHcloud's VPS-1 at £3.97 incl. VAT is the cleaner comparison. 👉 [See AkkoCloud's current plans and which ones deploy in London](https://bit.ly/akkocloud)

## What a UK data centre actually changes

London, Manchester and Maidenhead are where most UK capacity sits. A server in one of them shortens the network round trip for UK visitors, and that is most of the benefit. Hosting close to your audience has at most a marginal effect on UK search rankings, so treat location as a latency decision.

The second benefit is jurisdictional. Keeping customer data on a server inside the UK makes UK GDPR paperwork simpler to describe to a client or an auditor. It does not make the company British. OVHcloud, Contabo, IONOS and AkkoCloud all sell UK capacity while being headquartered elsewhere, so contract law, invoicing currency and support hours still follow the parent company.

That last point bites small businesses more often than latency does. If your accountant wants a VAT invoice in GBP, a CNY checkout creates a conversation you would rather not have in April. AkkoCloud's payment flow is built around Alipay and other China-friendly methods, and its ticket support and Telegram community operate in Chinese. Neither is a problem for a developer running a side project. Both are worth knowing before you move a client's store onto it.

## AkkoCloud's plans, in full

Every plan below is a single-core KVM slice. The differences are RAM, SSD size, monthly transfer and how you pay. Nothing in the catalogue has more than one vCPU, so if your workload needs multiple cores, this is the wrong shop.

| Plan (billing) | vCPU / RAM / SSD | Transfer / port | Price | Order |
| --- | --- | --- | --- | --- |
| 512 MB, quarterly | 1 / 512 MB / 10 GB | 500 GB · 500 Mbps | 99 CNY per quarter | [Order the 512 MB quarterly plan](https://bit.ly/akkocloud) |
| 512 MB, annual | 1 / 512 MB / 10 GB | 500 GB · 500 Mbps | 299 CNY per year | [Order the 512 MB annual plan](https://bit.ly/akkocloud) |
| 768 MB, quarterly | 1 / 768 MB / 15 GB | 800 GB · 500 Mbps | 149 CNY per quarter | [Order the 768 MB quarterly plan](https://bit.ly/akkocloud) |
| 768 MB, annual (London special) | 1 / 768 MB / 15 GB | 800 GB · 300 Mbps* | 449 CNY per year | [Order the 768 MB annual special](https://bit.ly/akkocloud) |
| 1 GB, annual | 1 / 1 GB / 20 GB | 1.2 TB · 500 Mbps | 699 CNY per year | [Order the 1 GB annual plan](https://bit.ly/akkocloud) |
| 768 MB, monthly (600 GB) | 1 / 768 MB / 10 GB | 600 GB · 500 Mbps | 50 CNY per month | [Order the 50 CNY monthly plan](https://bit.ly/akkocloud) |
| 768 MB, monthly (1 TB) | 1 / 768 MB / 15 GB | 1 TB · 500 Mbps | 75 CNY per month | [Order the 75 CNY monthly plan](https://bit.ly/akkocloud) |
| 1.5 GB, monthly | 1 / 1.5 GB / 20 GB | 1.5 TB · 500 Mbps | 110 CNY per month | [Order the 1.5 GB monthly plan](https://bit.ly/akkocloud) |
| 2 GB, monthly | 1 / 2 GB / 30 GB | 3 TB · 500 Mbps | 233 CNY per month | [Order the 2 GB monthly plan](https://bit.ly/akkocloud) |

\*The London annual special is a separate SKU from the monthly slices: same 1 core, different RAM steps, and a 300 Mbps port on the listing rather than 500 Mbps. Confirm the port and transfer cap on the order page before paying.

Two things about that table. Prices are quoted in CNY, so the amount your card or Alipay converts is the amount you actually pay; there is no point quoting a GBP equivalent that will be wrong by the time you check out. And plan availability differs by location: the order page shows which of San Jose, Frankfurt and London a given slice can be deployed in, and London is not guaranteed on every row.

Which tier fits:

- **299 CNY/year (512 MB).** A static site, a reverse proxy, a monitoring or DNS node, or one small service that does not keep a database in memory. This is the plan for people who know what they are doing with 512 MB.
- **449 CNY/year (768 MB).** A light WordPress install with a page cache, or two or three containers.
- **699 CNY/year (1 GB).** The smallest slice worth putting a database-backed site on. If you are unsure, this is the one.
- **110–233 CNY/month (1.5–2 GB).** Staging plus production, a build pipeline, or a client site you would rather not rebuild later.

## Annual versus quarterly: the same slice, two prices

AkkoCloud's two smallest slices are sold both ways, and the annual price is the cheaper one per month. Pay quarterly on the 512 MB slice and you spend 396 CNY a year (99 × 4) instead of 299, roughly 25% more. On the 768 MB slice the gap is the same shape: 596 CNY across four quarters against 449.

That pattern is industry-standard, and it is where most "cheap VPS" comparisons go wrong. Contabo's €4.40 is not a discount on the monthly rate, it is a discount for committing to 24 months: 24 months at €4.40 comes to €105.60, and the following 12 months at the €5.50 list price add €66, so three years average out at about €4.77 a month. Fasthosts' VPS 1 goes from £2 to £3 a month once the introductory period ends, which means year one costs roughly £30 and year two costs £36. Its own pages give different lengths for that introductory window, so read the checkout rather than the blog post.

The arithmetic to run before you buy anything: multiply the renewal price by 24 and add the first-year cost. That total, not the headline, is what you are comparing.

## VAT, currency, and why "from £2" is not a comparison

OVHcloud publishes both figures on the same page: £3.31 a month excluding VAT, £3.97 including it. That 20% gap is the UK standard rate, and it is the difference between a plan that looks cheaper than a rival and one that does not.

IONOS advertises its VPS line "from £2/mth". The page does not state whether that figure includes VAT, so the number to compare is whatever the checkout totals, not the banner. Contabo lists in euros but accepts payment in pounds, which means the GBP amount depends on its conversion rather than yours. AkkoCloud prices in CNY and settles through Alipay.

Any table that puts £2, €4.40, $5 and 299 CNY in the same column and calls it a price comparison is not one. Convert at checkout, add VAT where it applies, and compare the second-year figure.

## The add-ons that quietly cost more than the server

Backups are the usual culprit. IONOS charges Cloud Backup from £0.045 per GB per month excluding VAT, so 100 GB of backup runs £4.50 a month on top of a plan that starts at £2. Its Plesk Obsidian licence is £5 a month, an extra IPv4 address is £5, and Plesk itself needs at least 20 GB of storage on Linux or 32 GB on Windows. Fasthosts lists Acronis backups at £0.20 per GB. On either provider, protecting a modest site can cost more than hosting it.

OVHcloud includes a daily backup of the previous 24 hours with every VPS, which is unusual at this price. Read its footnotes anyway: VPS instances in Mumbai, Singapore and Sydney carry monthly traffic quotas (500 GB on VPS-1, 1 TB on VPS-2 and VPS-3, 3 TB on VPS-4) and are throttled to 10 Mbps once exceeded, and Local Zones drop preinstalled apps, Windows, additional storage, monitoring, extra IPs, load balancing and managed databases. None of that affects a UK deployment today. It matters if you plan to add an Asian node later on the same product.

Contabo's "unlimited traffic" is governed by a fair-usage policy, and postpaid contracts need four weeks' notice to cancel. AkkoCloud's plan listings do not mention snapshots or backups at all, so assume you are responsible for your own: a scheduled restic or rsync job to cheap object storage is the standard answer.

## How the better-known UK options compare

Pure information, no links, same rules as above: these are the entry configurations and what each price assumes.

| Provider | Entry configuration | Listed price | What the price assumes |
| --- | --- | --- | --- |
| OVHcloud | VPS-1: 2 vCores / 4 GB / 40 GB NVMe, 500 Mbps | £3.31 ex. VAT, £3.97 incl. VAT per month | Monthly billing; daily backup of the previous 24 hours included; UK among 13 European geolocations |
| Contabo | Cloud VPS 4: 4 vCPU / 8 GB / 100 GB SSD, 200 Mbit/s | €4.40/month for the first 24 months, €5.50 after | 24-month introductory pricing; fair-usage traffic policy |
| IONOS | VPS line, from £2/month | £2/month | VAT status not stated on the page; 99.99% availability claim; UK, Germany, Spain or US location |
| Fasthosts | VPS 1, UK data centres only | £2/month introductory, £3/month after | Introductory length differs between Fasthosts' own pages; backups £0.20/GB extra |

Put OVHcloud's VPS-1 next to AkkoCloud's 1 GB plan and the trade is clear. OVHcloud gives you four times the RAM, twice the cores and a VAT invoice for £3.97 a month including tax. AkkoCloud gives you a lower entry cost and a London box with a China-optimised return route. If every one of your visitors is in Britain, that route is dead weight.

## Who should not buy this

**You only need shared hosting.** A brochure site with no server-side logic and no root access requirement is cheaper and better looked after on a shared plan. Someone else patches the OS.

**You want managed operations.** AkkoCloud, OVHcloud and Contabo all sell unmanaged root access. If you would rather not handle updates, firewalls and migrations yourself, a managed VPS costs more and is the right product.

**You need more than 2 GB of RAM.** AkkoCloud's listed catalogue tops out at 2 GB on a single core. Contabo's Cloud VPS 8 gives 8 vCPU and 24 GB for €11.20 a month on the introductory term, and €14 after it.

**You need English-language phone support and a GBP VAT invoice.** Those are legitimate reasons to pay more. Buy from a UK-billing provider and stop optimising the last 50p.

## FAQ

**Does a London data centre make a UK site faster?**
It cuts the network round trip for UK visitors, which is the main gain. Server CPU, caching and your CMS do the rest. A 512 MB London box with no page cache will feel slower than a Frankfurt box that has one.

**Can I pay monthly?**
Yes on four slices (50, 75, 110 and 233 CNY a month) and quarterly on the two smallest. Annual billing is about 25% cheaper per month where both options exist.

**Are backups included?**
OVHcloud includes a daily backup of the previous 24 hours on every VPS. IONOS and Fasthosts charge separately, from £0.045/GB/month and £0.20/GB respectively. AkkoCloud's listings do not mention backups or snapshots, so plan your own from day one.

**Is CN2 GIA worth paying for if all my visitors are in the UK?**
No. It is a premium return route to mainland China, useful when you also serve Chinese users and irrelevant to a visitor in Manchester. Judge the London plan on RAM, transfer and price like any other.

**Do I have to rebuild the server to upgrade?**
OVHcloud allows upgrades from its control panel at any time without a rebuild. AkkoCloud's public plan information does not describe an upgrade path, so ask support before you buy if you expect to grow within a year.

## How to decide

- **One small site, low traffic, comfortable on the command line:** AkkoCloud 512 MB annual at 299 CNY, or the 768 MB at 449 if it runs WordPress. 👉 [Start with the annual 512 MB plan](https://bit.ly/akkocloud)
- **A database-backed site or a couple of containers:** the 1 GB annual at 699 CNY.
- **Several client sites:** do not stack them on 1 GB. Either the 2 GB monthly slice at 233 CNY, or OVHcloud's VPS-1 at £3.97 incl. VAT for the extra cores and the invoice.
- **UK and Chinese visitors from one box:** the London plan is the unusual part of AkkoCloud's offer, and the only scenario where its routing earns its keep.

Before you pay, confirm three things: the total including VAT for year one and year two, the refund and cancellation terms (AkkoCloud's are not spelled out in its public plan information, so ask before transferring money), and that the slice you are ordering is the London SKU rather than San Jose.

👉 [Check AkkoCloud's London plans and current pricing](https://bit.ly/akkocloud)
