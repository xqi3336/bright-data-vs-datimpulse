# Bright Data Review: What You Actually Pay Per GB, Who It Fits, and When a $1/GB Alternative Wins

Most people typing this search already know the name. What they don't know is the number.

Bright Data publishes a headline price on its navigation bar, a different set of numbers on the product page, and a third set of rules in the billing FAQ that decide what actually leaves your bank account. If you're a developer or a small team trying to budget a scraping project, that gap is the whole review. So let's start there.

## What you're reviewing, exactly

Bright Data isn't one product, and that trips people up. The catalogue splits into four proxy networks (residential, datacenter, ISP, mobile) plus a stack of managed tools: Web Unlocker, SERP API, Crawl API, Browser API, pre-built scrapers for sites like Amazon and LinkedIn, a dataset marketplace, and a free MCP tier for AI agents.

Scale is the company's actual selling point. It advertises 400M+ monthly residential IPs across 195 countries, roughly 0.7-second response times, a 99.95% success rate, free geo-targeting down to state, city, ZIP and ASN, and unlimited concurrent sessions. It's an Israeli company, complies with GDPR and CCPA, and holds ISO 27001, SOC 2 and SOC 3 certifications.

If your project needs raw proxy bandwidth and nothing else, most of that catalogue is irrelevant to you. That matters, because the pricing you care about is the pricing on two or three pages, not the whole menu.

## The price on the menu is not the price on the card

Three of Bright Data's headline prices don't appear anywhere on the pages they link to.

- **Residential.** The nav says "from $2.50/GB." The residential page's own plan cards say **$8/GB pay-as-you-go**, and $4/GB with coupon code RESIGB50. The $2.50 figure is the $1,999/month tier with that coupon applied, which works out around $2.51/GB.
- **Datacenter.** The nav says "from $0.90/IP." That's the 1,000-IP shared tier at $900/month. Ten shared IPs cost $1.40 each.
- **Web Unlocker.** The nav says "from $1 per 1,000 requests." The page itself lists $1.50 pay-as-you-go, with $1.30 as the overage rate on the $499 plan.

This is standard practice in the proxy market, and Bright Data isn't hiding it. But it does mean you should budget from the plan card that matches your volume, not from the headline.

Here's what the cards actually say across the main products.

| Product | Pay-as-you-go | Monthly tiers |
| --- | --- | --- |
| Residential | $8/GB | $499/mo for 141 GB ($3.50/GB), $999/mo for 332 GB ($3.00/GB), $1,999/mo for 798 GB ($2.50/GB) |
| Datacenter (shared, per IP) | $1.40/IP | $14/mo for 10 IPs, $100 for 100, $475 for 500, $900 for 1,000 |
| Datacenter (dedicated, per IP) | — | $22/mo for 10 IPs, $170 for 100, $750 for 500, $1,300 for 1,000 |
| Datacenter (per GB) | $0.60/GB | $0.51/GB at 1 TB ($499), $0.45/GB at 2 TB ($999), $0.42/GB at 5 TB ($1,999) |
| ISP | $1.80/IP | $18/mo for 10 IPs, $145 for 100, $700 for 500, $1,300 for 1,000 |
| Mobile | from ~$8.40/GB | Volume tiers available; KYC required |
| Web Unlocker | $1.50 per 1,000 requests | Free tier of 5,000 requests/month, then $499/mo for 383,000 requests with $1.30/1,000 overage |
| MCP server | — | Free tier of 5,000 requests/month |

Two discounts are worth knowing. The RESIGB50 coupon halves residential rates for three months, so a $499 plan lands near $3.54/GB in that window. And new accounts get their first deposit matched dollar for dollar up to $500.

Rates change; check the current cards before you commit.

## The billing rules decide your real cost

The proxy pricing FAQ is long, and it's where the unpleasant surprises live.

**Unused commitment doesn't roll over.** Commitments are charged on the 1st. If you're on a $499 plan and use 60 GB that month, the other 81 GB don't follow you into next month.

**Bandwidth is counted in both directions.** Request headers, request bodies, response headers and response bodies all count. A scraper that pulls uncompressed HTML, or retries a lot, pays for all of it.

**Residential and mobile require KYC.** A representative may ask for a short video call plus company or personal verification before those networks are switched on. Web Unlocker doesn't require it, which is one reason Bright Data itself points scraping buyers toward it.

