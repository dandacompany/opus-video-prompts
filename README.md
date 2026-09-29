<div align="center">

# Opus 5.5 영상 제작 프롬프트

**Claude Opus 5.5로 코드를 작성해 영상을 만드는 공개 사례와 한국어 프롬프트 모음**

프롬프트 17개 · 공개 사례 53건 · 제작 방식 9가지

[빠른 시작](#빠른-시작) · [프롬프트 목록](#프롬프트-목록) · [사례 목록](#사례-목록) · [작성 요령](#프롬프트-작성-요령) · [출처](#출처)

</div>

## 이 저장소는 무엇인가

Opus 5.5는 영상 파일을 직접 출력하는 모델이 아니다. HTML Canvas, p5.js, Three.js, Remotion, Manim, Blender 등의 코드를 작성해 장면을 만든다. 브라우저에서 프레임을 캡처하고 FFmpeg로 MP4를 합성할 수 있다. 음악에는 Web Audio나 Python 합성을, 내레이션에는 TTS를 사용할 수 있다.

이 방식은 모션 그래픽, 선화·수묵 애니메이션, 설명 영상, 제품 출시 영상, 가사 뮤직비디오에 잘 맞는다. 사실적인 인물 영상이 필요하면 Seedance, Runway, Higgsfield 같은 영상 모델을 호출해 생성된 영상을 편집하는 흐름도 있다.

이 저장소는 Opus 5.5 공개 첫 주(2026년 9월 22~25일)에 X, Bilibili, Linux.do, GitHub, YouMind 등에 올라온 공개 사례를 정리했다. **프롬프트는 한국어 번역·현지화본**이며, 작성자와 원문 링크를 각 파일에 표기했다. 일부 원문은 발췌되거나 재게시 과정에서 잘렸으므로 해당 파일에 그 사실을 명시했다. 사례의 시간과 비용은 게시자가 밝힌 수치이며 동일한 결과를 보장하지 않는다.

## 빠른 시작

1. Claude Code를 설치하고 Opus 5.5를 선택한다. 추론 강도는 high 이상으로 설정한다.
2. 영상 렌더링에 필요한 Node.js, Chrome, FFmpeg를 준비한다.
3. 빈 폴더에서 아래 프롬프트 하나를 복사하고, 필요한 입력값과 자산을 제공한다.
4. 생성된 코드와 시범 프레임을 확인한 뒤 MP4로 렌더링한다.

가장 짧은 예시는 [추론 스타트업 출시 영상](prompts/01-inference-startup-launch.md)이다.

```text
현대적인 추론 기술 스타트업을 위한 세련되고 강렬한 출시 영상을 만들어 줘.
```

## 프롬프트 목록

| 자료 ID | 프롬프트 | 작성자 | 유형 | 파일 |
|---:|---|---|---|---|
| 01 | 추론 스타트업 출시 영상 | Deedy (@deedydas) | 한 문장 | [열기](prompts/01-inference-startup-launch.md) |
| 02 | 15초 모션 디자인 쇼릴 | Stephan Livera | 한 문장 | [열기](prompts/02-motion-showreel-15s.md) |
| 04 | Opus 5 광고: 애플 《1984》 오마주 | 1LittleCoder (YouMind 수록) | 한 문장 | [열기](prompts/04-opus-1984-ad.md) |
| 05 | Transformer를 설명하는 JavaScript 영상 | 바오위 (YouMind 수록) | 한 문장 | [열기](prompts/05-transformer-explainer-js.md) |
| 06 | 방에서 쿼크까지 확대하는 영상 | Taelin (YouMind 요약을 바탕으로 번역) | 한 문장 | [열기](prompts/06-room-to-quarks-zoom.md) |
| 07 | 30초 기업 설명 영상 템플릿 | Alex Prompter (@alex_prompter) | 구조화 템플릿 | [열기](prompts/07-business-explainer-30s.md) |
| 08 | 네그로니 칵테일 레시피 애니메이션 | Rory Flynn (@Ror_Fly) | 참고 이미지 | [열기](prompts/08-negroni-recipe-explainer.md) |
| 09 | 대기 대순환 설명: TTS와 이중 자막 | WY (@akokoi1) | 번역 프롬프트 | [열기](prompts/09-atmospheric-circulation-tts.md) |
| 10 | 실사 설명 영상을 선화 애니메이션으로 변환 | Axton (@AxtonLiu) | 번역 프롬프트 | [열기](prompts/10-talking-head-to-lineart.md) |
| 11 | 아우스터리츠 전투 역사 영화 | Winter (@WinterArc2125) | 장문 프롬프트 | [열기](prompts/11-austerlitz-film.md) |
| 12 | Remotion 앱 홍보 영상 1 | Danny Stuart | Remotion | [열기](prompts/12-remotion-app-promo-1.md) |
| 13 | Remotion 앱 홍보 영상 2 | Danny Stuart | Remotion | [열기](prompts/13-remotion-app-promo-2.md) |
| 14 | 실제 자산을 사용하는 SaaS 출시 영상 | Joe Davies (LinkedIn) | 브랜드 영상 | [열기](prompts/14-saas-launch-real-assets.md) |
| 15 | UI 변형 무한 반복 영상 | zero (@twoclipping) | 전문 템플릿 | [열기](prompts/15-ui-morph-loop.md) |
| 16 | 고급 미니멀 제품 영상 | zero (@twoclipping) | 전문 템플릿 | [열기](prompts/16-high-end-product-video.md) |
| 17 | 주문을 시전하는 픽셀 마법사 | Majid Manzarpour | 상세 사양 | [열기](prompts/17-pixel-wizard.md) |
| 18 | 상호작용하는 선사 시대 섬 | Vib3Coded | 상세 사양 | [열기](prompts/18-prehistoric-island-threejs.md) |

이 외에 긴 프롬프트 두 개는 원문 링크로 소개한다. [무지개 길 픽셀 달리기](https://x.com/riku720720/status/2102515058010132554)는 일본어 상세 사양이며, [Claude Pop 혼합 제작 뮤직비디오](https://x.com/donaldjewkes/status/2102801469976248500)는 fal 이미지 → Seedance 2.5 영상 → JavaScript 프레임별 재그리기 순서다.

## 한국어 프롬프트

아래 프롬프트는 공개된 원문 또는 인용된 발췌본을 한국어로 옮긴 것이다. 한국어 사용에 맞춰 자막과 인터페이스 언어를 바꾼 항목도 있다. 정확한 표현과 누락 여부를 확인하려면 원문 링크를 연다. 대괄호와 `<inputs>`는 사용자가 채워야 하는 항목이다.

### 01. 추론 스타트업 출시 영상

[원문](https://x.com/deedydas/status/2102787937482252537) · [설명과 사용 방법](prompts/01-inference-startup-launch.md)

<details>
<summary>한국어 프롬프트 펼치기</summary>

```text
현대적인 추론 기술 스타트업을 위한 세련되고 강렬한 출시 영상을 만들어 줘.
```

</details>

### 02. 15초 모션 디자인 쇼릴

[원문](https://x.com/stephanlivera/status/2103315922098470926) · [설명과 사용 방법](prompts/02-motion-showreel-15s.md)

<details>
<summary>한국어 프롬프트 펼치기</summary>

```text
15초짜리 역동적인 모션 그래픽 영상을 만들어 줘. 뛰어난 모션 디자이너의 이력서용 쇼릴처럼 실력을 마음껏 보여 줘.
```

</details>

### 04. Opus 5 광고: 애플 《1984》 오마주

[원문](https://youmind.com/opus-5-5-prompts) · [설명과 사용 방법](prompts/04-opus-1984-ad.md)

<details>
<summary>한국어 프롬프트 펼치기</summary>

```text
Opus 5를 위한 30초 광고를 만들어 줘.
```

</details>

### 05. Transformer를 설명하는 JavaScript 영상

[원문](https://youmind.com/opus-5-5-prompts) · [설명과 사용 방법](prompts/05-transformer-explainer-js.md)

<details>
<summary>한국어 프롬프트 펼치기</summary>

```text
JavaScript로 「Transformer란 무엇인가」를 설명하는 영상을 만들어 줘.
```

</details>

### 06. 방에서 쿼크까지 확대하는 영상

[원문](https://youmind.com/opus-5-5-prompts) · [설명과 사용 방법](prompts/06-room-to-quarks-zoom.md)

<details>
<summary>한국어 프롬프트 펼치기</summary>

```text
방에서 시작해 MacBook으로, 이어서 Apple M4 칩과 원자를 거쳐 마지막에는 쿼크까지 들어가는 애니메이션을 만들어 줘.
```

</details>

### 07. 30초 기업 설명 영상 템플릿

[원문](https://x.com/alex_prompter/status/2103499977632997524) · [설명과 사용 방법](prompts/07-business-explainer-30s.md)

<details>
<summary>한국어 프롬프트 펼치기</summary>

```text
모션 디자이너 전문가의 역할을 맡아 줘. 내 사업을 설명하는 30초 애니메이션을 단일 HTML 페이지로 만들어 줘. 장면은 5개다. 고객의 문제, 내가 제공하는 것, 3단계 작동 방식, 신뢰할 만한 근거 하나, 마지막으로 내 이름을 보여 줘. 굵은 글자, 부드러운 전환, 내 브랜드 색상을 사용해 줘. 내 사업: [판매하는 것, 대상 고객, 브랜드 색상을 설명]
```

</details>

### 08. 네그로니 칵테일 레시피 애니메이션

[원문](https://x.com/Ror_Fly/status/2102853258582880547) · [설명과 사용 방법](prompts/08-negroni-recipe-explainer.md)

<details>
<summary>한국어 프롬프트 펼치기</summary>

```text
작은 실험을 해 보자. JavaScript나 HTML 중 결과가 좋은 방법을 골라 레시피 설명형 모션 그래픽을 만들어 줄 수 있을까? 빈 잔에서 완성된 칵테일까지 전 과정을 보여 줘. 재료를 잔에 넣는 순간마다 재료명과 계량값을 표시하고, 전체 길이는 30초로 해 줘.
```

</details>

### 09. 대기 대순환 설명: TTS와 이중 자막

[원문](https://x.com/akokoi1/status/2102606609574941028) · [설명과 사용 방법](prompts/09-atmospheric-circulation-tts.md)

<details>
<summary>한국어 프롬프트 펼치기</summary>

```text
고등학교 지리 개념인 「대기 대순환」을 설명하는 애니메이션을 만들어 줘. 가볍고 재미있는 선화 스타일로 그리고 알맞은 음악을 넣어 몰입감 있게 완성해 줘. 자막은 한국어와 영어를 함께 넣고, 해설은 TTS로 만들어 줘. TTS API에 워터마크를 끄는 옵션이 있으면 사용해 줘. 문서는 TTS.md에 있고, API 키와 음성 설정은 각각 .env의 APIKEY와 VOICE에 있어. 완성 영상은 바로 내보낼 수 있어야 해.
```

</details>

### 10. 실사 설명 영상을 선화 애니메이션으로 변환

[원문](https://x.com/AxtonLiu/status/2102827887732932956) · [설명과 사용 방법](prompts/10-talking-head-to-lineart.md)

<details>
<summary>한국어 프롬프트 펼치기</summary>

```text
short-1.mp4를 새 세로형 짧은 영상 short-1-v5.mp4로 만들어 줘.

1. 내 얼굴 영상은 오른쪽 아래의 작은 원형 화면 속 화면으로 배치해 줘. 말하는 모습이 보이되 자막은 가리지 마.
2. 본 화면은 설명 내용에 맞는 애니메이션 B롤로 바꿔 줘. 내가 어떤 개념을 말하면 그 개념을 화면에 그려 줘. 가볍고 재미있는 선화 스타일로 만들고 실사처럼 만들지 마.
3. 원본 음성, 자막, 영상 길이는 그대로 유지해 줘.
```

</details>

### 11. 아우스터리츠 전투 역사 영화

[원문](https://x.com/WinterArc2125/status/2103116689944502720) · [설명과 사용 방법](prompts/11-austerlitz-film.md)

<details>
<summary>한국어 프롬프트 펼치기</summary>

```text
코드만으로 1805년 아우스터리츠 전투를 다룬 4~5분짜리 영화 같은 영상을 만들어 줘.

전투를 충분히 조사한 뒤 이야기 방식, 전개 속도, 전략 설명, 사건의 시각화를 스스로 결정해 줘. 역사적으로 정확하고 극적이며 이해하기 쉽고 시각적으로 뛰어나야 해.

첨부한 그림은 엄격한 스타일 지침이 아니라 시각적 영감으로 사용해 줘. 웅장한 규모, 분위기, 연기, 극적인 하늘, 기병대, 밀집 대형, 풍경, 혼돈이 마음에 들어. 그 느낌을 코드로 표현하되 더 강력한 시각 언어를 생각해 낼 수 있다면 그렇게 해 줘.

흔한 인포그래픽이나 전략 게임처럼 보이지 않게 해 줘. 코드로 렌더링했지만 역사 영화처럼 느껴져야 해.

창작 방향은 전적으로 맡길게. 놀라게 해 줘.
```

</details>

### 12. Remotion 앱 홍보 영상 1

[원문](https://dannystuart.substack.com/p/claude-code-opus-remotion-agentic-promo-video) · [설명과 사용 방법](prompts/12-remotion-app-promo-1.md)

<details>
<summary>한국어 프롬프트 펼치기</summary>

```text
가상의 디자이너용 Git 시각 관리 앱을 홍보하는 앱/SaaS 스타일 영상을 만들어 줘. […] 길이는 10~15초로 해 줘. 강렬한 장면 전환과 역동적인 타이포그래피를 사용하고, 역동적인 Apple 스타일의 밝은 영상으로 만들어 줘. […] 코드를 작성하기 전에 스토리보드를 만들고 신중하게 계획해 줘.
```

</details>

### 13. Remotion 앱 홍보 영상 2

[원문](https://dannystuart.substack.com/p/claude-code-opus-remotion-agentic-promo-video) · [설명과 사용 방법](prompts/13-remotion-app-promo-2.md)

<details>
<summary>한국어 프롬프트 펼치기</summary>

```text
앞서 만든 Twig 홍보 영상과 비슷한 수준의 영상을 만들고 싶어. […] Vanta Supply 계열 제품인 Glass Materials를 홍보해 줘. […] 길이는 15초로 해 줘. 강렬한 장면 전환과 역동적인 타이포그래피, 입자가 느껴지는 그러데이션이 있는 어두운 스타일을 사용해 줘. […] 코드를 작성하기 전에 스토리보드를 만들고 신중하게 계획해 줘.
```

</details>

### 14. 실제 자산을 사용하는 SaaS 출시 영상

[원문](https://community.startuptalky.com/discussions/post/opus-5-5-is-very-good-at-creating-videos-this-is-the-prompt-i-used-i-f6nYoYyvteUj6bd) · [설명과 사용 방법](prompts/14-saas-launch-real-assets.md)

<details>
<summary>한국어 프롬프트 펼치기</summary>

```text
fatjoe.com/grow를 위한 매우 전문적인 SaaS 제품 출시 영상을 만들어 줘. 사람들이 알아볼 만한 SaaS 제품 하나를 찾아 참고 대상으로 삼아 줘. 인터넷에서 실제 이미지와 자산을 찾아 사용해 줘. 새로운 SaaS를 출시할 때 소셜 미디어에서 볼 수 있는 세련된 모션 그래픽 제품 영상처럼 기능과 이점을 보여 줘. fatjoe 브랜드를 사용해 줘. […]
```

</details>

### 15. UI 변형 무한 반복 영상

[원문](https://x.com/twoclipping/status/2103273003555402193) · [설명과 사용 방법](prompts/15-ui-morph-loop.md)

<details>
<summary>한국어 프롬프트 펼치기</summary>

```text
<inputs>
다음 입력을 요청해 줘: 하나의 도형이 변할 UI 상태 8~12개(예: 버튼, 로더, 플레이어, 슬라이더, 토글, 탭, 차트, 명령 팔레트, 토스트), 순수 흑백 또는 강조색 한 가지, 120 BPM 안팎의 저작권료 없는 음악(예: 상업적 이용이 가능한 Mixkit 음악).
</inputs>

<direction>
Dribbble 수준의 UI 모션. 하나의 도형을 컷 없이 계속 변형한다. 각 상태는 같은 요소의 크기, 모서리 반경, 색을 바꾸고 내용은 짧은 흐림 효과와 함께 교체한다. 커서는 실제 클릭과 드래그로 모든 변화를 일으킨다. 밝고 따뜻한 회색 배경, 흑백 컴포넌트, 깔끔한 UI 글꼴 하나(Geist)를 사용한다. 곳곳에 스프링 동작을 넣되 초과 움직임은 아주 작게 한다. 각 상태가 화면을 채우도록 카메라를 확대한다. 마지막 프레임을 첫 프레임과 같게 만들어 반복한다.
금지: 과도하게 튀는 가속, 입자 폭발, 발광, UI 장식의 그러데이션, 제각각인 아이콘 선 굵기, 변화 없는 구간, 템플릿처럼 보이는 요소.
</direction>

<structure>
120 BPM, 7마디. 매 박자마다 사건이 일어난다.
버튼 → 로더 → 완료 표시 → 다이내믹 아일랜드 → 재생/일시정지 모양이 변하는 음악 플레이어 → 진행 막대 탐색 → 끝을 넘어 드래그하면 늘어나는 음량 슬라이더 → 박자에 맞춰 켜지는 토글 → 액체처럼 움직이는 탭 표시기로 바뀌는 손잡이 → 스스로 그려지는 차트로 펼쳐지는 탭과 마우스 오버 툴팁 → ⌘K로 접힘 → 필터 검색어 입력 → Enter → 토스트 → 처음 버튼으로 복귀.
</structure>

<build>
1. 1440×1440 단일 HTML 파일. 모든 스타일을 seek(t) 함수의 시간값으로 계산한다. CSS 전환, 타이머, 프레임 간 상태 저장은 사용하지 않는다.
2. 스프링은 닫힌 형태의 계단 응답으로 계산한다. 목표값이 여러 번 바뀌면 변화마다 스프링 하나를 더해 시간의 순수 함수로 유지한다.
3. 탭 표시기의 양쪽 끝에 서로 다른 스프링을 적용해 앞쪽 끝이 뒤쪽보다 먼저 늘어나게 한다. 토글 손잡이에도 같은 기법을 사용한다.
4. 드래그는 직접 조작으로 구현한다. 커서를 누르고 있는 동안 위치에서 값을 계산하고, 놓으면 그 지점에서 스프링으로 되돌린다.
5. numpy로 음악을 분석해 박자표를 만들고 강박에서 시작한다. UI 효과음은 측정한 소리의 정점에 맞춰 배치한다.
6. Playwright로 프레임마다 하위 프레임 4개를 렌더링하고 FFmpeg tmix로 혼합해 60fps 모션 블러를 만든다.
7. 전체 렌더링 전에 박자마다 한 프레임씩 출력해 박자에서 벗어나거나 비좁거나 읽기 어려운 부분을 수정한다.
</build>

<gotchas>
카메라가 확대하는 요소에 will-change를 설정하지 마라. 글자가 흐려진다. 변형되는 컨테이너 안의 글자를 바꿀 때는 등장과 퇴장 시점을 따로 잡아 겹침을 막아라. 반복 구간이 끊기지 않도록 커서의 위치와 속도까지 마지막 프레임을 첫 프레임과 같게 만들어라.
</gotchas>

<start>
코드를 작성하기 전에 입력값을 물어보고 박자표 위에 상태 목록을 보여 줘.
</start>
```

</details>

### 16. 고급 미니멀 제품 영상

[원문](https://youmind.com/video-prompts/high-end-product-video-prompt-11292) · [설명과 사용 방법](prompts/16-high-end-product-video.md)

<details>
<summary>한국어 프롬프트 펼치기</summary>

```text
<inputs>
제품 이름과 한 줄 약속, 보여 줄 UI 순간 3~5개, 강조색 하나, 내가 소유한 실제 세로 영상 10~20개, 뚜렷한 드롭이 있는 저작권료 없는 음악(예: 상업적 이용이 가능한 Mixkit 음악)을 요청해 줘.
</inputs>
<direction>
고급스러운 미니멀 스타일. 한 장면에 한 가지 생각만 담고 여백을 넉넉히 둔다. 강조색 하나와 자간을 좁힌 깔끔한 산세리프 글꼴 하나(Geist 또는 Inter)를 사용한다. 마스크로 글자가 드러나고, 동작을 이어 붙이는 매치 컷과 일관된 카메라 움직임을 사용한다. 실제 촬영 영상만 사용하고 임시 카드 화면은 쓰지 않는다. 화면 글자 끝에는 마침표를 넣지 않는다.
금지: 충격파 고리, 입자 폭발, RGB 분리, 카메라 흔들림, 렌즈 플레어, 네온 발광, 격자 바닥, 깜박이는 배경, 튀는 가속.
</direction>
<structure>
120 BPM에서 10마디, 마디당 2초.
1마디: 시선을 끄는 문구가 박자마다 한 단어씩 나타난다.
2마디: 문구의 한 단어가 제품 UI로 변형되고 커서가 입력하고 클릭한다.
드롭: 버튼에서 원이 확장되며 어두운 장면으로 전환된다.
이후 마디마다 한 가지 동작: 실제 영상의 벽과 스캔 라인, 선택된 영상 3개 → 핵심 결과를 큰 글자로 표시 → 바닥 반사가 있는 실제 영상의 3D 회전 목마와 모션 블러가 걸린 빠른 카메라 전환 → 휴대전화 속 대표 영상과 결과 화면으로 뒤집히는 패널 → 빠른 컷에 맞춘 큰 통계 → 세 단어 티커 → 로고 공개 → 검은 화면으로 페이드아웃.
</structure>
<build>
1. 1920×1080 단일 HTML 파일. 모든 스타일은 seek(t)의 시간값으로 계산한다. CSS 애니메이션, 타이머, 프레임 간 상태 저장은 금지한다.
2. 실제 영상은 FFmpeg로 30fps JPEG 시퀀스로 추출하고 프레임마다 img 소스를 교체한다. seek는 이미지 디코딩이 끝날 때까지 기다린다.
3. numpy로 음악의 템포, 박자표, 마디별 에너지와 드롭을 분석한다. 실제 킥 소리에 맞춰 박자표를 보정한다. 모든 컷은 강박에, 모든 UI 동작은 박자에 배치한다.
4. Playwright로 각 프레임의 t-1/240초, t, t+1/240초 하위 프레임 3개를 렌더링한 뒤 FFmpeg tmix로 혼합해 60fps 모션 블러를 만든다.
5. 각 효과음의 파일 시작점이 아니라 측정한 소리의 정점이 사건에 맞도록 배치한다. 효과음은 음악보다 작게 유지한다. loudnorm으로 -14 LUFS에 맞춘다.
6. 전체 렌더링 전에 최소 20프레임을 검사하고 복잡하거나 겹치거나 읽기 어려운 부분을 수정한다.
</build>
<gotchas>
preserve-3d 요소에 opacity나 filter를 설정하면 평면화되어 앞뒷면이 함께 보이므로 래퍼에 페이드를 적용하라. 매치 컷에는 실행 중 측정한 요소 위치를 사용하라. 음악과 효과음은 상업적 이용이 허용된 것만 사용하라.
</gotchas>
<start>
코드 작성 전에 입력값을 물어보고 모든 시점을 박자표에 맞춘 스토리보드를 보여 줘.
</start>
```

</details>

### 17. 주문을 시전하는 픽셀 마법사

[원문](https://x.com/majidmanzarpour/status/2102476499387383834) · [설명과 사용 방법](prompts/17-pixel-wizard.md)

<details>
<summary>한국어 프롬프트 펼치기</summary>

```text
외부 자산, 라이브러리, 네트워크 요청 없이 순수 JavaScript와 Canvas 2D만으로 주문을 시전하는 픽셀 마법사 애니메이션을 구현한 단일 HTML 파일을 만들어 줘.

렌더링
- 고정 논리 해상도 128×96의 화면 밖 캔버스에 모두 그린 뒤 창에 맞는 최대 정수 배율로 확대해 중앙의 전체 화면 캔버스에 복사한다. imageSmoothingEnabled = false와 CSS image-rendering: pixelated를 적용한다.
- 모든 그림은 논리 캔버스의 정수 좌표에 맞춘다. 부분 픽셀 위치, 안티앨리어싱, 그러데이션, shadowBlur는 사용하지 않는다.
- 밤하늘의 진한 파랑과 보라, 따뜻한 로브 색, 밝은 마법 색 3~4개를 포함한 약 24개 16진수 색상으로 고정 팔레트를 만든다. 모든 픽셀은 이 팔레트에서 고른다.

캐릭터
- 채운 사각형과 픽셀 줄로 약 24×32 논리 픽셀의 마법사를 절차적으로 그린다. 휘어진 뾰족 모자, 긴 수염, 진한 외곽선이 있는 두 가지 색조의 로브, 끝에 보석이 달린 지팡이를 포함한다.
- 지팡이 각도, 팔 높이, 고개 기울기, 로브 흔들림을 매개변수로 만든다. 매개변수는 부드럽게 움직이되 프레임마다 픽셀 격자에 맞춰 양자화한다. 반복 루프가 60fps여도 8~12fps 픽셀 애니메이션처럼 보이게 한다.

애니메이션
- 반복 상태 기계: 대기(2프레임 상하 움직임과 수염 흔들림) → 충전(지팡이를 들고 보석이 깜박이며 불꽃이 안쪽으로 나선 이동) → 시전(밝은 폭발과 화면을 가로지르는 발사체, 1~2픽셀 화면 흔들림) → 회복(원래 자세로 돌아옴). 핵심 자세 사이 매개변수를 부드럽게 보간한다.
- 할당 없는 재사용 입자 풀을 미리 만든다. 충전 중 불꽃은 보석을 돌고, 시전 중 바깥으로 퍼진다. 입자는 흰색에서 마법 색, 어두운 색 순으로 팔레트 인덱스를 바꾼 뒤 사라진다. 그릴 때 위치를 픽셀 격자에 맞춘다.
- 고정 60Hz 시간 간격으로 갱신하고 requestAnimationFrame으로 렌더링한다. 반복 루프 안에서는 객체를 할당하지 않는다.

장면
- 어두운 하늘, 반짝이는 1픽셀 별 몇 개, 달, 돌바닥 선만 있는 간결한 배경. 캐릭터의 실루엣이 분명해야 한다.
- 보석에서 마법사 쪽으로 은은한 1픽셀 윤곽광을 비추고 충전과 시전 때 밝게 한다.

품질 기준
- 창 크기에 관계없이 선명한 픽셀, 끊기지 않는 반복, 안정적인 60fps, 알아보기 쉬운 실루엣. 확대된 벡터 도형이 아니라 완성도 높은 16비트 스프라이트 애니메이션처럼 보여야 한다.
```

</details>

### 18. 상호작용하는 선사 시대 섬

[원문](https://x.com/vib3coded/status/2102450842070569099) · [설명과 사용 방법](prompts/18-prehistoric-island-threejs.md)

<details>
<summary>한국어 프롬프트 펼치기</summary>

```text
Three.js와 WebGL로 아름답고 세부 묘사가 풍부하며 완전히 상호작용할 수 있는 3D 선사 시대 섬을 만들어 줘. Chrome에서 바로 열 수 있는 단일 HTML 파일로 제공하고 가능한 자산은 파일 안에 포함해 줘.

시각적 방향
투명한 수중 단면이 보이는 바다로 둘러싸인 크고 둥근 섬을 만들어 줘. 무성한 식물, 생동감 있는 공룡, 풍부한 재질, 분위기 있는 조명, 매끄러운 애니메이션으로 고급 미니어처 세계처럼 보여야 해. 단순한 기하학적 모양 대신 일관된 스타일을 적용해 줘.

섬
해변, 바위 절벽, 울창한 선사 시대 숲, 거대한 양치식물, 폭포, 민물 연못, 화산을 넣어 다양한 지형을 만들어 줘. 작은 연구 기지, 나무 산책로, 관찰대, 보급 상자, 공룡 둥지도 추가해 줘. 공룡이 서로 다른 구역을 자연스럽게 오갈 만큼 넓게 만들어 줘.

물의 단면
섬 주변 바다는 깊고 둥근 부피감을 가져야 하며 측면을 통해 수중 풍경이 또렷이 보여야 해. 질감 있는 해저, 바위, 수생 식물, 물고기, 기포, 수면 아래를 헤엄치는 초록색 해양 파충류를 넣어 줘. 육지 공룡을 물속에 넣거나 잠수함을 추가하지 마.
애니메이션 파도, 프레넬 반사, 수중 빛무늬, 해안 거품, 물보라를 넣어 줘. 투명도 정렬 오류와 섬과 바다 사이의 틈이 보이지 않게 해 줘.

공룡
목이 긴 용각류, 트리케라톱스, 스테고사우루스, 큰 수각류, 작은 무리 동물 등 구별되는 여러 종을 포함해 줘. 하늘에는 익룡이 선회하게 해 줘.
각 종의 해부학적 특징이 드러나도록 몸체, 관절이 있는 팔다리, 세부 묘사가 있는 머리와 꼬리, 적절한 피부 무늬를 만들어 줘. 뻔한 상자나 분리된 구체를 이어 붙인 완성형 공룡은 피해야 해.

자연스러운 애니메이션
관절 위치가 정확한 계층형 골격을 사용해 줘. 걸음은 지지 단계와 다리를 들어 옮기는 단계를 구분해야 해. 땅을 딛는 동안 발은 고정되고 매 걸음마다 분명히 들려야 해. 보폭은 이동 속도에 맞춰 줘.
지형 높이 샘플링과 역운동학으로 발을 땅에 붙여 줘. 체중 이동, 미세한 몸 움직임, 균형 잡힌 꼬리 움직임, 고개 돌리기, 호흡도 넣어 줘. 공룡이 뜨거나 미끄러지거나 땅을 뚫거나 건물, 바위, 나무, 다른 공룡을 통과하면 안 돼.
장애물을 피하고 안전한 경로로 움직여 줘. 종마다 이동 속도, 걸음걸이, 행동이 달라야 해. 해양 동물은 이동 방향을 바라봐야 해.

상호작용
사용자가 다음 작업을 할 수 있게 해 줘.
- 카메라를 자유롭게 돌리고 확대하며 수중 단면을 관찰한다.
- 공룡을 선택하고 부드럽게 움직이는 카메라로 따라간다.
- 적절한 곳에 먹이를 놓고 주변 공룡이 다가와 먹는 모습을 본다.
- 마시기, 쉬기, 울기, 무리 이동을 실행한다.
- 둥지를 탐색하고 새끼가 부화하는 모습을 본다.
- 해양 파충류가 수면으로 올라오며 물보라를 일으키게 한다.
- 낮, 석양, 밤을 전환한다.
- 비, 바람, 화산 활동을 조절한다.
- 시뮬레이션을 일시정지하고 장면을 초기화한다.
모든 조작에 분명하고 눈에 보이는 반응을 제공해 줘. 상호작용을 반복할 수 있어야 하며 애니메이션이 겹쳐 캐릭터 자세가 망가지면 안 돼.

분위기와 오디오
흔들리는 나뭇잎, 흘러가는 구름, 새, 곤충, 빗방울, 밤에 켜지는 연구 기지의 따뜻한 조명을 넣어 줘. 잔잔한 배경 음악과 환경음을 추가하고 실제로 작동하는 음악 전환 버튼과 음량 슬라이더를 제공해 줘. 사용자가 상호작용한 뒤에만 오디오를 시작해 줘.

인터페이스
한국어 레이블을 쓰는 간결하고 세련된 인터페이스를 만들어 줘. 큰 패널이 섬을 가리지 않도록 장면을 중심에 두고 데스크톱과 모바일에 반응하도록 해 줘.

기술적 품질
반복되는 식물과 소품에는 인스턴싱을 쓰고 효율적인 지오메트리, 적절한 그림자, 절제된 후처리를 적용해 줘. 시각적 풍부함과 실시간 성능 사이의 균형을 맞춰 줘.
모형이 아닌 완성된 장면을 만들어 줘. 최종 HTML을 데스크톱 브라우저에서 직접 열고 스크린샷과 콘솔을 확인하며 모든 상호작용을 시험해 줘. 전달 전 로딩 오류, 공중에 뜬 공룡, 발 미끄러짐, 충돌 오류, 물 표현 문제, 카메라 문제를 고쳐 줘.
```

</details>

## 제작 방식

| 방식 | 주요 도구 | 해당 사례 |
|---|---|---|
| 단일 HTML과 Canvas로 프레임 그리기 | JavaScript, Canvas 2D, Web Audio, Playwright/Puppeteer, FFmpeg | 픽셀 마법사, 네그로니, UI 변형 |
| p5.js로 손그림풍 애니메이션 | p5.js, p5.brush, 헤드리스 Chrome, FFmpeg | P(doom), 《Let Me Go》, Opus의 일생 |
| Remotion으로 영상 구성 | React, TypeScript, SVG, Canvas, Remotion Studio | AI 발전사, 앱 홍보 영상 |
| HyperFrames로 HTML 영상 렌더링 | HyperFrames, 단일 HTML, Python 음악 합성 | Shotbase, Small Print |
| Manim으로 수학·논문 설명 | Manim, Kokoro-82M TTS, FFmpeg | 연구 논문 애니메이션 설명 |
| Python으로 선화 프레임 그리기 | Python, Pillow, TTS, FFmpeg | 대기 대순환, 실사 설명 영상 변환 |
| Three.js와 WebGL로 3D 장면 만들기 | Three.js, 절차 생성 모델·재질·음향 | 아우스터리츠 전투, 선사 시대 섬, 안티키테라 기계 |
| 전문 영상 도구 조작 | After Effects, Blender, Higgsfield, Runway MCP, Seedance API | 출시 광고, Blender 장면, 다큐멘터리 |
| 기존 영상 편집 | browser-use, video-use, FFmpeg | 원본 영상 13개를 엮은 출시 영상 |

## 사례 목록

공개 사례 53건이다. `—`는 원 게시물에 정보가 없다는 뜻이다. 기계가 읽을 수 있는 데이터는 [cases.json](cases.json)에 있다.

| 분류 | 사례 | 작성자 | 제작 방식·특징 | 시간·비용 |
|---|---|---|---|---|
| 제품 광고 | [추론 스타트업 출시 영상](https://x.com/deedydas/status/2102787937482252537) | Deedy | 한 문장으로 요청하고 도구 선택은 모델에 맡김 | 1분, 약 2달러 |
| 제품 광고 | [웹사이트 개편안을 엮은 예고편](https://x.com/trq212/status/2102477340920152162) | trq212 | 여러 웹사이트 개편안을 검토한 뒤 예고편으로 엮음 | — |
| 제품 광고 | [Shotbase 제품 출시 영상](https://x.com/Miguel07Code/status/2102441708395041170) | Miguel07Code | Opus 5.5와 HyperFrames 사용 | — |
| 제품 광고 | [수정 가능한 After Effects 출시 광고](https://x.com/seiiiiiiiiiiru/status/2102636308707287201) | SEIIIRU | Claude가 Higgsfield와 After Effects를 조작하며 프로젝트 파일을 계속 수정할 수 있음 | Pro 요금제 사용량 5%, 약 150엔 |
| 제품 광고 | [내레이션을 중심으로 한 After Effects 광고](https://x.com/seiiiiiiiiiiru/status/2103227982592831846) | SEIIIRU | Gemini 3.8 Flash TTS로 내레이션을 만들고 Claude가 화면, 음악, 효과음을 배치 | — |
| 제품 광고 | [BLVCKOUT 비공식 광고](https://x.com/ystknsh/status/2102766871007436993) | ystknsh | MulmoCast로 제작하고 Opus가 대본과 애니메이션, Gemini가 이미지와 음성, ElevenLabs가 음악을 담당 | — |
| 제품 광고 | [Mole 제품 홍보 영상](https://x.com/berryxia/status/2103419787565216023) | Berryxia | 제품 정보를 넣으면 홍보 영상을 만드는 재사용 스킬로 구성 | — |
| 제품 광고 | [앱 홍보 영상 두 편](https://dannystuart.substack.com/p/claude-code-opus-remotion-agentic-promo-video) | Danny Stuart | Remotion으로 스토리보드를 먼저 만든 뒤 코드를 작성 | 편당 약 10분 |
| 제품 광고 | [립밤 광고: GPT-6 Astra와 비교](https://x.com/higgsfield_ai/status/2102913101926731879) | Higgsfield AI | 같은 브랜드 자산으로 After Effects에서 20초 제품 영상을 제작 | — |
| 제품 광고 | [30초 기업 설명 영상 템플릿](https://x.com/alex_prompter/status/2103499977632997524) | Alex Prompter | 단일 HTML 파일의 5개 장면을 대화에서 재생하고 녹화 | — |
| 모션 그래픽 | [15초 모션 디자인 쇼릴](https://x.com/stephanlivera/status/2103315922098470926) | Stephan Livera | Max 추론 강도에서 한 문장으로 요청 | — |
| 모션 그래픽 | [끊김 없는 UI 변형 반복 영상](https://x.com/twoclipping/status/2103273003555402193) | zero | 상세 템플릿과 Playwright, FFmpeg tmix로 모션 블러 구현 | — |
| 과학·지식 설명 | [상호작용하는 카메라 렌즈 실험실](https://x.com/RyanSael/status/2102591147927654847) | Ryan Sael | 한 번에 완성된 상호작용 렌즈 시뮬레이션 | 1시간 26분, API 비용 25.66달러 |
| 과학·지식 설명 | [연구 논문 애니메이션 설명](https://x.com/deedydas/status/2103141339651350646) | Deedy | Claude가 Manim, Kokoro-82M, FFmpeg를 선택해 웹 대화에서 완성 | — |
| 과학·지식 설명 | [AI 발전사 3분 영상](https://x.com/kimmonismus/status/2102844654169575547) | Chubby (kimmonismus) | React/TypeScript 약 7,400줄, Remotion, SVG/Canvas, 오픈소스 TTS, Python 음악 | 약 1시간, 주간 한도의 7% |
| 과학·지식 설명 | [대기 대순환 설명 영상](https://x.com/akokoi1/status/2102606609574941028) | WY | 선화, TTS 내레이션, 이중 자막 | 26분, 토큰 사용량 적음 |
| 과학·지식 설명 | [물리 경시대회 어려운 문제 설명](https://x.com/akokoi1/status/2102680453912449223) | WY | 대기 대순환 프롬프트의 주제를 구체적인 문제로 교체 | — |
| 과학·지식 설명 | [네그로니 칵테일 레시피 애니메이션](https://x.com/Ror_Fly/status/2102853258582880547) | Rory Flynn | 참고 이미지 한 장으로 30초 HTML 애니메이션 제작 | — |
| 과학·지식 설명 | [46초 특수상대성이론 설명: 일본어](https://x.com/masahirochaen/status/2102722719502704941) | チャエン | 참고 게시물과 짧은 지시로 Canvas 1,395프레임 제작, 음악과 효과음도 JavaScript로 생성 | 렌더링 약 2분 |
| 과학·지식 설명 | [아우스터리츠 전투 영화](https://x.com/WinterArc2125/status/2103116235009347650) | Winter | WebGL과 Kokoro 내레이션 사용, 코드 공개 | — |
| 과학·지식 설명 | [실사 설명 영상을 선화 애니메이션으로 변환](https://x.com/AxtonLiu/status/2102827887732932956) | Axton | Python으로 약 30개 장면을 프레임마다 그리고 원음과 자막 유지 | 28분 53초, 수동 개입 없음 |
| 과학·지식 설명 | [Transformer 설명 영상](https://youmind.com/opus-5-5-prompts) | 바오위 | JavaScript로 영상 제작 | — |
| 과학·지식 설명 | [방에서 쿼크까지 확대](https://youmind.com/opus-5-5-prompts) | Taelin | 여러 크기 단계를 잇는 연속 카메라 이동 | — |
| 서사 애니메이션 | [당신이 사랑하는 것은 무엇인가?](https://x.com/kevin_t_ngo/status/2102437977435893771) | Kevin Ngo | JavaScript로 프레임마다 손그림풍 애니메이션 제작 | — |
| 서사 애니메이션 | [픽셀 마법사](https://x.com/majidmanzarpour/status/2102476258948927543) | Majid Manzarpour | 순수 JavaScript와 Canvas 2D로 만든 단일 HTML 파일 | — |
| 서사 애니메이션 | [화성 탐사선 단편](https://x.com/AndrewOnXYZ/status/2102512879258009818) | AndrewOnXYZ | 코드로 렌더링한 단편 영상 | — |
| 서사 애니메이션 | [Opus의 일생](https://x.com/shfred0/status/2102495989194236158) | shfred0 | Claude가 자신의 탄생부터 현재까지를 이야기하고 JavaScript로 프레임마다 그림 | — |
| 서사 애니메이션 | [어려운 문제 해결을 상상하기](https://x.com/chetaslua/status/2102478640428773861) | chetaslua | 코드 애니메이션 | — |
| 서사 애니메이션 | [Small Print: 글자 사이의 의미](https://x.com/Voxyz_ai/status/2102531681450119426) | Vox | 단일 index.html을 HyperFrames로 렌더링하고 Python으로 음악을 합성, 매초 검토 | — |
| 서사 애니메이션 | [맥주 축제 30초 애니메이션](https://x.com/cherry_mx_reds/status/2102493303388475855) | Tak | 캐릭터 스크린샷과 로컬 오디오 샘플 사용 | — |
| 서사 애니메이션 | [빗방울 하나의 이야기](https://x.com/aollivier82/status/2102498589259821559) | aollivier82 | 코드 애니메이션 | — |
| 서사 애니메이션 | [엄마를 찾는 올챙이: 수묵화](https://x.com/akokoi1/status/2102699703309898026) | WY | 수묵화풍 코드 애니메이션 | — |
| 서사 애니메이션 | [Rain Station 30초 2D 스토리보드 영상](https://youmind.com/opus-5-5-prompts) | Feicai | 2D 애니메이션 스토리보드 미리보기 | — |
| 예술·3D | [궤도 속 세계](https://x.com/devteamdrew/status/2102436464323661880) | devteamdrew | 순수 JavaScript 애니메이션 | — |
| 예술·3D | [안티키테라 기계의 해저 탐험](https://x.com/edwinarbus/status/2102463453176979794) | edwin | Three.js로 물고기 2,047마리, 풀잎 2만 5천 개, 입자 4만 7천 개, 톱니바퀴 30개 구현 | — |
| 예술·3D | [투석기 스케치를 상호작용 시뮬레이션으로 변환](https://x.com/poolio/status/2102445641205248145) | poolio | 스케치에서 물리 시뮬레이션 생성 | — |
| 예술·3D | [무지개 길 픽셀 달리기](https://x.com/riku720720/status/2102515055116063144) | Rikuo | 매우 긴 일본어 상세 사양 프롬프트 | — |
| 예술·3D | [움직이는 해안 그림](https://x.com/strawhatsu4/status/2102457111787745405) | strawhatsu4 | 코드로 그린 회화 애니메이션 | — |
| 예술·3D | [아크릴화풍 뉴질랜드 여행기](https://x.com/ann_nnng/status/2102573127192727704) | Ann Nguyen | 여행 사진을 아크릴화풍으로 바꾸고 JavaScript로 그림 | — |
| 예술·3D | [Blender 외골격·풍차·안구 해부](https://x.com/higgsfield_ai/status/2102449278283313303) | Higgsfield AI | Claude가 Blender를 조작해 모델링과 애니메이션 제작 | — |
| 예술·3D | [Blender 절차 생성 10초 장면](https://x.com/Stefan_3D_AI/status/2102471841046786153) | Stefan 3D AI | Blender만 사용해 절차적으로 제작하고 작업 과정 타임랩스도 녹화 | 35분, 출력 토큰 19만 9,600개, 약 13.3달러 |
| 예술·3D | [상호작용하는 선사 시대 섬](https://x.com/vib3coded/status/2102450842070569099) | Vib3Coded | Three.js로 만든 단일 HTML 파일 | — |
| 뮤직비디오 | [I'm Upping My P(doom)](https://github.com/JohnHeibel/PDoomVideo) | NotinReality / JohnHeibel | p5.js와 p5.brush로 그리고 헤드리스 Chrome으로 캡처해 FFmpeg로 합성, 156.6초 약 3,760프레임, 2회 시도 | Max 5x 주간 한도의 10% |
| 뮤직비디오 | [《Let Me Go》 애니메이션 뮤직비디오](https://linux.do/t/topic/2943096) | Linux.do 이용자 | 가사와 오디오를 올리고 xhigh 추론 강도로 p5.js 프레임 작업, 사람의 피드백으로 캐릭터 수정 | 초안 45분, 약 200달러 |
| 뮤직비디오 | [Claude Pop 혼합 제작 뮤직비디오](https://x.com/donaldjewkes/status/2102801274173587569) | donald | fal 캐릭터 이미지, Seedance 2.5 영상, JavaScript 프레임별 재그리기 | fal 예산 약 2,000달러 |
| 뮤직비디오 | [Suno 작곡과 Opus 작사 뮤직비디오](https://www.bilibili.com/video/BV1qihf6rE6f/) | Bilibili 크리에이터 | Suno가 편곡·노래하고 Opus 5.5가 작사·뮤직비디오 제작 | — |
| 뮤직비디오 | [EVA풍 세로 가사 영상](https://youmind.com/opus-5-5-prompts) | kurahu | 가사를 주인공으로 삼은 세로형 뮤직비디오 | — |
| 다큐·편집 | [5분 초지능 다큐멘터리](https://x.com/gavinpurcell/status/2103304514329854102) | Gavin Purcell | Runway MCP를 연결해 일반 대중을 위한 Netflix풍 다큐멘터리 제작 | — |
| 다큐·편집 | [원본 영상 13개를 엮은 출시 영상](https://x.com/gregpr07/status/2102984873351037161) | gregpr07 | video-use로 장면을 골라 편집, 색보정, 자막 작업 | — |
| Bilibili 모음 | [지구 46억 년 진화사](https://www.bilibili.com/video/BV1Vfau6iE9Q/) | Bilibili 크리에이터 | 코드 애니메이션 | — |
| Bilibili 모음 | [군론의 아름다움 홍보 영상](https://www.bilibili.com/video/BV12Zhm6oE6m/) | Bilibili 크리에이터 | 코드 애니메이션 | — |
| Bilibili 모음 | [벤치에 앉아 핵폭발을 보는 애니메이션](https://www.bilibili.com/video/BV1jyaA6QEoH/) | Bilibili 크리에이터 | 코드 애니메이션 | — |
| Bilibili 모음 | [한 문장으로 만든 뮤직비디오](https://www.bilibili.com/video/BV1EDhW6LEYU/) | Bilibili 크리에이터 | 한 문장으로 뮤직비디오 제작 | — |

## 프롬프트 작성 요령

- **스토리보드를 먼저 만든다.** 장면이나 박자표를 확인한 뒤 코드를 작성하면 특정 장면만 다시 수정하기 쉽다.
- **시간과 장면을 구체적으로 적는다.** 총 길이, 장면 수, 각 장면의 메시지, 참고 영상이나 이미지를 제공한다. 매치 컷이나 역동적인 타이포그래피처럼 원하는 영상 문법도 명시한다.
- **피하고 싶은 효과를 적는다.** 입자 폭발, RGB 분리, 렌즈 플레어, 네온 발광, 튀는 움직임 등 원치 않는 요소를 분명히 한다.
- **프레임을 시간의 함수로 만든다.** `seek(t)`로 모든 시각 상태를 결정하면 임의 시점의 프레임을 안정적으로 렌더링할 수 있다. CSS 전환과 타이머, 이전 프레임의 상태에 의존하는 구현은 피한다. [PDoomVideo 애니메이션 가이드](https://github.com/JohnHeibel/PDoomVideo/blob/main/ANIMATION_GUIDE.md)를 참고할 수 있다.
- **전체 렌더링 전에 대표 프레임을 검사한다.** 글자 겹침, 화면 밀도, 가독성, 박자 정렬을 고친다.
- **사용할 도구와 자산을 준비한다.** TTS나 영상 모델을 쓴다면 해당 API 문서를 먼저 확인한다. 인증 정보는 프롬프트에 붙이지 말고 별도로 안전하게 관리한다.

## 한계와 비용

- 코드 기반 렌더링은 주로 모션 그래픽이며 실제 촬영 영상과 결과가 다르다.
- MP4를 만들려면 로컬 렌더링 환경이 필요할 수 있다.
- 비용 차이가 크다. 짧은 영상은 몇 달러였다는 사례가 있지만, 몇 분짜리 뮤직비디오는 한 세션에 200달러가 들었다는 사례도 있다.
- 한 번에 완성했다고 소개된 영상도 여러 차례 수정했을 수 있으므로 반복 작업을 고려해 예산을 잡는다.

## 출처

- [awesome-claude-video 사례 모음](https://github.com/opusvideo/awesome-claude-video)
- [YouMind의 Claude Opus 5.5 프롬프트 모음](https://youmind.com/opus-5-5-prompts)
- [Danny Stuart의 Claude Code와 Opus 영상 제작 글](https://dannystuart.substack.com/p/claude-code-opus-remotion-agentic-promo-video)
- [OrcaRouter의 영상 계획 사례 분석](https://www.orcarouter.ai/blog/claude-opus-5-5-video-plan-one-shot)
- [SlopTV의 네그로니 HTML 영상 사례](https://sloptvnews.com/opus-5-5-negroni-explainer-html-motion-graphics-iteration/)
- [80aj의 Opus 애니메이션 뮤직비디오 소개](https://www.80aj.com/2026/09/25/claude-opus-animation-mv/)
- [Sina Tech의 Opus 5.5 실험 기사](https://finance.sina.com.cn/tech/roll/2026-09-25/doc-inisyuqm4676290.shtml)
- [Linux.do의 프레임별 애니메이션 뮤직비디오](https://linux.do/t/topic/2943096)
- [PDoomVideo 저장소](https://github.com/JohnHeibel/PDoomVideo)
- [Battle-of-Austerlitz-Film 저장소](https://github.com/WinterArc21/Battle-of-Austerlitz-Film)
- [riba2534의 Claude Opus 5.5 3D 게임 예제](https://github.com/riba2534/claude-opus-5-5-demo)

## 기여

새 사례를 제안할 때는 원저작자가 공개한 프롬프트와 원 게시물 링크를 함께 제공해 주세요. 번역 오류 수정도 환영합니다.

## 저작권과 삭제 요청

프롬프트와 영상의 저작권은 각 원저작자에게 있습니다. 이 저장소는 사례를 정리하고 한국어 번역을 제공합니다. 원저작자가 수록을 원치 않으면 이슈를 남겨 주세요.

---

원자료 정리: [샹양차오무](https://github.com/joeseesun) · 2026-09-27
