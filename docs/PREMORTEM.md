# PREMORTEM.md

Team: [team number and name]
Members: [names]
Merged on: [YYYY-MM-DD]
Last updated: [YYYY-MM-DD]

> **Order matters, and here it is the entire method.**
> Every member first writes their own list in `docs/premortem/<name>.md`, alone.
> Only then does the team fill in this file.
>
> If you brainstorm as a group first, the first risk named anchors everyone else, and the quiet member's risk, which is usually the real one, never gets written down.
>
> Write content in Korean or English.
> Keep the headings exactly as they are.

---

## 1. Individual lists

| Member | File | Written on | Causes listed |
|---|---|---|---|
| [name] | `docs/premortem/[name].md` | [YYYY-MM-DD] | [n] |
| [name] | `docs/premortem/[name].md` | [YYYY-MM-DD] | [n] |
| [name] | `docs/premortem/[name].md` | [YYYY-MM-DD] | [n] |

## 2. Read-out

Go around the table.
One cause each, in turn, until every list is exhausted.
No debating during the read-out, and nobody reads their whole list at once.
People have to feel safe saying the awkward one, so the only allowed response is writing it down.

## 3. The merged list

Every cause from every list goes here.
Stack the repeats into one row and keep the sharpest wording, not the most diplomatic one.
Cluster by problem, never by role or department: once a cluster is called "development", half the team decides it is somebody else's problem.

Sort by how many members raised it, most first.
The repeats are your priority signal, and you get it for free.
Break ties by expected damage.

Mark a cause with **(us)** when it exists because of who is on this team, not because of the software.
At least two rows must carry that mark: skill asymmetry, time asymmetry, who will actually debug the code the artificial intelligence (AI) wrote, who has a product launch at work in November, who agrees in meetings and then goes quiet.
A premortem with no **(us)** rows is a premortem about software, not about this team.

| # | Failure cause (past tense, specific) | Problem cluster | Raised by | How many |
|---|---|---|---|---|
| 1 | | | | |
| 2 | | | | |
| 3 | | | | |
| 4 | | | | |
| 5 | | | | |
| 6 | | | | |
| 7 | | | | |
| 8 | | | | |

Add rows until every individual list is used up.

## 4. What only one person saw

Look again at every row above that a single member raised.

| Cause | Raised by | What we decided to do about it |
|---|---|---|
| | | |
| | | |

A cause only one person saw is not a weak signal.
It is usually the one the rest of the team is structurally unable to see.

## 5. The three we act on

Pick at most three.
More than three is a list, not a plan.

The top of the merged list is where you start looking, not an automatic answer.
If a cause only one person saw is the one that would end the project, pick it.

| # | Failure cause | Early warning signal — what we would actually observe, and when | Countermeasure — the action | Owner | By when |
|---|---|---|---|---|---|
| 1 | | | | | |
| 2 | | | | | |
| 3 | | | | | |

Three tests every row must pass:

- **The signal is observable.** "We notice we are falling behind" is not a signal. "Two members have not opened the project in seven days" is.
- **The countermeasure is an action, not a posture.** "열심히 하기", "우선순위 관리", and "we will be careful" are intentions. "Call three potential users and write down what they say" is an action. If it has no verb, rewrite it.
- **The owner is one named person, and there is a date.** "The team" owns nothing. A countermeasure with no date is a countermeasure with no week: it never lands on anyone's calendar.

> Example of a finished row. Delete this block before you send.
>
> - **Failure cause:** Nobody outside the team ever used it. We demoed to ourselves for ten weeks. **(us)**
> - **Early warning signal:** On October 24, no one outside the team has touched a working screen.
> - **Countermeasure:** Show a clickable first screen to three people who have the problem, and write down the first thing each of them does.
> - **Owner:** [one name]
> - **By when:** October 24

You do not need a 1-to-5 likelihood and impact matrix, and we would rather you did not add one.
It makes every risk look equally considered whether or not it was.

Everything in section 3 that is not in this table is a risk you are knowingly leaving alone for now.
That is a decision, and it is fine.

---

## Revision log

Any change of direction needs a new row here within one week.
A premortem that analyzes a product you no longer build is worse than none, because it reads as covered.

| Date | What changed and why |
|---|---|
| [YYYY-MM-DD] | Draft for consultation |
| [YYYY-MM-DD] | Revised after consultation on [date]: [what changed] |

---

Method note: Gary Klein, "Performing a Project Premortem", Harvard Business Review, September 2007.