**No documented refund policy.** None of the pricing pages describe one. Oxylabs, by comparison, refunds self-service plans within three days if you've used less than 20%.

**Fine geo-targeting costs extra.** Targeting a specific city or ZIP reportedly adds a 20–40% multiplier to the per-GB rate.

For a one-off project, pay-as-you-go avoids most of this. For a team that scopes a plan badly in month one, it doesn't.

## What independent testing and reviews say

PCMag's hands-on testing rates Bright Data as a strong choice for enterprise buyers and flags above-average prices as the trade-off. The same review notes support is aimed squarely at enterprise clients: email and documentation Monday to Friday, with any premium SLA behind a sales conversation. Rivals offer live chat at lower tiers.

Critical reviews PCMag cites cluster around three things: frustration with the refund policy, inconsistent quality on ISP and residential IPs, and bugs in the proxy manager. Bright Data's support director responded directly to at least one complaint and offered to arrange a call, which is a reasonable sign.

One criticism is worth repeating because it has nothing to do with scraping: PCMag found Bright Data collects a notable amount of customer information, including details harvested from public sources rather than provided by the customer. It's disclosed in the privacy policy and it's compliant, but it's more collection than comparable enterprise providers.

One cost-analysis simulation puts Bright Data at about $8.40/GB for a 10 GB residential purchase, dropping to roughly $3.30/GB at 10 TB. That's the shape of the whole business: expensive at the entrance, competitive at depth.

## Who the price actually makes sense for

Bright Data earns its premium in a few specific situations.

You're pulling serious volume. Below a terabyte a month, you're paying a premium for infrastructure capacity you're not using. Past that, per-GB rates fall to levels most budget providers can't match.

Your targets fight back. If you're scraping SERPs, marketplaces or social platforms with serious anti-bot defenses, the 400M-IP pool and fingerprinting stack are the reason the bill is high. Cheap proxy bandwidth that gets blocked on 40% of requests isn't cheaper.

You need the managed layer. Web Unlocker's free 5,000 requests a month is a genuinely useful way to test whether Bright Data's infrastructure clears a target before you spend anything.

You have compliance requirements. Two decades of audits, SOC 2, ISO 27001 and a documented consent model for IP sourcing matter to enterprise procurement.

It fits badly if you're a solo developer testing an idea, if your monthly volume swings between 5 GB and 80 GB, if you want unused credits to survive a quiet month, or if you just want proxy credentials and zero account management.

That last group is large, and it's the group the budget end of the market built itself around.

## The other end of the market: DataImpulse

DataImpulse takes the opposite approach. Instead of tiered plans and volume commitments, it charges **$1 per GB** for residential proxies pay-as-you-go, with no subscription, and the traffic you buy never expires. Start at $5 for 5 GB, use it over six months if you want, and nothing is lost.

The network is smaller than Bright Data's: 90M+ ethically sourced IPs across 195 countries, with a published 99.51% success rate. You get HTTP/HTTPS and SOCKS5, rotating sessions (port 823 for HTTP, 824 for SOCKS5) and sticky sessions that hold an IP for 1 to 120 minutes, with country targeting included.

The catches are real, so here they are. Advanced targeting filters (state, city, ZIP, ASN) are billed at twice the standard rate on the standard residential plan. There's no managed scraping API at all, which means you write your own request handling, parsing, retries and CAPTCHA logic. DataImpulse's history is shorter than Bright Data's, and its IP pool is a fraction of the size.

What you get in return is the pricing model most small projects actually want.

