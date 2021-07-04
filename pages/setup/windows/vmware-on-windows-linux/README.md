---
navigation_title: "Windows & Linux에 VMware"
position: 4
changed: "2021-03-22"
---

# Windows (및 Linux)에 VMWare Workstation Pro 구성하기

**이미 운영 체제로 Windows를 실행하고 있더라도, 접근성 테스트를 위해 별도로 구성된 가상 머신 내에 다른 Windows를 설정하는데 필요한 초기 노력을 기울이는 것이 좋습니다. 이는 시스템을 깨끗하게 유지시키고 접근성 테스트를 좀 더 편안하게 합니다.**

![VMware Workstation Pro 로고](_media/vmware-workstation-pro-logo.png)

## Windows vs. Linux

다음 지침은 VMware Workstation Pro의 Windows 버전에 대해 별도로 작성되었지만, Linux 버전과 유사한 방식으로 적용되어야 합니다.

## 가상머신 준비하기

계속 하기 전에, 여기 설명된 대로 미리 설정 된 VM을 다운로드 받으세요: [Microsoft에서 무료로 Windows 가상 머신 받기](/setup/windows/virtual-machine).

VM을 적절한 위치 예를 들어 `C:\Virtual Machines\Accessibility Testing`에 압축을 풉니다.

## VMware Workstation Pro 설치

참고: 본 지침에서는 [VMware Workstation Pro](https://www.vmware.com/products/workstation-pro.html) 사용을 추천합니다. 하지만 [VMware Workstation Player](https://www.vmware.com/products/workstation-player.html)도 있습니다: 더 저렴하지만, 기능이 제한되어 있습니다, 예를 들어 스냅샷 기능이 없습니다(아래 참조).

VMware Workstation Pro를 다운로드 한 후, 설치하고 실행합니다:

- `Open a virtual machine`를 클릭하고, 압축을 푼 폴더에서 `*.ovf` 파일을 선택하고, 확인.
- 스냅샷 생성 (`Ctrl + Shift + S`).
    - 이렇게 하면 나중에 해당 상태로 쉽게 돌아갈 수 있습니다, 즉 VM의 Windows 90일 라이센스를 반복해서 다시 활성화 할 수 있음을 의미합니다.
    - 더 자세한 내용은 [스냅샷 이해하기 (VMware)](https://www.vmware.com/support/ws5/doc/ws_preserve_sshot_understanding.html)를 참고하세요.
- `Edit virtual machine settings`를 클릭.
    - `Processors & Memory`로 가서, 최소 2000MB 메모리를 선택하세요.
    - 인터넷에 연결하려면, `Hardware` 탭 하단의 `Add`를 클릭.
        - `Hardware types` 목록에서 `Network Adapter`를 선택하고 `Next` 클릭.
        - `NAT: Used to share the host's IP address`을 선택하고 `Finish` 클릭 후 `OK`.

## 처음으로 VM 부팅하기

VM을 시작하세요. 사용자와 암호는 여기에서 확인 할 수 있습니다: [Microsoft에서 무료로 Windows 가상 머신 받기](/setup/windows/virtual-machine).

## 매끄러운 통합 개선하기

### Insert 키 에뮬레이트하기

Windows 데스크탑 스크린리더는 `Insert` 키에 크게 의존합니다.

![키보드의 Insert 키](_media/insert-key-on-a-keyboard.png)

이 키는 일부 키보드에서 쉽게 사용 가능하지 않기 때문에, 에뮬레이트해야 할 수 있습니다. 가장 쉬운 방법은 SharpKeys 소프트웨어를 사용하는 것입니다.

- SharpKeys은 주어진 키를 다른 키로 변환합니다 (VM 자체에서).
- VM에서, [SharpKeys](http://sharpkeys.codeplex.com/)를 다운로드하고 설치 및 실행하세요.
- `Add`를 클릭 후, 원하는 키를 (예를 들어 오른쪽 `Alt` 키 `E0_38`을) `Insert` 키 `E0_52`로 매핑하세요.
- `OK`를 클릭하고 `Write to Registry`.
- VM을 재시작하세요.

## VM과 매끄럽게 작업하기

자신에게 가장 적합한 모드를 찾기 위해 "Single Window"와 "Unity"를 둘러보기를 권합니다.
