# PROJECT.md

Team: [9, team name]
Members: [양대성, 홍푸른, 배지열, 임태훈]
Last updated: [2026-09-27]

One page.
Draft it together before anyone writes a premortem, and come back to it after the merge.

You are not committing to this.
You are making it concrete enough to argue about, and concrete enough that a premortem about it means something.
A project idea you cannot imagine failing in a specific way is not yet an idea.

Later in the term you will run a Why Tree on this, and the Why Tree may well move it.
That is expected, and it is not wasted work.

Write in Korean or English.
Keep the headings exactly as they are.

---

## What we think we are building

[Instead of viewing personal bankruptcy as traditional legal practice, we are approaching it as an industrial engineering problem by turning this highly repetitive casework into a strict production line. The platform we are building directly routes raw client financial documents into structured application drafts, stripping away the manual data entry so attorneys only step in for hard exceptions and final sign-offs.]

## Who it is for

- **Person:** [Paralegals and supervising attorneys running high-volume personal bankruptcy practices.]
- **Situation:** [The exact moment a client dumps a chaotic pile of debt certificates, pay stubs, and asset records on their desk, and they have to extract the actual principal and interest to build a 36-month repayment schedule.]
- **What they do today instead:** [Staff stare at PDFs to hunt for numbers, manually typing the exact same figures into Excel sheets and court forms over and over. When things don't add up, they waste hours chasing the client down on KakaoTalk or calling them just to plug holes in the data.]

## How we know this problem is real

[Nobody yet. We haven't actually sat inside a law office to watch the staff handle this manually.
Right now, our evidence comes from securing 10 anonymized, previously completed personal bankruptcy case files for our initial pilot test. We are looking at the massive paper trail these cases generated and inferring that the manual data extraction must be a bottleneck, but we still need to go out and interview the actual paralegals who do the typing to prove it.]

## Why us

[One of our team members is actually a law firm CEO. This isn't a theoretical pain point we stumbled upon; it is a desperate bottleneck their own office deals with every single day. This gives us a live, built-in testing ground and immediate access to real staff who can tell us exactly what works and what fails. We can skip the cold-calling phase and deploy our pilot straight into a real practice.]

## What would make us drop this idea

[We will scrap this project if we hit any of these three hard stops:
 First, if strict privacy constraints prevent us from securing properly masked client files for our 10-case pilot, or if the staff running that pilot end up spending more time hunting down our extraction errors than they currently do typing the numbers from scratch.   
 Second, if our upcoming business consulting session with the professor confirms the business model lacks real commercial upside.
 Finally, if our specialized pipeline fails to beat a generic tool. If simply dumping all the raw client files into Astra yields a more accurate bankruptcy application draft, or if our approach fails to drastically cut token costs compared to that brute-force method, there is no reason to build this.]

The thing you are least sure about does not go here.
It goes at the top of `docs/QUESTIONS.md`, because it is the best use of the 30 minutes.

---

## Revision log

| Date | What changed and why |
|---|---|
| [YYYY-MM-DD] | Draft for consultation |
| [YYYY-MM-DD] | Revised after consultation on [date]: [what changed] |
