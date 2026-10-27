# iPhone·iPad 수동 설치

**현재 내려받아 설치할 수 있는 IPA 파일은 없습니다.** Apple Developer 팀의 서명·프로비저닝과 대상 기기 등록을 확인한 뒤 추가할 예정입니다. 서명되지 않은 파일을 설치 가능 파일로 제공하지 않습니다.

App Store에 등록하지 않아도 iPhone 앱에는 유효한 Apple 서명이 필요합니다. 이번 수동 설치는 **Ad Hoc 배포로 등록된 관리자 기기에 설치**하는 방식으로 준비합니다. Apple의 [등록 기기 배포 안내](https://developer.apple.com/documentation/xcode/distributing-your-app-to-registered-devices)와 [Ad Hoc 프로파일 안내](https://developer.apple.com/help/account/provisioning-profiles/create-an-ad-hoc-provisioning-profile)를 따릅니다.

## IPA가 준비된 뒤의 절차

1. 관리자에게 기기 등록을 요청합니다. 기기의 UDID가 배포 프로비저닝에 포함되어야 합니다. UDID는 이 공개 저장소에 게시하지 않고 담당 관리자에게 전달합니다.
2. 이 저장소의 릴리스에서 해당 기기용으로 서명된 `.ipa`와 해시 파일을 내려받습니다. 현재는 제공하지 않습니다.
3. Mac의 Apple Configurator에 iPhone을 연결하고 기기를 신뢰한 뒤, 내려받은 앱을 추가합니다. 기기에서 개발자 모드 등 설치 안내가 표시되면 Apple의 안내에 따라 진행합니다.
4. 기존 Tailscale 연결과 서버 공유 권한을 확인합니다.
5. 신화 메신저를 실행하고 기존 승인된 Microsoft 계정으로 로그인합니다.

다른 Apple 팀·등록되지 않은 기기·만료된 프로비저닝에는 같은 IPA가 설치되지 않을 수 있습니다. 인증서나 프로비저닝이 만료되면 새 서명 파일을 받아 업데이트해야 합니다. 설치 가능한 IPA가 게시되면 적용되는 기기 등록 범위와 확인한 OS를 함께 안내합니다.

최소 빌드 대상은 iOS 15입니다. iPhone Duo의 접기·펼치기·화면 회전과 실제 로그인·알림·전체 기능 검증은 아직 완료되지 않았습니다.
