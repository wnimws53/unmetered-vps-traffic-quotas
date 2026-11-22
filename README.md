# Unmetered VPS: Is the Traffic Really Unlimited, What Port Speed Do You Get, and Which Plan Is Enough? (Port Speeds, Regional Quotas, Full Plan Table)

"Unmetered" on a VPS listing means the provider doesn't count or bill the gigabytes you push. It says nothing about how fast those gigabytes move: every plan still sits behind a port with a fixed rate, and a few regions add a monthly quota on top. OVHcloud's unmetered line runs on ports from 250 Mbps to 2 Gbps depending on the plan, and its Mumbai, Singapore and Sydney locations carry quotas of 1 TB to 4 TB before traffic gets throttled to 10 Mbps.

Below: AVA Hosting's current VPS range (1 Gbps ports from €5.00/month), what port and guarantee numbers look like at three other providers, and which box fits a proxy node, a file server, or a handful of small sites.

> **Quick pick.** VPS One at **€5.00/month** covers most readers: 1 vCPU, 2 GB ECC RAM, 25 GB NVMe, a 1 Gbps port and unlimited bandwidth. Move up to VPS Basic at €10.00/month when several sites or a database share the machine. 👉 [Check the VPS One configuration and current price](https://my.ava.hosting/aff.php?aff=15562)

## All AVA Hosting VPS plans

Seven plans are listed on the VPS store page. Every one includes free DDoS protection, weekly backups, full root access, a control panel, a 99.9% uptime SLA and 24/7 support, running on Intel Xeon E5 hardware with NVMe storage.

| Plan | vCPU / RAM / NVMe | Port and traffic | Price | Order |
| --- | --- | --- | --- | --- |
| VPS Nano | 1 / 512 MB ECC / 20 GB | 100 Mbps, unlimited bandwidth | €11.00 / year | [ Order VPS Nano](https://my.ava.hosting/aff.php?aff=15562) |
| VPS One | 1 / 2 GB ECC / 25 GB | 1 Gbps, unlimited bandwidth | €5.00 / month | [ Order VPS One](https://my.ava.hosting/aff.php?aff=15562) |
| VPS Basic | 2 / 4 GB ECC / 50 GB | 1 Gbps, unlimited bandwidth | €10.00 / month | [ Order VPS Basic](https://my.ava.hosting/aff.php?aff=15562) |
| VPS Lucky | 2 / 6 GB ECC / 70 GB | 1 Gbps, unlimited bandwidth | €15.00 / month | [ Order VPS Lucky](https://my.ava.hosting/aff.php?aff=15562) |
| VPS Power | 4 / 8 GB ECC / 90 GB | 1 Gbps, unlimited bandwidth | €20.00 / month | [ Order VPS Power](https://my.ava.hosting/aff.php?aff=15562) |
| VPS Extra | 6 / 12 GB ECC / 120 GB | 1 Gbps, unlimited bandwidth | €30.00 / month | [ Order VPS Extra](https://my.ava.hosting/aff.php?aff=15562) |
| VPS Ultra | 8 / 16 GB ECC / 160 GB | 1 Gbps, unlimited bandwidth | €40.00 / month | [ Order VPS Ultra](https://my.ava.hosting/aff.php?aff=15562) |

Two details deserve a flag. VPS Nano lists **port 25 as closed** and showed **0 available** at the time of checking, so the €11.00/year box is an annual-billing, 100 Mbps machine that may not be in stock. The order page for VPS One also offers a smaller entry configuration at **€2.00/month** (1 vCPU, 1 GB RAM, 15 GB NVMe) and quotes slightly different storage on some upper tiers, so confirm the spec on the checkout screen instead of assuming the store listing carries over exactly.

## What an unmetered plan actually limits

Three things decide what you feel in practice: the port rate, the guaranteed rate, and any regional quota or acceptable-use rule attached to the plan.

OVHcloud spells out the first. Traffic on an unmetered VPS is not measured and not billed, and the maximum connection speed is set by the plan, from 250 Mbps to 2 Gbps. A footnote on the same page adds quotas for Asia-Pacific: VPS-1 and VPS-2 get 1 TB per month, VPS-3 and VPS-4 get 3 TB, VPS-5 and VPS-6 get 4 TB, and past that the connection drops to 10 Mbps. Switching from a metered OVHcloud plan to unmetered costs the prorated difference for the remainder of the billing period.

VerticHost publishes its port range as 100 Mbps to 1 Gbps, varying with the location of the VPS, with unlimited traffic on every plan.

ZetServers approaches it from the other end: all VPS sit on a **25 Gbps unmetered port** with a guaranteed rate of **1 to 8 Gbps** depending on the plan, no traffic caps, no overage billing and no throttling, on nodes uplinked with 100 Gbps fiber ports.

AVA Hosting belongs to the first group. The store page states a 1 Gbps port and unlimited bandwidth on every monthly plan, with no separate guaranteed-rate figure printed next to it. If you intend to keep the port saturated for hours at a time, that's a question for support before ordering rather than something to assume from the word "unlimited".

## How the four options compare at the entry level

| Provider | What "unmetered" means here | Cheapest verified price | Port or guarantee |
| --- | --- | --- | --- |
| AVA Hosting | Unlimited bandwidth stated per plan | €5.00/mo | 1 Gbps (100 Mbps on VPS Nano) |
| VerticHost | Unlimited traffic on every plan | €19.00/mo | 100 Mbps to 1 Gbps by location |
| ZetServers | 25 Gbps unmetered port | €29.00/mo | 1 to 8 Gbps guaranteed |
| LightNode | Labelled unmetered, 1 to 4 TB per plan | $7.71/mo | Not stated |
| OVHcloud | Traffic not metered or billed | Not shown on the plan page | 250 Mbps to 2 Gbps by plan |

LightNode's page is the clearest case of why the wording deserves a second look. The heading and body copy promise "no bandwidth limitations", while each plan card carries a hard allowance: 1 TB on Start, 2 TB on Agency, 3 TB on Premium, 4 TB on Enterprise. The same page also quotes two prices, **$7.71/month** on the cards and "around $9.50" in the pricing section, with a $0.015/hour rate in between. Treat the allowance as the real limit and the card price as the working number.

## Which plan for which job

**Proxy and VPN exit nodes.** These are light on CPU and RAM and heavy on sustained throughput, so the port rate is the spec that matters. VPS One at €5.00/month gives you 1 Gbps and 2 GB of RAM, which is enough for a single exit node or a small fleet of tunnels. Location matters more than core count here, and AVA's store pages don't state where its VPS are hosted, so ask before you buy if latency to a specific country decides the purchase. ZetServers markets the same use case with dedicated vCPU cores and 1 to 8 Gbps guaranteed across eight European cities, at €29.00/month and up.

**File transfer, mirrors and video.** Storage per euro is roughly flat across AVA's range: 25 GB for €5.00 works out to €0.20 per GB, and 160 GB for €40.00 to €0.25 per GB. Paying more buys CPU and RAM rather than cheaper disk, so pick by the storage you actually need today: 90 GB at €20.00/month (VPS Power) is the sensible step up from Basic, and VPS Extra at €30.00/month adds 120 GB if you're pushing media out regularly.

**Small sites, APIs and bots.** VPS Basic at €10.00/month (2 vCPU, 4 GB) is the first plan with room for a web server, a database and a build process on the same box. One vCPU and 2 GB on VPS One will run a static site or a single low-traffic app, and it will struggle the moment a compile or a backup job runs alongside it. 👉 [Compare the VPS Basic and VPS One specs side by side](https://my.ava.hosting/aff.php?aff=15562)

**Outbound mail.** VPS Nano is documented as having port 25 closed. If sending mail is part of the plan, confirm the policy on whichever tier you choose before migrating a mail server.

**Anything above 8 vCPU.** VPS Ultra is the top of the line at 8 vCPU and 16 GB. Past that, the conversation moves to dedicated hardware.

## Billing period, renewals and the annual trap

AVA's monthly plans run €60.00 to €480.00 per year if you stay on them. VPS Nano is the only annual-billed listing at €11.00/year, and it comes with a 100 Mbps port, 512 MB of RAM and a closed port 25. That combination suits a DNS node, a monitoring probe or a jump host, and very little else.

Annual billing as a category tends to buy the smallest possible box. Space Hosting's listing showed **$23.99/year** for 1 core, 1 GB DDR5 and 25 GB NVMe, on a page dated September 2023, so treat the number as historical rather than current. The lesson carries over: divide the annual figure by twelve and compare it against the monthly plan you'd otherwise pick, because a cheap year on an undersized box costs more in migration time than it saves.

Renewal pricing is the other half of that calculation, and AVA's plan cards show starting prices without a renewal figure. VerticHost states its position plainly, with renewal at the same price, no setup fees and no contracts, which is a fair standard to hold any provider to. Ask the same two questions before committing to an annual plan anywhere: what does year two cost, and what's the refund window. AVA's VPS One order page carries a Free Trial tag, so it's worth asking support what that covers and for how long.

## Before you order, and after the server boots

Five checks, in order:

1. Confirm the port rate on the specific plan. VPS Nano is 100 Mbps; everything else on AVA's list is 1 Gbps.
2. Ask which data centre you'll land in. It isn't stated on the VPS store page, and it decides latency for proxy and VPN use.
3. Ask what the acceptable-use policy says about sustained saturation, public torrent traffic and proxy use. Unlimited traffic still comes with rules at every provider.
4. Ask for the renewal price and the refund window in writing.
5. Test throughput properly once the box is live. ZetServers makes the point that speedtest.net endpoints usually cap below 1 Gbps and will under-report a fast link, and recommends iperf3 instead: `iperf3 -c ping.online.net -p 5201 -P 30`. Run it before you migrate anything.

Choosing, then: one app or one tunnel, buy VPS One at €5.00/month. Several sites or a database, VPS Basic at €10.00/month. Storage-led work, VPS Power at €20.00/month. Need a multi-gigabit guaranteed rate rather than a shared 1 Gbps port, and the budget is €29.00/month or more, then a specialist like ZetServers is the honest answer. Everything else in AVA's line is a step you take when a specific resource runs out. 👉 [Start with AVA Hosting's VPS list and pick the plan that matches](https://my.ava.hosting/aff.php?aff=15562)
