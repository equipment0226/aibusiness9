# PROJECT.md

Team: \[Team 9, Firm Engine]
Members: \[임태훈, 홍푸른, 배지열, 양대성]
Last updated: \[2026-10-05]

One page.
Draft it together before anyone writes a premortem, and come back to it after the merge.

You are not committing to this.
You are making it concrete enough to argue about, and concrete enough that a premortem about it means something.
A project idea you cannot imagine failing in a specific way is not yet an idea.

Later in the term you will run a Why Tree on this, and the Why Tree may well move it.
That is expected, and it is not wasted work.

Write in Korean or English.
Keep the headings exactly as they are.

\---

## What we think we are building

\[개인회생 희망 고객, 개인회생 담당 변호사, 개인회생 사건 담당자 (사무장), 개인회생 고객 상담직원을 위한 개인회생 AI-Automation 서비스입니다. 

&#x20;의뢰인의 진술과 원본 금융 서류를 AI로 구조화된 신청서 초안으로 즉시 변환하여 수작업 데이터 입력을 최소화하고, 원본과 입력값의 검증 및 대조까지 AI가 수행하도록 합니다.   

&#x20;변호사와 사무장은 까다로운 예외 사항 내지 전체 프로세스의 최종 검토 및 승인 단계 중심으로 개입하도록 하는 효율과 편의를 제공하고자 합니다.]

## Who it is for

* **Person:** \[개인회생 희망 고객 (고객 넣을지 말지 회의 제안), 개인회생 담당 변호사, 법률회사 개인회생 사건 담당자, 개인회생 고객 상담직원]
* **Situation:** \[1) 회생신청을 위한 고객 소비내역 (카드 등)과 진술 수취 후 증빙 간 서류와 진술이 일치하는지 하나하나 대조해 진술서와 신청서류를 작성하거나 수작업 검수,

&#x20;                              2) 법원 보정 명령이 오면 기존 서류와 새답변이 어긋나지 않았는지 하나하나 수작업 대조,

&#x20;                              3) 의뢰인이 부채증명서, 급여명세서, 재산 관련 서류를 정리되지 않은 채 한꺼번에 책상 위에 쏟아놓고, 

&#x20;                     직원이 그 안에서 실제 원금과 이자를 뽑아 36개월 변제계획표를 만들어야 하는 순간

&#x20;            

* **What they do today instead:** 

&#x20;    \[서식은 회생 서류작성 프로그램으로 만들지만, 진술과 증빙 일치 여부는 담당자가 PDF 출력물을 대조하고 엑셀과 법원양식에 반복하여 금액을 옮겨 적는다. 고객진술은 카톡/메일을 다시 검색해 찾고, 이전 제출 서류와의 일관성은 담당자와 변호사의 기억에 의존한다. 놓친 불일치는 법원 보정명령이 와야 드러난다. 숫자가 맞지 않으면 빠진 데이터를 채우기 위해 의뢰인에게 카카오톡을 보내거나 전화를 걸어 확인합니다.]

## How we know this problem is real

\[본 Painpoint 사례는 실제 Decent 법률 사무소의 CEO 변호사 홍푸른님의 현장 경험 공유를 통해 알게 되고, 논의한 사실입니다.]



or



아직 직접 확인한 사람은 없습니다. 법률사무소에 직접 들어가 직원들이 이 작업을 수작업으로 처리하는 모습을 관찰한 적은 아직 없습니다. 현재 근거는 초기 파일럿 테스트를 위해 확보한 비식별 처리된 기존 개인회생 완료 사건 10건입니다. 이 사건들에서 생성된 방대한 서류량을 보고 수작업 데이터 추출이 병목일 것이라고 추론하고 있지만, 이를 입증하려면 실제로 입력 작업을 하는 직원들을 직접 인터뷰해야 합니다.

## Why us

\[CEO를 통한 시스템과 데이터, 현장과 실상 Access. 실제로 테스트할 수 있는 현장이 이미 마련되어 있고, 무엇이 효과가 있고 무엇이 실패하는지 정확히 알려줄 실무 직원들에게 바로 접근할 수 있습니다. 콜드콜 단계를 건너뛰고 파일럿을 실제 사무소에 곧바로 적용할 수 있습니다.]

## What would make us drop this idea

\[사용자 반응 기준: 실무자 (사건 담당자, 변호사 등) 대상 모수 중 60% 이상이 "진술 증빙 대조는 지금방식이나 쓰는 프로그램으로 충반하다"고 하면 Drop 한다.



or

첫째, 엄격한 개인정보 보호 제약 때문에 10건 파일럿에 필요한 적절히 마스킹된 의뢰인 파일을 확보하지 못하거나, 파일럿을 운영하는 직원들이 지금 숫자를 처음부터 직접 입력하는 것보다 저희 시스템의 추출 오류를 찾아내는 데 더 많은 시간을 쓰게 되는 경우. 둘째, 곧 있을 교수님과의 비즈니스 컨설팅 세션에서 이 비즈니스 모델에 실질적인 상업적 가능성이 없다고 확인되는 경우. 마지막으로, 저희의 특화 파이프라인이 범용 도구를 이기지 못하는 경우. 원본 의뢰인 파일을 전부 Astra에 그대로 넣었을 때 더 정확한 개인회생 신청서 초안이 나오거나, 그런 무식한(brute-force) 방식에 비해 토큰 비용을 크게 줄이지 못한다면 이것을 만들 이유가 없습니다.





Revision log

|Date|What changed and why|
|-|-|
|\[2026-10-05]|Draft for consultation|
|\[YYYY-MM-DD]|Revised after consultation on \[date]: \[what changed]|



