# 1. Payments and team dashboard

**RNF Technologies, 2026 · the main tool of the digital marketing division**

## The problem
The division ran on Google Sheets: one sheet for each of 16 project managers, a master sheet joining them, and more sheets for payment tracking and call reports. One small change meant editing 16 sheets, numbers did not always match, and anyone could copy a whole sheet.

## What I built
One web app for the whole division. Its tabs cover:
- **Money:** payments, refunds and disputes, month-end numbers, month-on-month trends, delayed payments
- **Project managers:** each PM's book of clients ("inventory"), retention, upsells, a month-by-month performance review
- **Sales:** new sales, the sales pipeline, a sales scoreboard, a leads-to-sales funnel
- **Leads:** lead management and lead-generation reports
- **Calls:** the daily call report (see case study 2)
- **Admin:** user access by tab, a log of every change, live health alerts, and a bin where deleted rows can be restored

## How it works
- Payments from Stripe and PayPal flow into a MySQL database every 5 minutes, and deals from HubSpot every minute.
- The server works out every number with SQL, and the website shows it.
- Background jobs assign new leads and send the daily report on their own.
- In-app alerts warn when a job fails or the database is getting busy.
- When a payment is mapped, the app creates the HubSpot deal and next month's client record by itself.

## My part
I designed the data model, the metrics (for example retention %, money in the bank after refunds, PM efficiency), the business rules and the checks. Every new number was matched against the old sheets before people switched over. The code was written with an AI coding assistant from my detailed specifications, and I tested it at each step.

## Results
- About **65 people** use it every day: project managers, sales reps, lead generation and managers.
- It replaced **16 project-manager sheets and a master sheet**, and holds **32 months** of history in one place.
- Mapping a payment takes seconds; refunds and disputes match up automatically.
- In my words: work that used to take a week now takes one or two days.

## Tools
MySQL 8 · SQL · Node.js, Express and TypeScript · React · Stripe, PayPal, HubSpot and Gmail APIs · scheduled jobs · Python (for Excel and PDF reports)

## What I learned
Design the data first. Check every new number against the old system before asking people to trust it. Build alerts, so problems are found before users find them.
