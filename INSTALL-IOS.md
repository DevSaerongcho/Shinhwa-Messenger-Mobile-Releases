# iPhone·iPad 수동 설치

**0.17.3 Ad Hoc 기술 시험판 IPA를 제공합니다.** Apple 배포 서명·프로비저닝·푸시 권한 검증을 통과했습니다. 현재 팀에 등록된 **기기 2대만 설치 대상**이며, 실제 기기 설치와 전체 기능 검증은 아직 완료되지 않았습니다.

[IPA 다운로드](https://github.com/DevSaerongcho/Shinhwa-Messenger-Mobile-Releases/releases/download/mobile-v0.17.3-preview.1/Shinhwa-Messenger-0.17.3-iOS-preview.ipa) · [SHA-256 파일](https://github.com/DevSaerongcho/Shinhwa-Messenger-Mobile-Releases/releases/download/mobile-v0.17.3-preview.1/Shinhwa-Messenger-0.17.3-iOS-preview.ipa.sha256)

현재 프로비저닝 만료: **2027년 4월 3일 09:48 한국 시간**. 만료 전에 새 서명 파일로 업데이트해야 합니다. 푸시의 Apple 권한은 포함됐으나 운영 서버의 APNs 키 설정과 실제 알림 수신 확인은 별도로 필요합니다.

App Store에 등록하지 않아도 iPhone 앱에는 유효한 Apple 서명이 필요합니다. 이번 수동 설치는 **Ad Hoc 배포로 등록된 관리자 기기에 설치**하는 방식으로 준비합니다. Apple의 [등록 기기 배포 안내](https://developer.apple.com/documentation/xcode/distributing-your-app-to-registered-devices)와 [Ad Hoc 프로파일 안내](https://developer.apple.com/help/account/provisioning-profiles/create-an-ad-hoc-provisioning-profile)를 따릅니다.

## 설치 절차

1. 관리자에게 기기 등록을 요청합니다. 기기의 UDID가 배포 프로비저닝에 포함되어야 합니다. UDID는 이 공개 저장소에 게시하지 않고 담당 관리자에게 전달합니다.
2. 이 저장소의 릴리스에서 `.ipa`와 `.ipa.sha256` 파일을 내려받습니다. 터미널에서 두 파일이 있는 폴더로 이동한 뒤 `shasum -a 256 -c Shinhwa-Messenger-0.17.3-iOS-preview.ipa.sha256`을 실행해 `OK`를 확인합니다.
3. Mac의 Apple Configurator에 iPhone을 연결하고 기기를 신뢰한 뒤, 내려받은 앱을 추가합니다. 기기에서 개발자 모드 등 설치 안내가 표시되면 Apple의 안내에 따라 진행합니다.
4. 기존 Tailscale 연결과 서버 공유 권한을 확인합니다.
5. 신화 메신저를 실행하고 기존 승인된 Microsoft 계정으로 로그인합니다.

등록되지 않은 기기에는 이 IPA를 설치할 수 없습니다. 설치 대상 여부는 담당 관리자에게 확인해주세요. 새 기기를 등록한 뒤에는 프로비저닝과 IPA를 다시 생성해야 합니다. 기기 식별자 목록은 안내 문서에 게시하지 않습니다. 인증서나 프로비저닝이 만료되면 새 서명 파일을 받아 업데이트해야 합니다.

최소 빌드 대상은 iOS 15입니다. iPhone Duo의 접기·펼치기·화면 회전과 실제 로그인·알림·전체 기능 검증은 아직 완료되지 않았습니다.
