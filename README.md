# RackNerd vs CloudCone: Is the $11.29 Plan Enough, Do Renewals Stay Flat, and Who Should Pay $16.99 Instead? (Full RackNerd Plan Table + Recurring Codes)

RackNerd's entry KVM VPS is **$11.29/year**. CloudCone's 2026 Hashtag SSD entry plan is **$16.99/year**. For most people typing "racknerd vs cloudcone" into a search box, the $11.29 box is the one to buy, and the extra $5.70 at CloudCone only buys you something real if you need hourly billing, snapshots, or a server you assemble core by core.

The rest of this page is the part that decides it: RackNerd's full lineup with prices, the recurring codes that keep cutting 30% off renewals, what each control panel can and cannot do, what renews at what price, and the two numbers the popular comparison posts keep getting wrong.

> **Quick picks**
> - **Tightest budget, one small box:** RackNerd 1GB at $11.29/year (1 vCore, 24GB SSD, 2TB/month).
> - **The tier most buyers end up on:** RackNerd 3.5GB at $32.49/year (2 vCores, 65GB SSD, 7TB/month).
> - **Need hourly billing, snapshots, or on-demand RAM:** CloudCone SC2 from $0.00699/hour, or the $31.25/year SC2-1 with 3 cores and 2GB.
>
> 👉 [See RackNerd's current VPS specials and prices](https://bit.ly/RacKnerd)

## RackNerd's full VPS lineup, and which tier you actually need

All five KVM specials run on a 1Gbps port with one dedicated IPv4 and full root. Pricing below is the New Year 2026 annual rate.

| Plan | vCPU / RAM | SSD | Bandwidth | Price | Order |
| --- | --- | --- | --- | --- | --- |
| 1 GB KVM | 1 vCore / 1 GB | 24 GB | 2 TB/mo | **$11.29/yr** | [Order](https://bit.ly/RacKnerd) |
| 2 GB KVM | 1 vCore / 2 GB | 40 GB | 3.5 TB/mo | $18.29/yr | [Order](https://bit.ly/RacKnerd) |
| 3.5 GB KVM | 2 vCores / 3.5 GB | 65 GB | 7 TB/mo | **$32.49/yr** | [Order](https://bit.ly/RacKnerd) |
| 4 GB KVM | 3 vCores / 4 GB | 105 GB | 9 TB/mo | $43.88/yr | [Order](https://bit.ly/RacKnerd) |
| 6 GB KVM | 4 vCores / 6 GB | 140 GB | 12 TB/mo | $59.99/yr | [Order](https://bit.ly/RacKnerd) |

The 2GB plan is the one to think twice about. It doubles the RAM over the $11.29 box but keeps a single vCore, and single-core boxes get painful the moment a database and a web server compete for the same core. The jump from $18.29 to $32.49 buys a second core, 25GB more disk, and double the transfer, which is why the 3.5GB tier is the one flagged as most popular.

Where the tier ladder actually matters is memory ceilings on one-click apps. RackNerd's own app notes put Ollama, AnythingLLM, LibreChat and Hermes Agent at 4GB minimum, n8n and Coolify at 2GB, OpenClaw at 8GB. If you plan to run a local model or an agent stack, the $43.88 plan is the floor, and the $11.29 plan is a proxy or a small static site and nothing more.

**Shared hosting and dedicated servers**, for completeness:

| Shared plan | Storage | Bandwidth | Price |
| --- | --- | --- | --- |
| Shared 30 GB | 30 GB SSD | 2 TB | $5.59/mo |
| Shared 100 GB | 100 GB SSD | 3 TB | $9.59/mo |
| Shared 200 GB | 200 GB SSD | 5 TB | $15.59/mo |
| Dedicated server | RAM | Storage | Price |
| --- | --- | --- | --- |
| Intel Xeon E3-1240 v3 | 32 GB | 1 TB SSD + 3 TB HDD | $64.95/mo |
| AMD Ryzen 5 7600 | 64 GB | 1 TB NVMe | $109.95/mo |
| Dual Xeon E5-2683 v4 | 256 GB | 2 × 2 TB SSD | $209.00/mo |

One warning on the dedicated line: the specials list and the main dedicated-servers page don't quote the same entry price. A later check of the dedicated page showed an older Xeon E3-1230 v2 at $139/mo, well above the $64.95 figure the specials list carries. Treat any "from $X" number on this product line as a snapshot and confirm on the live config page.

## The recurring codes, and the rule the comparison posts skip

| Code | Discount | Applies to |
| --- | --- | --- |
| `INTENSEINVESTOR` | 30% recurring, for life | KVM VPS and NVMe Windows VPS |
| `DRWOOKIEE` | 30% recurring, for life | All RackNerd VPS plans |
| `WIN-30OFF` | 30% recurring, for life | Windows VPS |
| `MYPHPNOTES` | 30% recurring | All VPS plans |
| `15OFFDEDI` | 15% recurring, for life | Dedicated servers |
| `15OFFRESELLER` | 15% recurring | Reseller hosting |

Two things about these codes get lost in most write-ups. First, **one code per order**, so you pick the single best one for what's in your cart. Second, **recurring** means the discount repeats on every renewal, not just the first invoice, and it applies on top of the already-discounted annual price rather than replacing it. Run the arithmetic and 30% off turns the $11.29 plan into roughly **$7.90/year**, the $32.49 plan into about **$22.74/year**, and the $59.99 plan into about **$41.99/year**, held for as long as you keep the server.

These codes were compiled in early 2026. Availability shifts with whatever promotion is running, so type the code into the cart and watch the total change before you pay. 👉 [Open RackNerd's order page and test a code in the cart](https://bit.ly/RacKnerd)

## Where RackNerd will actually annoy you

Every special is a **shared CPU** plan. Neighbours matter, and third-party testing has caught that variance (more on the grades below). If your workload needs guaranteed cores, that's a dedicated server, not a $32 VPS.

Base plans ship with **no snapshots and no automated backups**. RackNerd's VPS specials page now describes *ctrl* as the bundled panel, covering reboot, OS reinstall, an HTML5 VNC console, one-click apps, inbound firewall rules, root password reset and upgrades; older plan listings and several third-party comparisons still name SolusVM. Whichever panel your node lands on, the gap is the same: you build the backup yourself. A nightly `rsync` or `rclone` push to object storage elsewhere costs a couple of dollars a month and is the difference between a bad afternoon and a dead project.

Support is **ticket-based** and consistently described as fast, with third-party notes putting average first response somewhere under 30 minutes and community reports claiming under 10. Fast tickets are still not live chat at 3am.

Shared-node **IP reputation** is worth checking before you run a mail server. If the address you get has history, you inherit it.

Dedicated servers are **provisioned manually, 24 to 72 hours** after ordering. If you need a box tonight, that's a VPS.

## What CloudCone gives you for the extra $5.70

CloudCone runs three US locations: Los Angeles, St. Louis (Missouri, opened September 2025) and Reston, Virginia (October 2025). Same KVM virtualisation, but a custom panel with snapshots, firewall rules, API access, and hourly billing. That panel is the actual product difference here.

The price confusion around CloudCone is worth untangling, because it's why you'll see four different "entry prices" for the same company. In January 2026 it ran a Hashtag sale with lifetime pricing: the SSD entry plan at **$16.99/year** for 2 cores, 1GB RAM, 20GB RAID-10 and 3TB of transfer, with a 2GB tier around $24/year. Separately, the standard SSD line on its site works out to about **$28/year** for 1GB ($2.33/mo billed annually) and **$46/year** for 2GB with 4 vCores. Other listings quote $10.24, $14.99 or $23.50 for entry configurations. Those are different promotions and different billing terms, not contradictions. Compare the plan specs, not the headline.

The SC2 line is the interesting one: configurable cores, RAM, disk and IPv4 count, starting at **$0.00699/hour**, with automatic backups, snapshots, a one-click app library and priority support included, and a $31.25/year SC2-1 plan at 3 cores / 2GB / 60GB RAID-10. One billing detail that surprises people: hourly metering settles monthly, and you need balance roughly equal to a month's charge before an instance will deploy. Destroyed instances bill for hours used. Backups, snapshots and optional resources bill separately.

Two more things to know before comparing. Backups are **SC2-only**; the cheap SSD plans don't include them, so CloudCone's "we have backups" claim doesn't apply to the $16.99 box. And refund terms are murky across sources: one set says 7 days on SC2, another says the policy tightened to no refunds in June 2025. Check the checkout page rather than trusting either.

## RackNerd vs CloudCone at a glance

|  | RackNerd | CloudCone |
| --- | --- | --- |
| Entry annual price | $11.29/yr (New Year 2026) | $16.99/yr (Hashtag 2026); ~$28/yr standard line |
| Locations | 21 data centers, 20 cities, incl. Singapore and Europe | 3 US (Los Angeles, St. Louis, Reston) |
| Panel | ctrl / SolusVM; firewall rules, VNC, one-click apps | Custom; snapshots, firewall, API |
| Snapshots & auto backups | Not on base plans | SC2 tier only |
| Billing | Annual promo plans | Annual, monthly, hourly (SC2) |
| Custom configs | No, fixed plans | Yes, on SC2 |
| Renewal pricing | Locked on annual promos | Stated as locked at deploy |
| Support | 24/7 tickets, reported under 30 min | 24/7 tickets, reported 12 to 24 hours |

Both claim lifetime price locks on their promotional plans, and long-term users of both report renewals that didn't jump. That's the real reason these two get compared at all; the big clouds will happily double your bill at renewal.

## Performance: the third-party data is thinner than it looks

VPSBenchmarks tested one RackNerd plan, a Ryzen 2 vCore / 4GB machine at $24.59/month, on 11 December 2025. Grades: **Web B, raw CPU D, performance stability D, disk IO C, network E**, with provisioning at 110 seconds. That's a single sample, and the plan tested is a monthly-billed Ryzen instance, not the annual specials in the table above, so don't read those letters as a verdict on the $11.29 box. The same site has **no usable test data for CloudCone at all**, which means no apples-to-apples comparison exists there.

A March 2026 comparison on vpsrankings reaches harsher conclusions from its own testing: noticeable Geekbench swings on the same RackNerd machine at different times (a classic overselling signature), some nodes still on standard SSD at 100–200MB/s versus NVMe on most CloudCone nodes measuring two to three times faster, higher packet loss on RackNerd during evening peaks, uptime around 95–99% against roughly 99.9% for CloudCone. Other write-ups describe RackNerd's 2026 infrastructure as stable with no major incidents.

Those two pictures don't reconcile, and I'm not going to pretend they do. Different authors, different nodes, no shared methodology. What's safe to say: the disk and CPU gap is the plausible one, because CloudCone's newer Missouri hardware is NVMe and RackNerd's cheapest tiers are not guaranteed to be. For a static site or a proxy, it won't matter. For WordPress with plugins and a database, it shows up on page loads.

## Asia, China, and the CN2 question

RackNerd's marketing describes its Los Angeles and Singapore locations as having Asia-facing routing blends including China Telecom, CN2 and China Unicom. Third-party testing says neither provider is on genuinely CN2-optimised routes, with mainland latency in the 150–200ms range and mediocre evening performance.

Both things can be true if "blend" means some China-bound traffic takes a better path some of the time. If mainland China is your primary audience, test before you buy rather than trusting either claim. CloudCone publishes test addresses for exactly this (66.154.118.2 in Missouri, 148.135.114.75 in Los Angeles); RackNerd runs public looking-glass tools across its locations so you can check routing from your own connection.

## The January 2026 CloudCone Los Angeles incident

In late January 2026, CloudCone's Los Angeles DC1 was hit by a ransomware-style attack that exploited a vulnerability in a third-party virtualisation platform. Missouri and Virginia were unaffected. The response was unusually documented: all API keys and credentials rotated, IP-level access controls hardened, the deployment gateway rebuilt from a clean environment, migration to an in-house virtualisation platform started, affected customers given a month of credit plus two free months on upcoming renewals, and backups discounted 50% for up to a year.

That's the right way to handle it. It's also a reminder that "the provider has backups" is not your disaster plan. Keep your own copy off the server, on either platform.

## Which one to buy

- **Learning Linux, a proxy node, a cron-job box, a staging server:** RackNerd 1GB at $11.29/year. Nothing else in this price bracket comes close, and a 30% recurring code takes it under $8/year.
- **One WordPress site or a small side project:** RackNerd 3.5GB at $32.49/year. Two cores and 65GB of SSD is the point where a LEMP stack stops swapping.
- **Anything where an outage costs money:** CloudCone SC2. Snapshots, automatic backups and hourly scaling are worth the premium when a dead server means lost orders, and the $31.25/year SC2-1 is the cheapest way in.
- **You want a server in Asia or Europe:** RackNerd, since CloudCone is US-only.
- **You want to resize up for a launch week and back down:** CloudCone SC2, hourly. RackNerd's specials are fixed annual plans.
- **You want more cores per dollar at 2GB:** CloudCone's standard line gives 4 vCores and 60GB for $46/year against RackNerd's single vCore at $18.29. Different trade: more money, more parallelism.
- **You need Windows:** both offer it; RackNerd has dedicated Windows codes, and licensing terms are worth reading on either side.

## Before you pay

Confirm four things at checkout, in this order: the **renewal price** shown for year two, whether your **coupon applied to the recurring total** rather than a one-time discount, the **refund terms** for the specific plan (neither provider publishes a policy generous enough to rely on), and the **data center** you selected, because that's the setting you can't change cheaply later.

Then pick the smallest plan that fits the job. Most people reading a comparison like this one end up on the 3.5GB tier and never touch the extra capacity, which is fine, and a fair number would have been equally happy on the $11.29 box.

👉 [Start with RackNerd's 3.5GB plan at $32.49/year, or drop to the $11.29 entry box](https://bit.ly/RacKnerd)
