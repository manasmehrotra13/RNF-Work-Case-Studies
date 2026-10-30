# 2. PM Recommendations

**RNF Technologies · a tab in The Scale Agency Dashboard**

## The problem
Every month around 300 new recurring clients have to be handed to one of about 18 project managers (PMs). The PM manager used to choose by judgment, so most of the work went to a handful of trusted PMs, and the others never got a chance to build a track record.

## What I built
A ranking of PMs for each new client, built from our own history:
1. **The sales rep's past clients:** for the rep who closed the sale, which PMs looked after that rep's earlier clients, and whether those clients kept paying.
2. **Each PM's own retention:** how well their clients keep paying overall.
3. **A fair-share rule:** no PM goes above the monthly average number of new clients; after that, the next-best PM is recommended.
4. **Room to learn:** PMs who have never worked with a rep are sometimes recommended on purpose, so we build data for every pair.

## How it is used
- The ranking is built into the dropdown the PM manager uses to assign clients, best first.
- It recalculates by itself as new payments come in.
- A separate page lists every new sale, the PM it went to, where that PM ranked, and the reason for the top pick in plain English.
- The manager still makes the final call, for example when a client asks for a specific PM.

## My part
The idea and all the rules are mine. The code was written with an AI coding assistant.

## Results
- In daily use since 2026, built on about **1,650 past handovers** since April 2024.
- New clients are now spread much more evenly across PMs.
- **Not measured yet:** whether recommended picks keep clients longer. That is the next step, and the page already holds the data for it.

## Tools
SQL · MySQL · The Scale Agency Dashboard (Node.js, React)

## What I learned
A recommendation needs fairness rules, not just a score, and the person who decides should stay in control.