| Plan | Rate | What you get | Billing |
| --- | --- | --- | --- |
| Residential | $1/GB | 90M+ IPs, 195 countries, country targeting included, HTTP/SOCKS5, non-expiring traffic | Pay-as-you-go, from $5 / 5 GB —  [start with the $5 intro pack](https://bit.ly/dataimPulse) |
| Residential, volume | $0.80/GB at 1 TB ($800), $0.70/GB at 5 TB | Same pool, bulk top-up | One-time payment, credits don't expire —  [check the bulk residential rates](https://bit.ly/dataimPulse) |
| Premium residential | $5/GB | Faster, lower-latency IPs, dedicated account manager, all targeting options included at no extra charge | Pay-as-you-go, from $5 / 1 GB or $50 / 10 GB —  [compare premium residential](https://bit.ly/dataimPulse) |
| Datacenter | $0.50/GB | 20M+ datacenter IPs, 195+ countries, sub-100ms response times, sticky sessions up to 30 minutes | Pay-as-you-go —  [see datacenter pricing](https://bit.ly/dataimPulse) |
| Mobile | $2/GB | 16M+ 3G/4G/5G/LTE IPs, sticky sessions up to 2 hours | Pay-as-you-go —  [view mobile proxy rates](https://bit.ly/dataimPulse) |

New users get a 7-day refund window, and support is 24/7 with actual humans. Ratings sit around 4.8/5 on G2 according to DataImpulse's own site, with an independent 2024 write-up recording a 4.6/5 Trustpilot average.

## Doing the math on a real workload

Take a common scenario: a two-person team scraping e-commerce pricing at 50 GB per month.

On Bright Data's pay-as-you-go rate, that's **$400/month**. On a residential plan, the smallest tier is $499 for 141 GB, which is more bandwidth than they need at a higher cost than pay-as-you-go. With the RESIGB50 coupon, $499 buys 141 GB at an effective $3.54/GB for three months, then reverts.

On DataImpulse, 50 GB is **$50**, and any unused portion from a top-up survives to the next month.

That's an eightfold difference, and it's not because one provider is being generous. Bright Data is selling a 400M-IP pool with KYC, SLAs, a managed unlocking layer and enterprise support. DataImpulse is selling bandwidth through a smaller, more self-service network. If your targets don't block residential IPs, the extra infrastructure doesn't do anything for you.

Now push the volume to 5 TB a month and the picture flips. Bright Data's per-GB rates fall toward $2–$3, its success rate on hard targets holds up, and the account management starts paying for itself. DataImpulse at $0.70/GB is still cheaper on paper, but you'd be running 5 TB through a 90M-IP pool with no managed unlocking layer behind it.

👉 [Test DataImpulse's $1/GB rate on your own targets](https://bit.ly/dataimPulse) — that's the only benchmark that counts for your specific workload.

## Which one should you actually use

Work through this in order.

1. **Under 100 GB a month with unpredictable usage?** DataImpulse. Non-expiring credits beat a commitment you might waste.
2. **Getting blocked on residential IPs with a cheap provider?** The problem is likely pool quality, not pool size. Premium residential at $5/GB is still below Bright Data's pay-as-you-go rate.
3. **Scraping hard targets at scale with a team behind it?** Bright Data. Web Unlocker's free 5,000 requests will tell you quickly whether its infrastructure clears your targets.
4. **Need structured data without writing a scraper?** Bright Data. DataImpulse doesn't offer a managed scraping API, and that's deliberate.
5. **Running datacenter workloads at low cost?** DataImpulse at $0.50/GB is hard to argue with for unprotected targets. Bright Data's per-GB datacenter ladder only beats it past 1 TB.
6. **Procurement needs SOC 2, ISO 27001 and audit trails?** Bright Data. That paperwork is part of what the premium pays for.

The honest summary: Bright Data is expensive at the entry point and earns it at scale, and its pricing pages require more reading than most buyers expect. DataImpulse does one thing at $1/GB, does it without commitments, and asks you to bring your own code.

## FAQ

**Does Bright Data have a free plan?**
Not for proxies. Web Unlocker, SERP API, Scraper APIs and the MCP server each list a free tier, with Web Unlocker and MCP specifying 5,000 requests a month with no credit card. Proxy networks start with trial credit and a first-deposit match up to $500.

**Is Bright Data worth the price?**
At high volume or on heavily defended targets, it can be. At entry volume, you're paying for capacity you won't use. Run a small batch through pay-as-you-go before committing to $499 a month, because unused commitment doesn't carry over.

**How long does the RESIGB50 coupon last?**
Three months on residential rates. Budget the reversion to full price in month four rather than treating the discounted rate as your ongoing cost.

**Which is cheaper, Bright Data or DataImpulse?**
For residential proxies at any volume below roughly a terabyte, DataImpulse at $1/GB pay-as-you-go is substantially cheaper, and unused traffic doesn't expire. Bright Data closes the gap as volume rises and pulls ahead on pool size, managed tooling and hard-target success rates.
