---
navigation_title: "MacOS에 VMware"
position: 3
changed: "2021-03-22"
---

# macOS에 VMware Fusion 설정하기

**macOS에서, Windows를 가상 머신으로 수행하려면, 특히 일상적인 워크플로에 매끄럽게 통합하려면 몇 가지 별도의 구성이 필요합니다. 일단 제대로 설정되면, macOS에서 접근성 테스트가 편안해 질 것입니다.**

![VMware Fusion logo](_media/vmware-fusion-logo.png)

## 가상 머신 준비하기

계속 하기 전에, 여기 설명된 대로 미리 설정 된 가상 머신(VM)을 다운로드 받으세요: [Microsoft에서 무료로 Windows 가상 머신 받기](/setup/windows/virtual-machine).

이후 (내장 된 unzip 버전은 zip64 파일에 사용할 수 없으므로 [The Unarchiver](http://wakaba.c3.cx/s/apps/unarchiver.html)를 사용하여) 적절한 위치 예를 들어 `~/Virtual Machines`에 압축을 풉니다.

## VMware Fusion 설치

[VMware Fusion](http://www.vmware.com/ch/products/fusion)를 다운로드 후, 설치하고 실행합니다:

- `File` -> `Import`를 선택, 압축 해제 된 폴더에서 `*.ovf`를 선택하고 확인.
- 스냅샷 생성 (`Command + Shift + S`).
    - 이렇게 하면 나중에 해당 상태로 쉽게 돌아갈 수 있습니다, 즉 VM의 Windows 90일 라이센스를 반복해서 다시 활성화 할 수 있음을 의미합니다.
    - 더 자세한 내용은 [스냅샷 이해하기 (VMware)](https://kb.vmware.com/s/article/1014509)를 참고하세요.
- `Virtual Machine` -> `Settings`에서:
    - 레티나 디스플레이라면, `Display`로 가서 `레티나 디스플레이에 전체 해상도 사용`을 선택 해제합니다 (그렇지 않으면 눈이 아플 겁니다).
    - `Processors & Memory`로 가서, 최소 2000MB 메모리를 선택하세요.
    - 인터넷에 연결하려면, `Add Device...` 를 클릭하고 `Network Adapter`를 선택하세요.
        - `Share with my Mac` 옵션을 사용하세요.

## 처음으로 VM 부팅하기

VM을 시작하세요. 사용자와 암호는 여기에서 확인 할 수 있습니다: [Microsoft에서 무료로 Windows 가상 머신 받기](/setup/windows/virtual-machines).

## 매끄러운 통합 개선하기

당신의 사랑하는 Mac에서 Windows 머신이 돌아가는 것만으로도 이미 소름끼치게 느껴질 수 있습니다. 작업 할 때 가능한 편안함을 느낄 수 있도록 다음의 추가적인 설정 단계를 제안합니다.

### 왼쪽 Windows 키 비활성화

VMware Fusion에서, 기본적으로 왼쪽 `Command`키가 왼쪽 `Windows`키로 할당됩니다. 따라서 `Command + Tab`를 누르는 것은 종종 외관상 임의로 VM의 "시작" 메뉴를 열고 닫는 왼쪽 `Windows` 키로 작용합니다.

![열려진 Windows 7 시작 메뉴](_media/opened-windows-7-start-menu.png)

이를 방지하고 싶다면:

- `VMware Fusion` -> `Preferences` -> `Keyboard & Mouse` -> `Mac Host Shortcuts`.
- 이후 `For Windows key, use`에서 `Right Command key`를 선택하세요.

여전히 오른쪽 `Command`키를 "시작" 메뉴를 열고 닫는데 사용할 수 있음을 기억하세요.

### 기능 키 동작 변경하기

Windows 데스크탑 스크린리더는 기능 키 (`F1` ~ `F12`)를 많이 사용합니다.

![키보드의 기능 키](_media/function-keys-on-a-keyboard.png)

기본적으로, macOS에서는, 특정 기능키를 트리거 하기 위해 `Fn`키와 함께 눌러야 합니다.

데스크탑 스크린리더의 키보드 단축키는 상당히 까다롭습니다 (정말 궁금하고 이에 대해 더 배우고 싶다면 [Insert 보조 키](/knowledge/screen-readers/desktop/insert-modifier-key)와 [스크린리더 단축키](/knowledge/screen-readers/desktop/screenreader-shortcuts)로 건너뛰어 읽어보세요). 기능 키는 종종 그것들의 일부이므로, [기능 키의 동작을 변경 (Apple Support)](https://support.apple.com/en-us/HT204436)하여 그것들에 대해 `Fn` 키를 사용할 필요가 없도록 하는 것을 권장합니다.

### Insert 키 에뮬레이트하기

Windows 데스크탑 스크린리더는 `Insert` 키에 크게 의존합니다.

![키보드의 insert 키](_media/insert-key-on-a-keyboard.png)

이 키는 Mac에서 사용할 수 없으므로(이전 macOS에서는, "Help"키 였음), 에뮬레이트해야 합니다. 이를 수행하는 가장 강력한 방법은 주어진 키를 다른 키로 변환하는 무료 소프트웨어 Karabiner-Elements를 사용하는 것입니다.

- [Karabiner-Elements](https://pqrs.org/osx/karabiner/)를 다운로드하고 설치하세요.
    - `System Preferences`' `Security & Privacy` 섹션에서 실행을 허용해야 합니다.
- 실행 후, `Simple Modification`을 추가하세요:
    - `right_option`에서 `insert`로.
    - `right_option` 대신, 원하는 키를 선택할 수 있습니다. 일상적인 워크플로에서 실제로 필요하지 않은 키인지 확인하세요.

그렇지 않으면, Mac에 물리적 [USB num lock 키보드](http://lmgtfy.com/?q=USB+num+lock+keyboard) (또는 `Insert` 키를 제공하는 다른 키보드)를 연결할 수 있습니다.

## VM과 매끄럽게 작업하기

VMware를 `Single Window` 모드(기본값)로 실행하는 것이 가장 쉽다고 생각합니다:

- Mac 앱간 전환에 `Command + Tab`을 사용하세요.
- Windows 앱 (VMWare가 활성화 된 경우) 전환에 `Option + Tab`을 사용하세요.

Dock에서 (따라서 `Command + Tab`을 누를 때 앱 전환기에서도) 모든 Windows 앱에 접근하도록 하려면, "Unity" 모드가 매우 멋집니다. Windows의 작업표시줄도 Mac의 메뉴바에 나타납니다.
