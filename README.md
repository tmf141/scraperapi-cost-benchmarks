# Web Scraping API Comparison: Is ScraperAPI Worth $49 a Month, What Does a Page Really Cost, and When Should You Pick Something Else?

ScraperAPI starts at **$49/month for 100,000 credits**, which works out to $0.49 per 1,000 standard pages. On plain, unprotected HTML that is one of the cheapest entry points in the general-purpose unblocking category, and the onboarding is genuinely quick: one API key, official SDKs for Python, Node, Java, Ruby and PHP, and a request that works without configuring a proxy zone first.

The price stops being $0.49 per 1,000 pages the moment your targets need help. Bot-protection bypass adds 10 credits, JavaScript rendering adds 10, and premium proxies add another 10, so the same $49 buys roughly 4,700 hardened rendered pages instead of 100,000 plain ones. Third-party benchmarks put ScraperAPI's success rate on heavily protected sites somewhere between 60% and 69%, which is fine for a supplementary pipeline and uncomfortable as your only one.

This comparison covers the full plan ladder, the credit multipliers that decide your real bill, the benchmark numbers with the test conditions attached, and the specific cases where Bright Data, Zyte, Firecrawl or a cheaper option is the better purchase.

> **Quick verdict**
> - **Buy ScraperAPI** if you scrape public catalogues, search results, directories or lightly protected pages, and you want structured endpoints for Amazon, Walmart, eBay and Google without building parsers.
> - **Start with the 7-day trial** (5,000 credits, no card), then Hobby at $49/month if 100,000 credits covers your volume.
> - **Look elsewhere** if your target list is mostly Cloudflare or DataDome protected, if you need 1–3 second responses, or if your pipeline expects clean JSON out of the box.
>
> 👉 [See the current ScraperAPI plans, credit allowances and per-plan thread limits](https://www.scraperapi.com/pricing?fp_ref=coupons)

## Full plan comparison

ScraperAPI runs eight tiers. The headline number that changes between them is credits per month, but the differences that actually force an upgrade are concurrency, geotargeting scope and whether you can keep spending past your cap.

| Plan | Monthly | Annual (per month) | Credits/mo | Threads | Get it |
| --- | --- | --- | --- | --- | --- |
| Free | $0 | — | 1,000 | 5 | [ Compare the free tier](https://www.scraperapi.com/pricing?fp_ref=coupons) |
| Hobby | $49 | $44.10 | 100,000 | 20 | [ Start with Hobby](https://www.scraperapi.com/pricing?fp_ref=coupons) |
| Startup | $149 | $134.10 | 1,000,000 | 50 | [ See Startup pricing](https://www.scraperapi.com/pricing?fp_ref=coupons) |
| Business | $299 | $269.10 | 3,000,000 | 100 | [ Check Business allowances](https://www.scraperapi.com/pricing?fp_ref=coupons) |
| Scaling | $475 | $427.50 | 5,000,000 | 200 | [ View the Scaling plan](https://www.scraperapi.com/pricing?fp_ref=coupons) |
| Professional | $975 | $877.50 | 10,500,000 | 300 | [ Compare Professional](https://www.scraperapi.com/pricing?fp_ref=coupons) |
| Advanced | $1,975 | $1,777.50 | 21,500,000 | 500 | [ See Advanced limits](https://www.scraperapi.com/pricing?fp_ref=coupons) |
| Enterprise | Custom | Custom | 22,000,000+ | 500+ | [ Request Enterprise pricing](https://www.scraperapi.com/pricing?fp_ref=coupons) |

Annual billing saves exactly 10% on every self-serve tier. That is a smaller discount than most SaaS tools offer, and it comes with the usual catch: credits reset on each monthly renewal date and unused credits do not roll over, so prepaying a year does not buy you a year of credits you can bank.

Three limits are buried in the plan structure rather than the pricing table:

| Plan | Geotargeting | Analytics history | Pay-as-you-go | Support |
| --- | --- | --- | --- | --- |
| Hobby | US and EU only | 30 days | No | Standard |
| Startup | US and EU only | 30 days | No | Standard |
| Business | Global, country level | Unlimited | No | Standard |
| Scaling and above | Global, country level | Unlimited | Yes, up to a cap you set | Standard / priority |

The geotargeting split matters more than it looks. If your project needs requests routed through Brazil, Japan or Germany, Hobby and Startup cannot do it at any volume, and Business at $299 is the real entry price. The pay-as-you-go row matters just as much: on Hobby, Startup and Business, running out of credits returns HTTP 429 errors instead of an overage charge. Teams that expect a soft landing get a broken pipeline at 3 a.m. instead.

## What a credit actually costs per page

ScraperAPI prices per credit, not per page, and the multiplier depends on the target. This is the single biggest gap between the advertised entry price and the invoice.

| Request type | Credits | Cost at Hobby ($0.49/1K credits) |
| --- | --- | --- |
| Standard page | 1 | $0.49 per 1,000 pages |
| Amazon, Walmart, eBay | 5 | $2.45 per 1,000 pages |
| Bot-protection bypass (Cloudflare, DataDome, PerimeterX, Akamai) | +10 | $5.39 per 1,000 pages |
| JS rendering (`render=true`) | +10 | $5.39 per 1,000 pages |
| Premium proxies (`premium=true`) | +10 | $5.39 per 1,000 pages |
| Premium proxies + JS rendering | 25 | $12.25 per 1,000 pages |
| Google or Bing SERP | 25 | $12.25 per 1,000 pages |
| LinkedIn | 30 | $14.70 per 1,000 pages |
| Ultra premium + JS rendering | 75 | $36.75 per 1,000 pages |

Geotargeting, sessions, device type, output format and auto parsing add nothing to the credit count. The multipliers stack additively on top of the base cost, and the anti-bot surcharge is applied automatically when ScraperAPI activates bypass logic, not when you ask for it. A target that quietly starts challenging requests can double your bill without a code change.

Run the numbers on a realistic mixed workload and the gap widens. ScrapingTest's October 2026 review measured an effective cost of **$12.04 per 1,000 requests** across 16 priced sites. A Scrapeway benchmark from the same month landed at **$5.81 per 1,000** across 11 targets. Both figures sit far above the $0.49 headline because both mixes included domains that trigger multipliers. Neither number is wrong; they simply describe different target lists.

The per-credit rate does fall as you climb. At Scaling, $475 buys 5,000,000 credits, or about $0.095 per 1,000 credits. A protected page with rendering on costs 21 credits, which is roughly $10.29 per 1,000 pages on Hobby and about $2.00 per 1,000 on Scaling. If multipliers are what is eating your budget, moving up a tier beats buying more requests at the entry rate, because the per-request credit cost never changes with the plan.

ScraperAPI does give you tools to keep this under control. Every response carries a `sa-credit-cost` header showing what that request cost, the dashboard has a Domain Cost Estimator that prices a URL before you scrape it, and `max_cost` rejects a request that would exceed a limit you set. Test your ten hardest URLs through the estimator before you pick a tier; it will predict your bill better than any benchmark.

👉 [Price your own target URLs against the current ScraperAPI credit table](https://www.scraperapi.com/pricing?fp_ref=coupons)

## Success rates: four benchmarks, four different answers

No single number describes ScraperAPI's reliability, because success depends heavily on configuration and on which domains the tester chose. Here is what each published test found, with its conditions:

- **Scrape.do, 2026 benchmark** (16 APIs, 7 tough domains, a request counted only when it returned validated HTML): ScraperAPI at **68.95%**. For Cloudflare, DataDome or similarly hardened sites, that means roughly one in three requests fails.
- **Proxyway, 2025 report** (11 participants, 15 heavily protected sites): about **69%** on protected sites, with the note that it is cost-efficient on unprotected ones.
- **String benchmark**: **64%** at default settings, rising to **84%** once configured at its strongest setting. That 20-point swing is the most useful data point in this whole comparison, because it shows how much of the "success rate" conversation is really a configuration conversation.
- **Scrapeway, October 2026** (11 targets): **60%** overall, fifth of six APIs, with a 10.6 second average response and $5.81 per 1,000 requests.

Then there is the other side of the coin. ScrapingTest's October 2026 benchmark found ScraperAPI at **100%** on Amazon, Best Buy, LinkedIn and Idealista, and **93.3% on G2** against a 63.4% mean for the 15 APIs tested there. Amazon returning 100% at 5 credits per request is the strongest argument for ScraperAPI in this entire article: on retail and SERP targets with dedicated structured endpoints, it is competitive, and it is cheap.

The pattern is consistent once you line the tests up. ScraperAPI handles mainstream commercial domains well and struggles on the generic hardest-site list. If your targets look like Amazon, Walmart, Google, G2 or LinkedIn, the benchmarks are encouraging. If they look like the Cloudflare-fronted sites Proxyway and Scrape.do deliberately picked, plan for a third of your requests to fail and for retry logic to absorb the rest.

## Latency, including the rendering penalty

HasData's September 2026 test ran plain requests against sandbox pages and recorded a **median of 9.07 seconds**, a 75th percentile of 10.57 seconds and a **P95 of 12.57 seconds**. That is slow next to Zyte at 1.43s, ScrapingBee at 2.18s and Oxylabs at 2.72s in the same run. Scrapeway's independent October 2026 test measured 10.6 seconds average, which corroborates the ballpark.

The number that should shape your architecture is the rendering case. In HasData's fidelity check, with JavaScript rendering on, ScraperAPI's **median response took 29 seconds**. That is not a typo and not a worst case: it is the median for a JS-rendered page in that test.

A 29-second median changes what concurrency you need. Pulling 10,000 rendered pages in an hour at 20 threads is not achievable; you would need far more parallel capacity, which means a higher tier, which means the real cost of rendering is the plan upgrade plus the 10-credit multiplier plus the wall-clock time. Batch jobs that can run overnight are unaffected. Real-time enrichment inside a request path is a poor fit.

ScraperAPI does offer an Async API that accepts up to 50,000 URLs per batch and retries a job for up to 24 hours, which is the right way to use this service at volume. Sending rendered requests synchronously and waiting is the wrong way.

## Output format and the parsing work you inherit

The default response is raw HTML. You get the page and you write the parser. Structured JSON exists through dedicated endpoints for Amazon, Walmart, eBay and Google, and auto parsing can attempt JSON extraction from generic pages at no extra credit cost. Markdown and text output are also available without a credit surcharge.

For a classic data pipeline, raw HTML is fine and often preferable. For an LLM or RAG workflow, the output decision costs more than the success-rate decision. If you need clean, chunkable content and you are not building a parser, ScraperAPI hands you the page and leaves the extraction to you. Firecrawl's whole pitch is skipping that step with markdown output, and its own published figure claims 67% fewer tokens than raw HTML.

ScraperAPI does cover the AI-tooling side better than its documentation headlines suggest. ScrapingTest's October 2026 review documents a hosted MCP server, an agent plugin exposing 22 MCP tools and 19 skills, and LangChain and LlamaIndex integrations. If your pipeline is an agent that calls tools rather than a script that parses HTML, that changes the calculation.

## How ScraperAPI compares to the alternatives

Prices below come from each vendor's own materials or from published benchmarks, and several vendors publish more than one rate depending on target difficulty. Where sources disagree, both figures are shown.

| Tool | Best for | Starting price | Protected-site success (benchmark) | Output |
| --- | --- | --- | --- | --- |
| ScraperAPI | Budget scraping, retail and SERP endpoints | $49/mo for 100K credits | 60% (Scrapeway, 11 targets); 68.95% (Scrape.do, 7 domains) | Raw HTML, markdown/text, JSON on select domains |
| Bright Data | Highest success rate, largest proxy pool, enterprise compliance | $1.50 per 1K PAYG; other sources cite $0.75 or $1 per 1K | 98.87% (Scrape.do 2026, as cited by Bright Data) | Raw HTML |
| Zyte | The hardest sites, lowest median latency | $100/mo minimum commitment; $0.06–$0.61 per request | 93% (Proxyway 2025); 68% (String) | JSON and HTML |
| Firecrawl | LLM-ready markdown and schema JSON | $19/mo | 33.69% (Proxyway); 80% (String) | Markdown, schema-based JSON |
| ScrapingBee | Simplest onboarding, clean docs | $49/mo in one source, $29/mo in another | 73% (String); 84% dropping to 73% under load (Proxyway) | JSON and HTML |
| Oxylabs | E-commerce and SERP parsers at scale | $15/mo per one source; vendor lists from $0.5 per 1K results | 85.8% (Proxyway); 69% (String) | JSON and HTML |
| Decodo | Cheapest credible entry point | $19/mo, plus a free plan | 85.88% (Proxyway 2025) | JSON and HTML |
| Apify | Prebuilt site-specific scrapers | $19/mo plus compute units | Not included in the Proxyway or Scrape.do sets | JSON shaped by the chosen actor |

Two things to read out of that table. First, Bright Data and Zyte win on hardened sites and charge accordingly; Bright Data's own blog cites the 98.87% figure, so treat it as vendor-reported even though the underlying benchmark is third-party. Second, Firecrawl's 33.69% on Proxyway's protected set and its 80% in String's test are the same product measured twice, which is why "ranked fourth" and "worst success rate" can both be true.

## Who should not buy ScraperAPI

- **Your target list is mostly Cloudflare or DataDome protected.** At 60–69%, a third of your requests fail. Bright Data or Zyte handle those better, at a higher price per request.
- **You need responses in one to three seconds.** Zyte measured 1.43s median, ScrapingBee 2.18s and Oxylabs 2.72s in HasData's test; ScraperAPI measured 9.07s and 29s with rendering.
- **You need structured JSON from arbitrary pages.** Dedicated endpoints cover Amazon, Walmart, eBay and Google. Everything else is HTML or markdown plus your own parser.
- **You need a prebuilt scraper for a specific site.** Apify's actor store covers thousands of named targets; ScraperAPI's structured endpoints cover four.
- **You need city-level or non-US/EU geotargeting on a small budget.** Business at $299 is the floor, and geotargeting is country-level, not city-level.

## FAQ

**Can ScraperAPI get past Cloudflare?**
It can, at a cost. Bypass logic for Cloudflare, Cloudflare Turnstile, DataDome, PerimeterX/HUMAN and Akamai adds 10 credits to the base request and is applied automatically when ScraperAPI decides to use it. Published benchmarks put success at 60–69% on deliberately hardened target lists, so it works often enough to be a supplement and not often enough to be your only route.

**How many pages does the $49 plan actually buy?**
100,000 credits, which is 100,000 plain pages, 20,000 Amazon pages at 5 credits, 4,000 Google SERPs at 25 credits, or about 4,700 pages that need both bypass and rendering at 21 credits. The Domain Cost Estimator in the dashboard prices specific URLs before you commit.

**Does it return JSON?**
Not by default. The primary output is raw HTML. Structured JSON comes from dedicated endpoints for Amazon, Walmart, eBay and Google, and auto parsing can attempt extraction on other pages at no extra credit cost.

**Is there a free trial or a free plan?**
Both. The trial runs 7 days with 5,000 credits and no credit card. When it ends you can drop to the free plan with 1,000 credits per month and 5 concurrent threads, or move to a paid tier. The earlier "1,000 free credits per month" and "7-day trial" descriptions floating around in comparison posts are two halves of the same policy, not a contradiction.

**What happens when credits run out?**
On Hobby, Startup and Business you get HTTP 429 responses. Pay-as-you-go overage billing exists only from Scaling upward, and only up to a monthly cap you set yourself. Plan retry and backoff accordingly.

**How does this compare with Bright Data or Zyte?**
Bright Data and Zyte publish higher success rates on hard targets and charge more per request, with Zyte requiring a $100/month minimum. ScraperAPI is cheaper on plain pages and strong on retail and SERP domains. The right choice depends on your target list, not on a general ranking.

## Picking a plan without overpaying

The decision rules are short.

Scraping public catalogues, SERPs or lightly protected pages under 100,000 requests a month: **Hobby at $49**. It is the cheapest legitimate entry into this category and the 20 threads are enough for scheduled batches.

Same workload but you need geotargeting outside the US and EU: **Business at $299**, because Hobby and Startup cannot route there regardless of volume.

Heavy multiplier usage (rendered pages, protected targets, Google SERPs) where you keep hitting 429 errors: **Scaling at $475**, which drops the effective per-page cost by roughly five times and adds pay-as-you-go so a spike does not break the pipeline.

Rendered pages in the millions or a 24-hour batch window: talk to Enterprise, or split the work across an Async API job and a second provider for the domains that keep failing.

Before you pay, do three things: run 100 of your own URLs through the Domain Cost Estimator, confirm whether your targets need country-level geotargeting, and check the current trial terms on the pricing page, since credit allowances and plan limits are the parts vendors change most often. If your own test comes back above 90% success, the benchmark averages do not apply to you and the $49 tier is likely all you need.

👉 [Start the 7-day ScraperAPI trial or compare every plan side by side](https://www.scraperapi.com/pricing?fp_ref=coupons)
