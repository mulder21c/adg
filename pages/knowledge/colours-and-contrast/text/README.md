---
navigation_title: "텍스트에 대한 색상 대비"
position: 3
changed: "2019-12-15"
---

# 텍스트에 대한 색상 대비

**모든 종류의 텍스트에 대해 일반적인 최소 색상 대비 수준이 있습니다. 예외적으로, 큰 텍스트는 낮은 대비를 가질 수 있습니다. 이 요구 사항은 "실제" 텍스트와 이미지의 래스터화 된 텍스트 모두에 적용됩니다.**

## 최소 명암비

웹 콘텐츠 접근성 지침(WCAG)은 [일반적으로 텍스트에 대해 인접한 색상에 `4.5:1`의 최소 명암비](https://www.w3.org/TR/WCAG21/#contrast-minimum)를 지정합니다. 큰 글씨 텍스트에는 예외가 있습니다: 그것은 읽기 쉬운 것으로 간주되므로 적어도 `3:1`의 낮은 명암비를 설정할 수 있습니다.

큰 글씨 텍스트는 다음과 같이 정의됩니다:

- 적어도 14 포인트 (또는 18.5 픽셀)의 **굵은** 텍스트.
- 또는 18 포인트 (또는 24 픽셀)의 일반 텍스트.

더 자세한 정보는 [WCAG "큰 글씨 (텍스트)"의 정의](https://www.w3.org/TR/WCAG21/#dfn-large-scale)를 참고하세요.

이를 설명하기 위해: 다음 이미지는 흰 색 배경에 쓰여진 "빠른 갈색 여우가 게으른 개를 뛰어넘는다"라는 문장을 보여줍니다. 43글자를 가지고 있습니다. 첫 번째 문자 "T"는 흰색입니다. 다음 문자의 색상은 서서히 어두워지고, 마지막 글자 "g"는 완전히 검은색입니다. 

![색상 그라데이션 오버레이가 있는 텍스트](_media/lazy-dog.png)

"x"  (19번째 문자) 주변 어딘가의 명암비는 `3:1`에 도달합니다. "m" (23번째 문자) 주변 어딘가에서는 `4.5:1`에 도달합니다. 마지막 문자는 `21:1`의 최대 색상 명암비를 가집니다.

보다 직접적인 비교를 위해: 다음 이미지는 정확히 `3:1`과 `4.5:1`의 명암비를 가진 큰 텍스트와 기본 텍스트를 모두 보여줍니다.

![작은 글씨와 큰 글씨](_media/small-and-large-text.png)

큰 차이가 아닌 것 같아 보일 수 있지만, 실제로 가능한 색상 조합의 수를 크게 늘립니다.

`3:1`과 `4.5:1` 값이 **허용 가능한** 대비에 대한 **최소** 표준을 나타내며, 그것이 가장 알맞는다는 걸 나타내는 것이 아님을 언급하는 것이 중요합니다. 이는 목표가 아닌 임계 값으로 취급되어야 합니다; 더 높은 목표가 권장됩니다.

## 텍스트 대비 향상

텍스트의 색상이나 배경색을 변경하는 것 외에도 대비를 향상시키는 다른 많은 방법이 있습니다. 예를 들어:

### 그림자 추가

텍스트 주변의 그림자는 텍스트 색상과 배경 색상 사이의 불충분한 대비를 보완할 수 있습니다.

예를 들어, 다음 이미지를 보세요. 흰색 배경과 `2.1:1`의 불충분한 대비를 가진 빨간 색으로 채워진 두 단어가 있습니다.

![그림자가 없는 단어와 그림자가 있는 단어](_media/words-without-and-with-shadow.png)

두 번째 단어의 그림자는 적절하게 `4.5:1`의 대비를 만듭니다.

CSS로 이것은 `text-shadow: 0 0 5px #000`과 같은 것일 수 있습니다.

### 대비 레이어 추가

경우에 따라, 텍스트는 균일하지 않은 배경에 표시됩니다. 배경의 불균일에 따라 텍스트가 매우 읽기 어려울 수 있습니다.

예를 들어, 다음 이미지를 보세요. 흰 구름들이 있는 파란 하늘에 하얀 "Welcome to the beach!" 텍스트가 있습니다. 하얀 텍스트와 파란 하늘 사아에는 적절한 대비가 있지만 하얀 구름과 하얀 텍스트 사이에는 거의 대비가 없습니다. 전반적으로 읽기가 매우 어렵습니다.

![파란 하늘과 하얀 구름 위의 텍스트](_media/beach.png)

위에서 설명한 대로 텍스트 그림자를 추가하여 대비를 증가시킬 수 있습니다. 또는 텍스트와 배경 사이에 어두운 반투명 레이어를 추가할 수 있습니다.

![어두운 반투명 배경을 가진 하얀 텍스트](_media/beach-with-background.png)

물론 다른 해결책을 결합하여 효과를 추가할 수도 있습니다.

## 예외

텍스트 콘텐트의 대비 요구 사항에는 몇 가지 예외가 있습니다.

- **로고**는 일반적으로 기업 디자인 지침을 엄격하게 준수해야 하기 때문에 명암비에 관계 없이 해당 색상으로 표시 될 수 있습니다 (고객이 로고를 인식 할 수 없는 경우 여전히 불편하다는 것은 말할 필요도 없습니다).
- **장식용 텍스트:** 이것은 임의의 단어로 생성 된 이미지의 배경 패턴일 수 있습니다.
- **부수적인 테긋트:** 이것은 사진의 배경 어딘가에 임의의 겨리 표지판일 수 있습니다.
- **비활성화 된 텍스트:** 이것은 온라인 양식의 비활성화 된 엘리먼트의 레이블일 수 있습니다.

### 자리표시자 텍스트는?

WCAG의 텍스트에 대한 대비 요구사항은 자리표시자 텍스트에도 적용됩니다. 하지만 자리표시자는 적절한 대비 외에 - 때로는 적절한 대비 때문에 많은 사용성 및 접근성 문제를 일으킴을 언급하는 것이 중요합니다. 더 자세한 내용은 [article about why placeholders in form fields are harmful](https://www.nngroup.com/articles/form-design-placeholders/)를 참고하세요.

## "실제" 텍스트 vs. 텍스트 이미지

"실제" 텍스트는 문자 코드의 배열 (여기 이 텍스트 처럼)로 사용할 수 있는텍스트를 의미합니다. 본질적으로 기계가 읽을 수 있고 선택되고 복사-붙여넣기 될 수 있습니다. 반면 "텍스트 이미지"는 예를 들어 JPG나 PNG 파일처럼 저장되는 레스터화 된 타이포그래피 그림 (위 텍스트의 예제 이미지 같은) 입니다.

일반적으로, "실제" 텍스트와 텍스트 이미지에 동일한 대비 요구 사항과 예외가 적용됩니다.

여담으로: 유연성, 유용성, 파일 사이즈의 측면에서 텍스트 이미지의 많은 제한으로 인해 이를 사용하는 것은 권장하지 않습니다. 하지만, 텍스트 이미지를 사용*해야 한다*면 스크린리더 사용자가 접근 가능할 수 있도록 표시 된 텍스트가 이미지의 대체 텍스트(`alt` 어트리뷰트)로 설정 되었는지 확인하세요.
