# 4. Contest dashboards

**RNF Technologies · 2026 · live leaderboards on the office TVs**

## The problem
The company runs sales and project-manager contests, and the winners travel to an international conference (Singapore, Dubai). Each contest needed a live leaderboard that everyone could see and trust, with clear rules.

## What I built
Themed TV boards that update by themselves:
- a **basketball-themed** board for the sales contest
- a **Formula 1-themed** board for the project-manager contest
- a **"flight to Dubai"** board for the Dubai sales contest
- a smaller board for the rest-of-the-world sales team

Each board rotates through pages: standings, a scorecard, "what it takes to be number 1", and a full-screen pop-up with a sound when a new deal comes in.

## How it works
- Sales come from the team dashboard's database and HubSpot; a new sale shows on the TV within seconds.
- When a new version is released, the TV reloads itself, so nobody has to touch it.
- **Example rules:** deals count less when they come from an easier source (a past client or a conference lead); repeat payments from the same client within 31 days count as one sale; refunds come off the score; a deal with a "second voice" is split 70/30.

## My part
I designed the boards, the pages and the themes. Some rules were mine, for example the 60-day rule for when a client counts as a past client. Before the PM contest started, I noticed that the PMs' books were very different in size, so a simple comparison would be unfair; we gave every PM the same common target. Most other rules came from the sales managers. The code was written with an AI coding assistant.

## Checks
For the Dubai board, every counted sale was re-checked by hand from the raw records (39 of 39 correct), and a second, separate calculation matched the board on every row (0 differences).

## Results
- The boards run on the office TVs, and managers praised them.
- People changed how they worked: for example, more reps closed deals alone to keep full points. Scoring rules shape behaviour.

## Tools
React · Node.js and TypeScript · MySQL · SQL · Google Apps Script · Python (a small relay that copies counts to a sheet-based board)
