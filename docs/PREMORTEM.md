# PREMORTEM.md

Team: [9, Firm Engine]
Members: [임태훈, 배지열, 홍푸른, 양대성]
Merged on: [2026-10-05]
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
| [Daeseong Yang] | `docs/premortem/Daeseong Yang.md` | [2026-10-03] | [y] |
| [Jiyeol Bae] | `docs/premortem/Jiyeol Bae.md` | [2026-10-02] | [y] |
| [Pureun Hong] | `docs/premortem/Pureun Hong.md` | [2026-10-03] | [y] |
| [Taehoon Im] | `docs/premortem/Taehoon Im.md` | [2026-10-05] | [y] |

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
| 1 | 승인 가능한 수준의 문서를 생성해내지 못하거나, 법적 판단 Logic이 오작동 할 경우. 또한 주제가 변경되어 도메인 전문가가 없는 영역의 Product에 도전하게 될 경우 이로 인한 품질 문제 발생 가능 | 품질 실패 | 양대성, 배지열, 홍푸른 | 3 |
| 2 | 무리한 차별화 기획과 부가 기능 추가로 인한 리소스 낭비. 이로 인해 기본 기능 완성 및 데모 에러 검증에 쓸 시간을 빼앗겨 1/3 수준의 껍데기만 시연하게 될 경우. | 범위 선정 실패 | 홍푸른, 임태훈, 양대성 | 3 |
| 3 | (us) 직군별 관점 차이를 극복하지 못하고, 각자의 대안만 고집하다 시간을 허비하거나, 시연에서의 Q&A 답변마저 갈라지는 경우. | 팀 합의 부재로 인한 시간 지연 및 발표 실패 | 임태훈 | 1 |
| 4 | 의뢰인의 낮은 디지털 친화성이 고려되지 않았거나, 기존 업무 환경과 연동성이 낮은 Product가 제작되어 실사용 효율이 떨어질 경우. | 사용자 환경, 기능 고려 부족 | 홍푸른 | 1 |
| 5 | (us) 제출 마지막 주까지 AI의 낮은 신뢰도 문제를 뚫어내지 못하자, 데모 시연을 넘기기 위해 결과물을 조작하게 되는 경우. 혹은 제작한 부대 기능에 대한 기술적 전문성 부족으로, 근본 원인 규명 대신 임기응변식 대처만 하고 시스템 불안정성을 해결하지 못한 경우 | 품질 실패 및 결과물 조작 | 배지열 | 1 |
| 6 | (us) 법률 검토 담당자의 검수 부족 및 검수 일정 미할당으로 인해, 치명적 오류가 뒤늦게 발견되는 경우 | 품질 실패 | 홍푸른 | 1 |
| 7 | (us) 특정 팀원의 압도적인 AI 구현 속도에 위축되어 기획부터 아이디어 제시를 포기했고, 연장자라는 이유나 생업을 핑계로 잘못된 방향을 알면서도 클레임 없이 침묵으로 일관했다. | 역량 비대칭 및 방관 | 배지열 | 1 |
| 8 | (us) 카카오톡 및 통화 API의 기술적 제약과 보안 장벽을 정확히 아는 사람도 없이 상담 기능을 사양에 넣고 강행하다, 결국 시간만 날리고 불완전한 상태로 폐기했다. | 기술 제약 검토 누락 | 임태훈 | 1 |
| 9 | 고객 민감 정보라는 제약 탓에 실제 승인/반려 전략에 필요한 데이터나 과거 테스트 세트를 수집하지 못하는 경우 | 검증 데이터 부재 | 양대성 | 1 |

Add rows until every individual list is used up.

## 4. What only one person saw

Look again at every row above that a single member raised.

| Cause | Raised by | What we decided to do about it |
|---|---|---|
| (us) 직군별 관점 차이를 극복하지 못하고, 각자의 대안만 고집하다 시간을 허비하거나, 시연에서의 Q&A 답변마저 갈라지는 경우. | 임태훈 |  |
| 의뢰인의 낮은 디지털 친화성이 고려되지 않았거나, 기존 업무 환경과 연동성이 낮은 Product가 제작되어 실사용 효율이 떨어질 경우. | 홍푸른 |  |
| (us) 제출 마지막 주까지 AI의 낮은 신뢰도 문제를 뚫어내지 못하자, 데모 시연을 넘기기 위해 결과물을 조작하게 되는 경우. 혹은 제작한 부대 기능에 대한 기술적 전문성 부족으로, 근본 원인 규명 대신 임기응변식 대처만 하고 시스템 불안정성을 해결하지 못한 경우 | 배지열 |  |
| (us) 법률 검토 담당자의 검수 부족 및 검수 일정 미할당으로 인해, 치명적 오류가 뒤늦게 발견되는 경우 | 홍푸른 |  |
| (us) 특정 팀원의 압도적인 AI 구현 속도에 위축되어 기획부터 아이디어 제시를 포기했고, 연장자라는 이유나 생업을 핑계로 잘못된 방향을 알면서도 클레임 없이 침묵으로 일관했다. | 배지열 |  |
| (us) 카카오톡 및 통화 API의 기술적 제약과 보안 장벽을 정확히 아는 사람도 없이 상담 기능을 사양에 넣고 강행하다, 결국 시간만 날리고 불완전한 상태로 폐기했다. | 임태훈 |  |
| 고객 민감 정보라는 제약 탓에 실제 승인/반려 전략에 필요한 데이터나 과거 테스트 세트를 수집하지 못하는 경우 | 양대성 |   |

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
