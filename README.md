# Kirubel Abraham Assefa (Kay)

Product Advocate at Apify, Prague. I look after Apify's growing accounts and build the tools that watch them for me.

## What I ship

**[News Intelligence Agent](https://apify.com/kay_abraham/news-intelligence-agent)**
Ask a news question in plain English. Get a cited brief back. It pulls Google News, RSS, Reddit and Twitter, routes paywalled publishers to dedicated scrapers, groups the articles into themes and flags anything odd. Public on the Apify Store, pay per event. Node.js.

**Expansion Engine**
An Apify Actor that reads a billing-alerts Slack channel twice a day, keeps the accounts that are mine, scores them, holds back anyone already in a live deal or contacted in the last week, and DMs me a ranked list with one play per account. It also sweeps the warehouse for accounts that grow quietly and never trip an alarm, and tags every account with its owner so one instance can serve the whole team. Python, standard library plus the Apify SDK. The working repo is private because it holds real account data. A redacted showcase is on its way.

**Override Watch**
n8n workflow. Every weekday morning it checks which custom-price overrides expire within seven days and tells the account manager on Slack. A Friday bridge covers expiries that land on the weekend. Live since February 2026.

**Overdue Monitor**
n8n workflow. Daily overdue-invoice digest grouped by account manager, plus a Monday summary for finance ops. It reads the free-text notes people leave in the channel, retries the warehouse query, and stays inside Slack's block and character limits. Live since July 2026, co-owned with RevOps. Internal code, so no link.

## Rules I build by

- Standard library first. The engine's logic has no dependency outside the Apify SDK.
- Fail open, never silent. A missing token skips one check and says so in the log. A parser that stops matching raises an alarm.
- State between runs lives in a named store, so a crash never double-posts or drops a window.
- Nothing these tools find goes to a customer on its own. They tell me, I decide.

## Stack

Python, Node.js, Apify Actors, n8n, Slack API, HubSpot API, SQL on Snowflake via Redash.

## Elsewhere

[Apify Store](https://apify.com/kay_abraham)
