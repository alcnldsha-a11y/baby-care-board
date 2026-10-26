# 우리 아기 케어보드

GitHub Pages로 배포할 정적 육아 관리 웹사이트입니다. 현재 배포 준비 상태이며 온라인 배포는 완료되지 않았습니다.

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