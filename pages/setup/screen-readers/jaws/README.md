---
navigation_title: "JAWS"
position: 4
changed: "2020-04-30"
---

# JAWS 설치 및 구성

**JAWS (Job Access With Speech)는 가장 많이 사용 되는 데스크탑 스크린리더 중 하나입니다. 따라서 웹 사이트와 이것의 호환성을 보장하는 것이 매우 중요합니다. 무겁기 때문에, JAWS는 개발 중 다소 세련되지 못한 도구이지만, 데스크탑에서 접근성을 점검하기 위해 매 번 실행하는 것이 절대적으로 중요합니다.**

## 설치

JAWS는 Windows 운영 체제에 깊이 설치되는 매우 무거운 소프트웨어 입니다. 기존 Windows를 깨끗하게 유지하려면, 가상 머신(VM)에 JAWS를 설치하는 것이 좋습니다, [Windows 운영 체제](/setup/windows)를 참고하세요.

JAWS는 가격이 있는 상용 소프트웨어이므로, 무료 데모 버전을 사용하여 40분간 사용 할 수 있습니다.

[JAWS를 다운로드](http://www.freedomscientific.com/Downloads/JAWS)하고 간단히 설치를 실행하거나, [JAWS 빠른 시작 (PDF, FreedomScientific.com)](http://www.freedomscientific.com/Content/Documents/Manuals/JAWS/JAWS-Quick-Start-Guide.pdf)에서 자세한 정보를 참고하세요.

## JAWS 실행

### 시작하기

데스크탑의 아이콘을 사용하여 JAWS를 시작하세요.

![JAWS 아이콘](_media/jaws-icon.png)

실행 된 후에는, JAWS와 올바르게 상호작용 하도록 웹 브라우저를 다시 시작해야 합니다.

### 메뉴 사용

기본적으로 JAWS는 실행 중에 어플리케이션 창을 표시합니다.

![JAWS 어플리케이션 창](_media/jaws-application-window.png)

작업 표시줄의 공간을 아끼려면, JAWS가 시스템 트레이에서 실행되어야 합니다:

- JAWS에서, `Options` -> `Basics`을 여세요.
- `Run JAWS from System Tray`을 선택하세요.
- 확인 후 JAWS를 재시작하세요.

이제부터, 시스템 트레이에 있는 작은 아이콘을 제외하고는 JAWS를 많이 볼 수 없습니다.

![시스템 트레이의 JAWS](_media/jaws-in-the-system-tray.png).

아이콘을 클릭하면, JAWS 메뉴가 표시됩니다.

![JAWS 메뉴](_media/the-jaws-menu.png)

또는, `JAWS + J`를 툴러 표시할 수 있습니다. 기본적으로, `JAWS` 키는 `Insert` 키 입니다 (정말 궁금하고 이에 대해 더 배우고 싶다면, [The Insert 보조 키](/knowledge/screen-readers/desktop/insert-modifier-key)로 건너뛰어 읽어보세요).

키보드로 JAWS 메뉴를 사용하는 가장 좋은 방법은:

- 방향 키를 사용하여 탐색하고 항목을 선택하는데 `Enter`를 누르세요.
- 더 빠른 탐색을 위해, 원하는 메뉴 항목에 밑줄이 그어진 키보드의 문자를 누르세요.
    - 예를 들어, `Exit`를 위해 `X`를 누르세요.
    - 본 지침에서는, 이러한 문자를 괄호로 묶어서, 예를 들어 `E(x)it`나 `(H)elp`와 같이 표시합니다.
- `Esc`를 눌러 메뉴 항목을 닫을 수 있습니다.

### 필요시 JAWS 음소거

JAWS가 실행되는 동안, 현재 화면에 보여지는 내용이 낭독됩니다.

- JAWS가 현재 단어 스트림을 중단하도록 하려면, `Ctrl` 키를 누르세요.
- JAWS가 완전히 입다물게 하려면, `JAWS + Space` 누른 다음 `S`를 눌러 음성 출력 모드를 전환할 수 있습니다.
    - JAWS가 여전히 백그라운드에서 실행되고 있으므로, 일부 상황에서는 컴퓨터가 다르게 동작할 수 있습니다!

### 점자 뷰어

JAWS는 NVDA 처럼 `음성 출력 뷰어`를 제공하지 않지만 ([NVDA 설치 및 구성](/setup/screen-readers/nvda) 참고), `점자 뷰어`가 적어도 현재 JAWS 초점이 어디에 있는지에 대한 몇가지 정보를 제공합니다.

![JAWS 점자 뷰어](_media/jaws-braille-viewer.png)

점자 뷰어는 화면 상단에 있습니다. 출력은 종종 `vl` (방문한 링크에 있는 경우)이나 `r2c3` (테이블 내 2행 3열에 있는 경우)와 같은 기호 엘리먼트를 포함합니다.

### 음성 기록

종종 JAWS가 지나간 낭독된 것을 볼 수 있는 것은 (또는 일부 출력을 복사&붙여넣기 하는 것) 흥미롭습니다.

![JAWS 낭독 기록 대화상자](_media/jaws-speech-history-dialog.png)

출력 기록을 열려면:

- `JAWS + Space`를 누르고 (*비프*음이 날겁니다), `H`를 누르세요.
- 기록은 마지막 20개의 낭독을 보여줍니다.
- 안타깝게도, 기록은 자동으로 갱신되지 않습니다.

## 구성

일반적으로 스크린 리더는 동작에 큰 영향을 미칠 수 있는 다양한 구성 옵션을 제공합니다. 기본 값을 그대로 두는 것을 권장합니다. 다음 구성 제안은 유용하고 안전한 것으로 알려져 있습니다.

### 자동 양식 모드 비활성화 (선택 사항)

JAWS는 기본적으로 인터랙션 모드를 자동으로 전환합니다 (이에 대해 정말 궁금하다면, [스크린리더의 브라우즈 모드와 포커스 모드](/knowledge/screen-readers/desktop/browse-focus-modes)로 건너뛰어 읽어보세요). 프로그래밍 및 테스트 동안 (특히 복잡한 JavaScript 위젯의 경우), 이 동작은 다소 불쾌할 수 있습니다.

이 모드는 비활성화 될 수 있으므로, NVDA와 유사합니다. **하지만 무엇을 하는 것인지 정말 알고 있는 경우에만 이것을 하도록 강력히 권고합니다.**

- 파이어폭스를 여세요.
- `JAWS + V`를 누르세요 (이것은 현재 열려있는 응용 프로그램의 빠른 설정을 엽니다래그).
- 검색 필드에 "form"을 입력하세요.
- `Virtual Cursor Options`에사 `Form Options`을 찾고 `Auto Forms Mode`를 찾으세요.
- `SemiAuto`를 선택하고 확인을 누르세요.

인터넷 익스플로러에도 동일하게 하세요.
