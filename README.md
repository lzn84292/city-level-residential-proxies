# rank tracking proxies: Pick City-Level Residential IPs, Wire Them Into Ahrefs or Semrush, and Stop Burning Bandwidth on CAPTCHAs

Your rank tracker reports position 4. Your client opens Google in an office two miles away and sees position 9. Neither number is fake. The tool queried from a datacenter IP in Virginia; the client searched from a real home connection in a specific suburb, with local intent signals attached. Local packs, map results, and even plain organic rankings shift by city, and sometimes by neighbourhood.

That gap is the whole reason rank tracking proxies exist. Not for anonymity or "bypassing restrictions" in the vague marketing sense, but because a rank check is only worth the money if the IP you query from looks like the searcher your client actually cares about. Everything else follows from that.

This piece is about the practical side of picking and running those IPs: what breaks rank checks, how bandwidth adds up, what rotation mode suits which tool, and where 9Proxy's current packages sit in that picture.

## What actually breaks a rank tracking run

Google's traffic checks work on three layers, and proxies only solve one and a half of them.

**IP reputation comes first.** Before your request is even parsed, the source address gets classified. Residential ISP ranges carry more trust because abuse from home connections is rarer. Datacenter ranges from AWS, DigitalOcean, or budget VPS hosts get treated as suspect by default. This is why the same scraper behaves completely differently from a home connection than from a cloud instance.

**Then request patterns.** Identical queries fired at machine speed from a single address is a signature, not a coincidence. Rate limits and CAPTCHAs follow.

**Then geography.** Results are localised. A US-wide check for "roof repair" is not the same query as "roof repair" from a specific ZIP code, and a rank tracker fed with country-level IPs will happily produce a number that matches nobody's actual SERP.

The third layer is the one most people under-buy for. Rotating residential IPs in bulk solve layer one and two reasonably well, but if your targeting stops at country level, you're still reporting a national average and calling it local SEO.

## The three IP types you'll be choosing between

| Proxy type | Looks like | Best for rank tracking | The catch |
| --- | --- | --- | --- |
| Rotating residential | Real home ISP users | Per-query rotation, wide geo spread, local pack checks | Pay per GB, and retries eat budget |
| Static ISP / static residential | Real ISP users on a fixed address | Long sessions, tools that keep cookies between checks | Usually priced per IP, monthly commitment |
| Datacenter | Servers | Fast, cheap, non-localised keyword checks | Detected quickly; results can diverge from real user SERPs |

Most rank tracking setups want residential IPs with city or ZIP-level targeting. Datacenter ranges are fine for internal sanity checks where you only care about whether a page is indexed and roughly where it sits. They are the wrong foundation for client-facing reports.

## The bandwidth maths nobody does before buying

SERP pages are lighter than people assume. A Google results page HTML-only runs around 320 KB. That sounds trivial until you multiply it.

- 100,000 rank checks ≈ **31 GB** of traffic
- 1,000 tracked keywords across 10 cities × 2 devices = 20,000 checks per run ≈ **6.4 GB** before retries
- Add retries, pagination to page 3, and the occasional re-fetch and you're realistically 20–40% higher

This is why the billing model matters more than the headline price. On a per-GB plan, every CAPTCHA page you accidentally fetch, every retry, every "let me just grab page two as well" costs money. On a per-IP plan with unlimited bandwidth, the cost is fixed and the question becomes how many clean IPs you can keep rotating.

There's no universal formula for "one proxy per X keywords." Timing patterns, browser behaviour, request regularity, and target geography all feed into whether a search engine starts pushing back. A test using your own keyword set, your own schedule, and your own tool beats any ratio from a sales page.

## Sticky or rotating? Match the mode to your tool, not the other way round

Rank trackers generally want a **fresh IP per query** or per small batch, so no single address accumulates enough queries to look automated. That maps to rotating residential.

There is one case for sticky. If your check needs to accept a consent banner, keep a session cookie, or behave like a returning visitor for a personalised-results comparison, a sticky session that survives 10–30 minutes is more useful than a new IP every request. Beyond that, rotation wins.

