---
navigation_title: "NVDA"
position: 3
changed: "2020-04-30"
---

# NVDA 설치 및 구성

**NVDA (Non Visual Desktop Access)는 가볍고 안정적인 오픈 소스 데스크탑 스크린리더입니다. 표준에 대한 확고한 준수 때문에, 접근성 개발 할 때 선택하는 데스크탑 스크린리더 입니다. 잠시 사용하고 나면, 확고 하면서도 타당한 선생님으로 존경하게 될 것입니다.**

## 설치

[NVDA 다운로드](http://www.nvaccess.org/download/).

### 일반 설치

일반 설치는 부팅 시 자동 시작(선택 사항), 시작/재시작 키보드 단축키, 전용 파일과의 연결 등을 제공합니다.

휴대용 설치(아래 참고)보다는 일반 설치를 권장합니다.

설치 프로그램을 실행하거나, 더 자세한 내용은 [NVDA 설치 (NVAccess.org)](http://www.nvaccess.org/files/nvda/documentation/userGuide.html?#toc11)를 참고하세요.

### 휴대용 설치

NVDA는 휴대용 앱으로 실행할 수 있는 옵션을 제공하므로, 설치가 필요하지 않습니다 (또한 따라서 관리자 권한도 필요하지 않습니다). 우리 목적으로는 잘 동작하지만, 몇 가지 제한 사항이 있습니다. [휴대용 및 임시용 제한 (NVAccess.org)](http://www.nvaccess.org/files/nvda/documentation/userGuide.html?#toc10)를 참고하세요.

좀 더 자세한 내용은, [휴대용 만들기 (NVAccess.org)](http://www.nvaccess.org/files/nvda/documentation/userGuide.html?#toc15)를 참고하세요 (설치 위치로 새 폴더, 예를 들어 `NVDA`를 수동으로 만들어야 합니다).

## NVDA 실행

### 시작

일반 설치를 선택한 경우, `Ctrl + Alt + N`을 누르거나 데스크탑의 아이콘을 사용하여 언제든지 NVDA를 시작(과 재시작) 할 수 있습니다.

![NVDA 아이콘](_media/nvda-icon.png)

휴대용 설치를 선택한 경우, 설치 폴더의 `NVDA.exe`를 사용하여 NVDA를 실작하면 됩니다.

### 메뉴 사용

NVDA를 시작 하고 시작 화면을 클릭한 후, 시스템 트레이의 있는 작은 아이콘 외에는 별로 표시되지 않습니다.

![시스템 트레이의 NVDA](_media/nvda-in-the-system-tray.png).

아이콘을 클릭하면, NVDA 메뉴가 표시됩니다.

![NVDA 메뉴](_media/the-nvda-menu.png)

또는, `NVDA + N`을 눌러 표시할 수 있습니다. 기본적으로, `NVDA`키는 `Insert`키 입니다(정말 궁금하고 이에 대해 더 배우고 싶다면, [Insert 보조 키](/knowledge/screen-readers/desktop/insert-modifier-key)로 건너뛰어 읽어보세요).

키보드로 NVDA 메뉴를 사용하는 가장 좋은 방법은::

- 탐색에 방향 키를 사용하고 항목을 선택하는데 `Enter`를 누르세요.
- 더 빠른 탐색을 위해, 원하는 메뉴 항목에 밑줄이 그어진 키보드의 문자를 누르세요.
    - 예를 들어, `Exit`를 위해 `E`를 누르세요.
    - 본 지침에서는, 이러한 문자를 괄호로 묶어서, 예를 들어 `(E)xit`나 `(H)elp`와 같이 표시합니다.
- `Esc`를 눌러 메뉴 항목을 닫을 수 있습니다.

### 필요 시 NVDA 음소거

NVDA를 실행하는 동안, 화면에 현재 보여지는 내용이 낭독됩니다.

- NVDA가 현재 출력을 중단하게 하려면, `Ctrl`을 (또는 현재 행을 건너 뛰려면 `Shift`를) 누르세요.
- NVDA가 완전히 입다물게 하려면, `NVDA + S`를 눌러 음성 출력 모드를 전환할 수 있습니다.
    - NVDA가 여전히 백그라운드에서 실행되고 있으므로, 일부 상황에서는 컴퓨터가 다르게 동작할 수 있습니다!

### 음성 출력 뷰어

음성 출력 뷰어는 NVDA의 오디오 출력을 테스트 형식으로 표시하여, 정상 시력 사용자에게 매우 유용합니다.

![NVDA 음성 출력 뷰어](_media/nvda-speech-viewer.png)

음성 출력 뷰어는 NVDA 메뉴에서 `도구(T)` → `음성 출력 뷰어(S)`를 선택하여 열 수 있습니다.

몇 가지 유용한 옵션이 있습니다:

- 시작 시 음성 출력 뷰어를 자동으로 열 수 있습니다.
    - 음성 출력 뷰어 좌측 하단에 있는, `NVDA 시작 시 음성 출력 뷰어 실행(S)`을 활성화 하면 됩니다.
    - 글꼴 크기는 종료 시 항상 기본 값으로 다시 설정됩니다.

NVDA를 사용하는 동안 음성 출력 뷰어를 항상 열어 두는 것을 매우 권장합니다. 화면 우측 상단에 배치하고 브라우저 창 크기를 조절하여 서로 겹치지 않게 하세요. 시스템 트레이 팝업이 약간의 공간을 가지도록, 음성 출력 뷰어에 전체 높이를 지정하지 마세요.

![브라우저와 음성 출력 뷰어의 완벽한 레이아웃](_media/perfect-layout-of-browser-and-speech-viewer.png)

## 구성

일반적으로 스크린 리더는 동작에 큰 영향을 미칠 수 있는 다양한 구성 옵션을 제공합니다. 기본 값을 그대로 두는 것을 권장합니다. 다음 구성 제안은 유용하고 안전한 것으로 알려져 있습니다.

### 마우스 초점 비활성 화

기본적으로, 마우스 커서가 움직이면, NVDA는 그 아래에 있는 개체를 낭독합니다. 이는 운 좋게 화면을 스캔하다가 무언가를 찾는 시각 장애인에게는 유용합니다. 하지만 시각 장애가 없는 개발자에게는 완전 짜증 날 수 있습니다.

다음과 같이 마우스 초점을 비활성화 할 수 있습니다:

- NVDA 메뉴에서, choose `설정 (P)` -> `NVDA 설정(S)` -> `마우스`.
- `마우스 위치 추적 사용(T)`을 비활성화 하고 확인을 누릅니다.

### 페이지 로드 시 "모두 말하기" 비활성화

기본적으로 웹 사이트가 로딩 되면, NVDA는 자동으로 모든 콘텐츠를 읽어주기 시작합니다. 이것은 개발자가 일반적으로 원하는 것이 아니므로 비활성화 합니다:

- NVDA 메뉴에서, choose `설정 (P)` → `NVDA 설정(S)` -> `브라우즈 모드`을 선택하세요.
- `페이지 로딩 시 자동으로 읽기 (S)`를 비활성화하고 확인을 누르세요.

이제 NVDA는 현재 요소를 읽은 후, 사용자가 수동으로 다은 요소로 진행할 때까지 기다립니다.

### 들을 만한 음성 엔진 (선택 사항)

표준 NVDA 음성 엔진은 다소 기계적입니다. 빠르고 매우 정밀하지만, 일부에게는 이상하게 들릴 수 있습니다. 따라서, 더 멋지고 더 자연스러운 것을 설치합시다.

- [Svox Pico add-on을 다운로드](http://files.nvaccess.org/nvda-addons/svox-pico-2.0.nvda-addon)하고 설치하세요.
- NVDA메뉴에서 , `설정 (P)` → `NVDA 설정(S)` -> `음성 출력`을 선택하세요
- 음성 엔진으로, `Svox pico synthesizer`를 선택하세요.
- 보이스 (V)에서, 원하는 음성을 선택한 후 확인을 누르세요.

### GUI 언어 (선택 사항)

NVDA 자체 언어를 선택할 수 있습니다 (음성 말고 GUI):

- NVDA 메뉴에서, `설정 (P)` → `NVDA 설정(S)` -> `일반 설정`을 선택하세요
- 원하는 언어를 선택하고 확인을 누르세요.
    - ~~본 지침을 따라가기 쉽도록 `영어, en`을 사용하는 것을 권장합니다.~~

### 키보드 레이아웃 (선택 사항)

NVDA는 `desktop`과 `laptop` 키보드 레이아웃을 제공합니다. 본 지침에서는, `laptop`이 사용됩니다:

- NVDA 메뉴에서, `설정 (P)` → `NVDA 설정(S)` -> `키보드`를 선택하세요
- 키보드 레이아웃으로 `laptop`을 선택하고 확인을 누르세요.

### 종료 확인 비활성화 (선택 사항)

기본적으로, NVDA는 종료 시 확인 창을 표시합니다.

![NVDA의 종료 확인 대화상자](_media/nvdas-exit-confirmation-dialog.png)

다음과 같이 비활성화 할 수 있습니다:

- NVDA 메뉴에서, `설정 (P)` → `NVDA 설정(S)` -> `일반 설정`을 선택하세요
- `종료 시 NVDA 종료 옵션 표시(w)`를 비활성화하고 확인을 누릅니다.

## 애드 온

[NVDA 커뮤니티 애드온 웹 사이트 (NVDA-Project.org)](https://addons.nvda-project.org/index.en.html)에 많은 NVDA용 애드온이 있습니다.

### FocusHighlight

이 애드온은 NVDA의 내부 커서가 현재 화면의 어디에 있는지 시각적으로 보여줍니다 - 정상 시력자에게 매우 유용한 도움입니다.

![FocusHighlight 애드온 동작](_media/the-focushighlight-add-on-in-action.png)

몇 가지 표시가 있습니다:

- 현재 가상 커서가 위치한 엘리먼트 주위에 녹색 테두리가 그려집니다.
- 현재 포커스 커서가 위치한 엘리먼트 주위에 빨간 테두리가 그려집니다.
    - 엘리먼트가 상호작용 중인 경우 파란색으로 바뀝니다.

각각 다른 커서 유형에 대해 정말 궁금하고 이에 대해 더 배우고 싶다면, [스크린리더의 브라우즈 모드와 포커스 모드](/knowledge/screen-readers/desktop/browse-focus-modes)로 건너뛰어 읽어보세요.

[FocusHighlight 애드온을 다운로드](http://addons.nvda-project.org/addons/focusHighlight.en.html) (안정 버전)하고 설치하세요!

::: translator-comment
해당 플러그인은 표시가 다소 정확하지 않습니다. (특히 포커스 커서의 빨간색 테두리)  
오히려 방해가 될 수도 있으니 참고하시기 바랍니다.
:::

### 선택적 추가 기능

우리가 개인적으로 좋아하는 것들입니다:

- [오늘의 팁](http://addons.nvda-project.org/addons/tipOfTheDay.en.html)은 시작 시 사용 팁을 보여줍니다.
- [비프음 없음 음성 모드](http://addons.nvda-project.org/addons/noBeepsSpeechMode.en.html)는 음성 모드를 전환할 때 (`NVDA + S) "비프음"을 제외합니다.
- [제어 사용 도우미](http://addons.nvda-project.org/addons/controlUsageAssistant.en.html)는 `NVDA + H`를 누르면 현재 초점을 얻은 항목에 대한 도움말을 제공합니다.
