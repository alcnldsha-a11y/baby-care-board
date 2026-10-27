# 우리 아기 케어보드

GitHub Pages로 배포할 정적 육아 관리 웹사이트입니다. 배포 주소: https://alcnldsha-a11y.github.io/baby-care-board/

## 개인정보와 저장 방식

배포 파일에는 생년월일 기본값과 개인 기록을 포함하지 않습니다. 입력한 기록은 해당 기기와 브라우저의 localStorage에 저장됩니다. PC와 스마트폰의 기록은 자동 동기화되지 않습니다. 기존 로컬 파일의 기록도 새 사이트로 자동 이전되지 않습니다. 필요하면 화면에서 백업을 내보낸 후 새 사이트에서 직접 불러오세요. 백업 JSON 파일은 공개 저장소에 업로드하지 마세요.

## 최초 배포

사용자 승인과 GitHub 인증 후 새 공개 저장소 baby-care-board를 생성하고 이 폴더의 검토된 파일만 업로드합니다. 기존 저장소가 있으면 덮어쓰지 않습니다.

Settings → Pages → Deploy from a branch → main → /(root) → Save로 설정합니다.

## 수정 후 재배포

이 폴더의 index.html을 수정하고 VS Code 소스 제어에서 변경 내용을 확인하여 커밋하고 푸시하세요. 최초 배포 설정 후 main 브랜치에 푸시하면 자동 재배포됩니다.

터미널에서는 이 폴더에서 다음을 실행합니다.

```powershell
git add -- index.html README.md .gitignore .nojekyll
git diff --cached
git commit -m "Update care board"
git push origin main
```

.gitignore는 검토한 배포 파일만 허용합니다. 새 파일을 추가할 때 개인정보를 점검하고 허용 목록을 수정하세요. 인증 토큰이나 비밀번호를 코드에 저장하지 마세요.
## 사진·건강 기록

상단의 사진·건강 기록에서 사진 업로드, 앨범 검색, 보호자 수동 평가, 전후 비교, 성장 측정 기록·그래프, 진료용 요약 인쇄/PDF를 사용할 수 있습니다. 사진·측정값은 IndexedDB에 저장됩니다. 사진 포함 전체 ZIP 백업을 정기적으로 내려받으세요. 기존 JSON 백업은 육아 기록 전용으로 유지되며 사진을 포함하지 않습니다.

AI 자동분석은 미연결 상태입니다. 사진을 외부로 전송하지 않습니다. 연결 후보·요금·개인정보 처리·승인 필요 사항은 [AI 연결 검토](AI-INTEGRATION.md)를 참고하세요.

배포 자산: index.html, health.css, health.js, health-data.js. 외부 스크립트나 CDN 라이브러리를 사용하지 않습니다. 모든 자산 경로는 프로젝트 하위 경로에 대응하는 상대 경로입니다. 실제 사진·백업·비밀키·테스트 자료는 커밋하지 마세요.
