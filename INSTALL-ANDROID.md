# Android 수동 설치

현재 파일은 서명된 기술 시험판입니다. 운영용 전체 기능 검증은 아직 마치지 않았습니다.

1. 관리자가 제공한 기존 Tailscale 계정·서버 공유 권한을 준비합니다. Tailscale 연결을 켭니다.
2. [0.17.3 Android 시험판 릴리스](https://github.com/DevSaerongcho/Shinhwa-Messenger-Mobile-Releases/releases/tag/mobile-v0.17.3-preview.1)를 엽니다.
3. `Shinhwa-Messenger-0.17.3-Android-preview.apk`를 휴대폰에 내려받습니다. `Source code` 압축 파일은 설치 파일이 아닙니다.
4. 내려받은 APK를 엽니다. Android가 설치 권한을 요청하면 파일을 연 브라우저 또는 파일 앱의 **알 수 없는 앱 설치** 설정을 허용하고 설치를 진행합니다. 설정 이름은 기기·OS에 따라 다를 수 있습니다. 조직 정책이 설치를 차단하면 기기 관리자에게 확인합니다.
5. **신화 메신저**를 열고 기존 승인된 Microsoft 계정으로 로그인합니다.
6. 로그인·서버 연결·채팅·첨부·알림은 관리자 시험 절차에 따라 확인합니다. 현재 시험판은 서버의 모바일 지원 적용과 실제 기능 검증이 남아 있습니다.

Google Play Console 계정은 APK 직접 설치에 필요하지 않습니다. 다른 출처의 앱 설치에 관한 [Google 안내](https://support.google.com/android/answer/9457058?hl=ko)도 참고할 수 있습니다.

## 파일 확인

같은 릴리스의 `.apk.sha256` 파일과 다운로드한 APK의 SHA-256 값이 일치해야 합니다.

```sh
# macOS
shasum -a 256 Shinhwa-Messenger-0.17.3-Android-preview.apk
```

```powershell
# Windows PowerShell
Get-FileHash .\Shinhwa-Messenger-0.17.3-Android-preview.apk -Algorithm SHA256
```

## 업데이트와 설치 오류

앞으로 제공되는 같은 앱의 서명된 APK를 설치해 업데이트합니다. 인증서가 다르다는 오류가 나면 임의로 기존 앱을 삭제하기 전에 관리자에게 확인하세요. 예전에 내부 debug APK를 설치한 기기는 이번 전용 서명 시험판과 인증서가 다를 수 있습니다. 서버의 업무·대화 기록과 기기의 로그인 상태·전송 전 초안은 저장 위치가 다릅니다.

Microsoft 로그인 후 앱으로 돌아오지 않으면 관리자에게 알려주세요. 기존 신화 커뮤니티 앱과 로그인 콜백 스킴을 공유하므로 두 앱을 함께 설치한 기기의 복귀 동작은 별도 확인이 필요합니다. 앱을 완전히 닫은 상태의 알림은 APNs·FCM 서버 설정과 실제 수신 검증을 마친 뒤 지원 상태를 안내합니다.
