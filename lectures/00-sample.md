---
theme: apple-basic
title: 샘플 슬라이드
info: |
  교안 디자인 시스템 확인용 샘플입니다. 실제 교안은 lectures/ 아래에 회차별로 추가합니다.
colorSchema: light
transition: fade
mdc: true
lineNumbers: false
fonts:
  sans: SUIT Variable
  mono: Nanum Gothic Coding
  provider: none
layout: intro
---

# 멀티모달 AI 그로스 마케팅

샘플 슬라이드 · 디자인 시스템 확인

<div class="absolute bottom-10 text-sm" style="color: var(--muted)">
  Slidev · Apple Basic
</div>

---
layout: default
---

# 폰트 역할

제목, 본문, 코드와 강조 블록에 각각 다른 폰트를 씁니다.

| 역할 | 폰트 | 쓰는 곳 |
| --- | --- | --- |
| 제목 | IBM Plex Sans KR | 슬라이드 제목, 섹션 제목 |
| 본문 | SUIT | 문단, 목록, 표 |
| 코드·강조 | Nanum Gothic Coding | 코드 블록, 인용문, 강조 블록 |

<Callout title="확인 방법">
  이 슬라이드에서 제목과 표 머리글, 본문, 아래 코드가 서로 다른 폰트로 보이면 정상입니다.
</Callout>

---
layout: section
---

# 01
지표 읽기

---
layout: statement
---

# CTR과 전환율의 분모는 다르다

---
layout: default
---

# 퍼널 지표 정의

- **CTR** = 클릭 ÷ 노출
- **CPC** = 지출 ÷ 클릭
- **전환율** = 전환 ÷ 방문

<Callout title="핵심">
  분모가 다르면 같은 퍼널 단계가 아니므로, 두 값을 바로 비교하지 않는다.
</Callout>

> 인용문도 강조 블록과 같은 폰트와 색을 씁니다.

---
layout: default
---

# 박스 면적 비율

SAM 응답의 박스 좌표로 요소가 화면에서 차지하는 비율을 계산합니다.

```python
def box_area_ratio(x1: int, y1: int, x2: int, y2: int, w: int, h: int) -> float:
    """박스가 전체 이미지에서 차지하는 비율(0~1)."""
    return ((x2 - x1) * (y2 - y1)) / (w * h)


print(box_area_ratio(120, 80, 520, 480, 1080, 1080))  # 0.1371...
```

다음 슬라이드는 큰 숫자 레이아웃을 확인하기 위한 예시입니다.

---
layout: fact
---

# 7,700
그룹당 필요한 노출 수 (클릭률 1.0%에서 1.5%로, 유의수준 5%, 검정력 80%)

---
layout: default
---

# 다음 단계

- `lectures/` 아래에 회차별 슬라이드 파일을 추가합니다.
- 공통 스타일은 `lectures/styles/index.css`, 공통 컴포넌트는 `lectures/components/`에 둡니다.
- 실행: `npm run sample` 또는 `npm run dev -- lectures/<파일>.md`
