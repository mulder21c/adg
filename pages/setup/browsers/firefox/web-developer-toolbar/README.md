---
navigation_title: "웹 개발자 도구 모음"
position: 1
changed: "2018-05-10"
---

# 웹 개발자 도구 모음

**대부분의 엡 개발자가 이미 잘 알고 있는, 웹 개발자 도구 모음 확장은 파이어폭스에 모든 종류의 코드 검사 및 디버깅에 매우 유용한 다양한 도구를 추가합니다. 스크린리더의 제약을 알고 있다면 때때로 스크린리더의 대체로 볼 수도 있습니다.**

![웹 개발자 도구 모음](_media/web-developer-toolbar.png)

## 설치

[웹 개발자 도구 모음](https://addons.mozilla.org/de/firefox/addon/web-developer/) 설치.

## 사용법

브라우저 도구 모음에서 아이콘을 클릭하여 기능 메뉴를 여세요.

![웹 개발자 도구 모음 브라우저 icon](_media/web-developer-toolbar-browser-icon.png)

### 엘리먼트 정보 검사

도구 모음은 현재 페이지를 시각적으로 검사할 수 있는 많은 기능이 있습니다. `Images` -> `Display Alt Attributes`를 사용하여 이미지의 대체 텍스트나 `Information` -> `Display Abbreviations`를 사용하여 약어와 같이, 엘리먼트에 대한 다양한 정보를 빠르게 검사하는데 주로 사용합니다.

### 스크린리더 시뮬레이션 Poor man's screen reader simulation

도구 모음은 스크린리더가 현재 페이지를 인식하는 방법을 시각적으로 시뮬레이션 하는데 매우 유용할 수 있습니다. 이것은 `CSS` -> `Disable All Styles`를 사용하여 모든 스타일을 비활성화하여 달성될 수 있습니다.

모든 시각적 속성(property)를 제거하면, 가장 기본적인 HTML (bare HTML)만 남고, 사용 가능한 의미론이 사용자에게 시각적으로 쉽게 표시됩니다 (정말 궁금하고 이에 대해 더 배우고 싶다면, [의미론과 접근성에 대한 중요성](/knowledge/semantics)으로 건너뛰어 읽어보세요).

그러나 이 접근법에는 몇 가지 분명한 단점이 있습니다, 예를 들어:

- 이미지가 여전히 시각적으로 표시되므로, 적절한 대체 텍스트가 있는지 주의를 기울이세요.
    - 이를 보완하기 위해 `Images` -> `Display Alt Attributes`를 사용할 수 있습니다.
- `display: none`이나 `visibility: hidden`을 사용하여 모든 기기로부터 숨겨진 엘리먼트는 이제 숨김 해제됩니다.
    - 이를 방지하려면, 엘리먼트를 숨기기 위해 HTML의 `hidden` 어트리뷰트를 대신 사용하세요 (정말 궁금하고 이에 대해 더 배우고 싶다면, [모든 기기로부터 엘리먼트 숨기기](/examples/hiding-elements/from-all-devices)로 건너뛰어 읽어보세요).
- ARIA 어트리뷰트는 시각적인 표현이 없으며 이 방법으로는 완전히 놓치게 됩니다 (정말 궁금하고 이에 대해 더 배우고 싶다면, [ARIA — HTML만으로는 충분하지 않을 때](/knowledge/aria)로 건너뛰어 읽어보세요).
    - 이를 방지하려면, ARIA 사용을 최소한으로 유지하세요 (정말 궁금하고 이에 대해 더 배우고 싶다면, [ARIA 역할과 속성의 합리적인 사용](/examples/sensible-aria-usage)으로 건너뛰어 읽어보세요).
- 새로 추가 된 CSS는 차단되지 않습니다 (예를 들어 일부 JavaScript를 통해 페이지와 상호작용 하는 경우).

따라서 이것은 페이지에 대한 대략적인 아이디어를 빠르게 얻을 수 있는 유효한 방법이지만, 단연코 실제 스크린리더로 테스트 하는 것을 대체할 수는 없습니다.