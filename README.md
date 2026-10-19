# Kirubel Abraham (Kay)

Product Advocate, Expansion at Apify, Prague. Ten years between the people who buy software and the people who build it. Lately, building it too.

**[kayabraham.com](https://kayabraham.com)** has the full write-up of every machine below, with a working diagram of each.

## What I build

**[News Intelligence Agent](https://apify.com/kay_abraham/news-intelligence-agent)**
Ask a news question in plain English and get a cited brief back. A six-stage pipeline over Google News, RSS, Reddit and X: plan, discover, extract, analyse, synthesise, deliver. Every record reports the health of each source. Public on the Apify Store, pay per event. Node.js.

**[Expansion Engine](https://kayabraham.com/machines/engine/)**
An Apify Actor that reads six live signal feeds, scores every account and gives each Product Advocate on the team a ranked desk twice each weekday. It holds back accounts already in a live deal or contacted in the last week, tags every account with its owner, and keeps its state in a named store so a crash can't double-post. Python, 786 tests, nightly CI. The repo is private because it holds company data.

**[Override Watch](https://kayabraham.com/machines/override-watch/)**
n8n workflow. Every weekday at 09:00 it finds custom prices that expire in seven days and tells the account manager in Slack. On Fridays the window stretches to nine days, so weekend expiries get their warning too. Running since February 2026, co-owned with RevOps.

**[Overdue Monitor](https://kayabraham.com/machines/overdue-monitor/)**
n8n workflow. A daily overdue-invoice digest for each account manager and a Monday summary for finance ops. It reads the notes and snoozes people leave in the channel, retries the warehouse query and stays inside Slack's block and character limits. On version 5.1.1, co-owned with RevOps.

Also on the site: Finance's gross margin report rebuilt from raw warehouse tables and matched to the cent, a shared SQL library for pricing and usage questions, and a drafting agent that writes customer emails in my voice for me to review and send.

## How I build

- Standard library first. The Engine's only dependency beyond Python's standard library is the Apify SDK.
- Failures announce themselves. A missing feed or token is skipped and reported, and a parser that stops matching raises an alarm.
- State between runs lives in a named store.
- The tools inform and I decide what reaches a customer.

## Stack

Python, Node.js, TypeScript, Apify Actors, n8n, Slack API, HubSpot API, SQL on Snowflake via Redash. Astro and Three.js for the site.

## Elsewhere

[kayabraham.com](https://kayabraham.com) · [Apify Store](https://apify.com/kay_abraham) · [LinkedIn](https://www.linkedin.com/in/kirubelabraham)
