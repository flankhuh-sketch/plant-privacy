# 플랜트 개인정보처리방침 — 검토 초안

- 서비스: 플랜트(Plan_T)
- 개발자 공개 표시명: 허구리
- 개인정보 문의 이메일: flankhuh@gmail.com
- `index.html`: 모바일 대응 페이지 초안. 검토 후 확정해야 하며 아직 AdMob 제출용 완성본이 아닙니다.
- 앱 코드나 개인 실명은 이 저장소에 포함하지 않습니다.

## 공개 전 확인 항목

1. 1인 개발자의 국내법상 개인정보 보호책임자 표시 방법. 닉네임만으로 충족한다고 확정하지 않았습니다.
2. 이메일 계정 삭제 요청 접수 및 수동 처리 가능 여부. 로그아웃/앱 삭제는 서버 데이터 삭제가 아닙니다.
3. Firebase Console에서 Firestore 및 Storage 실제 리전 확인.
4. Cloud Logging 로그 버킷 보관 기간 확인.
5. Groq Data Controls의 Zero Data Retention 설정 확인.
6. 데이터 종류별 보관·파기 정책과 국외 이전 정보(받는 자/연락처/국가/항목/목적/시점·방법/기간/법적 근거/거부 방법) 확정.
7. 아동 이용 정책. 구현되지 않은 연령 제한이나 보호자 동의 기능이 있다고 표시하지 않습니다.

## 코드 확인 근거

2026-10-10 검토. 앱 main e27f2f79329b98617cc5334fd0d5ebcde4f75cb4 기준.
Google/Firebase 로그인, 게스트 익명 UID, 포트폴리오 및 거래기록, 분석보고서, 출석/미션/씨앗, AdMob 서버측 보상 검증을 사용합니다.
OCR은 ML Kit 기기 인식 후 추출 텍스트와 구조화된 후보값을 Groq에 전송합니다.
OCR 서버 로그에 첫/마지막 텍스트 및 행별 값이 남는 경로가 있어 무조건 미보관·즉시 파기라고 선언하지 않습니다.

## GitHub Pages

검토 완료 후 Settings → Pages → Deploy from a branch → main → /(root) → Save.
예상 주소: https://flankhuh-sketch.github.io/plant-privacy/
페이지가 실제 열리는지 확인 후 AdMob에 제출합니다.

## 참고

- https://www.law.go.kr/법령/개인정보보호법/제30조
- https://www.privacy.go.kr/front/bbs/bbsView.do?bbsNo=BBSMSTR_000000000049&bbscttNo=20885
- https://support.google.com/googleplay/android-developer/answer/10144311
- https://firebase.google.com/support/privacy
- https://console.groq.com/docs/your-data
- https://developers.google.com/admob/android/privacy/play-data-disclosure
