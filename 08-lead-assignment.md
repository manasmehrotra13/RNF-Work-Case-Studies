# 8. Lead Assignment

**RNF Technologies · my first automation (2025), now part of The Scale Agency Dashboard**

## The problem
Every day, about 100 to 200 new leads came in. Each one had to be checked (is it new, did it come back, or is it a duplicate?), shared fairly among the sales reps, and set up in HubSpot. All of it was done by hand.

## What I built
An automatic process that, for every new lead:
1. Checks HubSpot and marks it as **fresh**, **re-generated** or a **duplicate** (seen again within 30 days).
2. Adds company details from an internal data source.
3. Assigns a sales rep in turn (round robin), so the work is shared fairly.
4. Creates or updates the company and contact in HubSpot, with notes.
5. Sends a daily report to the sales managers.

It started as Google Apps Script on a sheet. It now runs inside The Scale Agency Dashboard on a schedule: rest-of-the-world leads in the afternoon and US leads in the evening, India time.

## My part
The logic and the rules are mine. My manager showed me that "anything you do every day can be automated", and I wrote out the exact steps and built the scripts with AI help.

## Results
- From fully manual to about **90% automatic** at first, and **fully automatic since October 2026**, including the daily report.

## Tools
Google Apps Script · HubSpot API · Node.js · MySQL

## What I learned
Write down the exact steps you follow by hand first. Then the automation is straightforward.