9Proxy splits this fairly cleanly:

- **Residential by IP** gives you fixed addresses with unlimited bandwidth. IPs last from a few hours up to about 24 hours naturally, and you can attach an auto-rotation proxy on selected ports to swap them on a timer. Setup runs through the desktop app with local port forwarding.
- **Residential by GB** rotates automatically per request or holds a sticky session for a configurable window. Everything happens in the dashboard, no app involved, and you can generate unlimited endpoints while only the consumed bandwidth is deducted.

For a headless rank tracking box in a cloud environment, the GB route is the simpler one to wire up. You authenticate with username/password or by whitelisting your server IP, generate endpoints, and export them as `.txt` or `.csv` with ready-made code samples for a handful of languages.

👉 [Compare the IP-based and GB-based plans on 9Proxy](https://bit.ly/9-Proxy)

## Where 9Proxy fits

Two things decide whether a provider is usable for rank tracking: targeting depth and cost structure. 9Proxy covers country, state, city, ZIP code, and ISP targeting across 20M+ residential IPs in 90+ locations, over HTTP and SOCKS5. ISP targeting is the less common one, and it's useful when you want the IP to look like it comes from a specific consumer broadband provider rather than just a generic residential range.

The company advertises 99.95% uptime, and independent comparisons put its residential success rate and response times in the region of 99.5% and 0.6 seconds average — respectable for the price bracket, not class-leading.

Pricing note: 9Proxy raised IP-based and bundle prices on June 1, 2026, the first increase in its history. GB-based prices were left untouched. Everything below reflects the current published structure.

| Plan | What you get | Price | Billing model | Purchase |
| --- | --- | --- | --- | --- |
| 100 IPs | 100 residential IPs, unlimited bandwidth | $24 ($0.24/IP) | One-time, IPs never expire | [Get the 100-IP entry package](https://bit.ly/9-Proxy) |
| 500 IPs | 500 residential IPs, unlimited bandwidth | $72 ($0.144/IP) | One-time, IPs never expire | [See the 500-IP package](https://bit.ly/9-Proxy) |
| 1,000 + 500 IPs | 1,500 residential IPs total, unlimited bandwidth | $126 ($0.084/IP) | One-time, IPs never expire | [Check the 1,000 + 500 bonus IP deal](https://bit.ly/9-Proxy) |
| 2,500 IPs | 2,500 residential IPs, unlimited bandwidth | $210 ($0.084/IP) | One-time, IPs never expire | [View the 2,500-IP package](https://bit.ly/9-Proxy) |
| 5,000 IPs | 5,000 residential IPs, unlimited bandwidth | $360 ($0.072/IP) | One-time, IPs never expire | [See the 5,000-IP agency package](https://bit.ly/9-Proxy) |
| 15,000 IPs | 15,000 residential IPs, unlimited bandwidth | $720 ($0.048/IP) | One-time, IPs never expire | [Check the 15,000-IP tier](https://bit.ly/9-Proxy) |
| 25,000 IPs | 25,000 residential IPs, unlimited bandwidth | $863 ($0.035/IP) | One-time, IPs never expire | [View the 25,000-IP tier](https://bit.ly/9-Proxy) |
| 50,000 IPs | 50,000 residential IPs, unlimited bandwidth | $1,438 ($0.029/IP) | One-time, IPs never expire | [See the 50,000-IP tier](https://bit.ly/9-Proxy) |
| 100,000 IPs | Business package, unlimited bandwidth | $2,300 ($0.023/IP) | One-time, IPs never expire | [Check the 100,000-IP business plan](https://bit.ly/9-Proxy) |
| 200,000 IPs | Business package, unlimited bandwidth | $4,140 ($0.021/IP) | One-time, IPs never expire | [View the 200,000-IP business plan](https://bit.ly/9-Proxy) |
| 500,000 IPs | Business package, unlimited bandwidth | $8,625 ($0.018/IP) | One-time, IPs never expire | [See the 500,000-IP business plan](https://bit.ly/9-Proxy) |
| 5 GB | Bandwidth, unlimited endpoints | $15 ($3.00/GB) | One-time, 180-day validity | [Start with a 5 GB traffic pack](https://bit.ly/9-Proxy) |
| 50 + 5 GB | Bandwidth, unlimited endpoints | $105 ($2.10/GB) | One-time, 180-day validity | [Get the 50 + 5 GB pack](https://bit.ly/9-Proxy) |
| 100 GB | Bandwidth, unlimited endpoints | $150 ($1.50/GB) | One-time, 180-day validity | [See the 100 GB pack](https://bit.ly/9-Proxy) |
| 200 GB | Bandwidth, unlimited endpoints | $200 ($1.00/GB) | One-time, 180-day validity | [Check the 200 GB pack](https://bit.ly/9-Proxy) |
| 1,000 GB | Bandwidth, unlimited endpoints | $800 ($0.80/GB) | One-time, 180-day validity | [View the 1,000 GB pack](https://bit.ly/9-Proxy) |
| 2,000 GB | Bandwidth, unlimited endpoints | $1,500 ($0.75/GB) | One-time, 180-day validity | [See the 2,000 GB pack](https://bit.ly/9-Proxy) |
| 3,000 GB (Enterprise) | Bandwidth, team mode, unlimited validity | $2,160 ($0.72/GB) | One-time, no expiry | [Check Enterprise 3,000 GB](https://bit.ly/9-Proxy) |
| 6,000 GB (Enterprise) | Bandwidth, team mode, unlimited validity | $4,200 ($0.70/GB) | One-time, no expiry | [View Enterprise 6,000 GB](https://bit.ly/9-Proxy) |
| 10,000 GB (Enterprise) | Bandwidth, team mode, unlimited validity | $6,800 ($0.68/GB) | One-time, no expiry | [See Enterprise 10,000 GB](https://bit.ly/9-Proxy) |
| Starter Bundle | 100 IPs + 5 GB | $30 | One-time, 180-day traffic validity | [Grab the Starter bundle](https://bit.ly/9-Proxy) |
| Mid Bundle | 1,500 IPs + 50 GB | $180 | One-time, 180-day traffic validity | [Check the 1,500 IP + 50 GB bundle](https://bit.ly/9-Proxy) |
| Pro Bundle | 5,000 IPs + 500 GB | $720 | One-time, 180-day traffic validity | [Get the Pro bundle](https://bit.ly/9-Proxy) |

One structural detail worth understanding: 9Proxy sells balance, not subscriptions. IP packages don't expire once purchased, and GB traffic lasts 180 days (unlimited on Enterprise). There's no monthly renewal clock quietly draining a card.

## Which package actually fits a rank tracking workflow

The honest answer depends on two numbers: how many checks you run, and whether your checks are shallow or deep.

**You're probably a GB-based buyer if** you track a few hundred to a few thousand keywords, in a handful of markets, once or twice a week, and you don't store raw HTML. A 50 + 5 GB pack covers roughly 160,000 SERP fetches at 320 KB each, which is several months of weekly reporting for a normal agency client list.

**You're probably an IP-based buyer if** your runs are deep and messy. Desktop plus mobile variants, page-one through page-three depth, competitor tracking in the same pull, city-level targeting across dozens of markets, and a pipeline that saves raw HTML so it can be re-parsed without re-fetching. That's exactly the profile where metered bandwidth becomes a budgeting problem, and unlimited bandwidth per IP removes it. The 500-IP and 1,500-IP tiers are the realistic entry points here, not because of bandwidth, but because you want enough distinct addresses to keep per-IP query rates low.

**Bundles exist for one specific situation:** an agency that runs one client's rank tracking on sticky IPs and another's on rotating traffic, and doesn't want two separate purchases. The 180-day validity on the bundled traffic is the feature that makes this workable, since project-based usage is rarely smooth.

👉 [Pick a 9Proxy package sized to your keyword volume](https://bit.ly/9-Proxy)

## Setting it up without wasting an afternoon

1. **Decide IP or GB first.** It changes the authentication model, not just the price. IP-based plans run through the 9Proxy desktop app, which forwards ports locally; GB plans generate endpoints straight in the dashboard.
2. **Target properly.** In the proxy generator, pick country, state, city, ZIP, or ISP. If you're checking local pack visibility for a specific service area, ZIP or city targeting is the difference between a report and a guess.
3. **Choose the session mode.** Rotating for per-query checks, sticky for anything that needs to hold a session.
4. **Sort out authentication.** Username and password, or whitelist the IP your rank tracking server runs on. Team setups on Enterprise plans can create sub-users and allocate traffic per member.
5. **Test one endpoint before you scale.** Confirm which country the IP resolves to and whether a search query returns a normal page or a consent/CAPTCHA interstitial. One endpoint, one query, thirty seconds of work. Do it anyway.
6. **Export and wire it in.** The generator hands you `.txt` or `.csv` plus code samples. Ahrefs and Semrush both accept external proxies in their proxy fields, and Playwright, Puppeteer, Selenium, or a plain `requests` script take the endpoint directly.
7. **Store the raw SERP.** Re-parsing saved HTML is free. Re-fetching is not.

## Where 9Proxy is the wrong tool

Not every workflow needs this. Three cases where you should look elsewhere:

- **Mobile SERP accuracy.** There are no mobile or carrier-targeted proxies here. If your rank tracking needs to reflect what a phone on a mobile network sees, this isn't the provider for it.
- **Datacenter-cheap bulk indexing checks.** 9Proxy's product line is residential only, with datacenter proxies listed as forthcoming rather than available. If you just need cheap, fast, non-localised checks, you're paying residential prices for a job that doesn't need residential IPs.
- **Massive single-market runs at the lowest possible per-IP cost.** A 20M+ IP pool is large, but the biggest networks in the space advertise well over 100M. For most rank tracking workloads 20M is plenty; for enormous geo-distributed operations it's a ceiling worth knowing about.

The IP-based workflow also leans on a desktop app for Windows and Mac, which is fine for a workstation and less convenient for a Linux VPS. The GB system sidesteps that entirely.

## Questions people ask before buying

**Do rank trackers need residential proxies at all?** Not always. If you track a handful of non-localised keywords, a static ISP or even a datacenter IP may hold up. Residential becomes necessary once localisation, volume, or client-facing accuracy enters the picture.

**Will Google know I'm using proxies?** Individual residential IPs are hard to distinguish from real users. The pattern gives you away faster than the address does, which is why rotation and per-IP query pacing matter more than which provider you picked.

**Can I use 9Proxy with Ahrefs, Semrush, or Ranktracker?** Yes. HTTP/HTTPS and SOCKS5 are supported, which covers the proxy fields in all three. It also drops into antidetect browsers and standard automation stacks if you're running your own checker.

**Is there a trial?** 9Proxy offers a limited trial for new users, subject to availability. You need to say whether you want an IP-based or GB-based trial when you request it.

**What payment methods work?** Cards, bank cards, Alipay, Apple Pay, Google Pay, and crypto including USDT, BTC, ETH, LTC, and DOGE.

👉 [Create a 9Proxy account and check current availability](https://bit.ly/9-Proxy)

## The short version

Rank tracking proxies solve a specific problem: making your checks originate from something that looks like a real searcher in the market you're reporting on. Residential IPs with city and ZIP targeting do that. Datacenter IPs mostly don't, and country-level targeting only gets you halfway there.

On cost structure, the split is simple. Light, shallow, infrequent checking fits a GB plan — SERP pages are small and metered bandwidth is cheap when you don't retry much. Deep, messy, multi-city, HTML-storing pipelines fit a per-IP plan with unlimited bandwidth. 9Proxy's entry point of $24 for 100 IPs or $15 for 5 GB is low enough that testing both against your own keyword set costs less than an hour of arguing about it.
