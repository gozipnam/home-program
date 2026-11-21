# 지안·선규 4주 홈 프로그램

클릭하면서 진행하는 4주 홈 프로그램 앱입니다. 설치 없이 폰 브라우저에서 열어 씁니다.

- 아이 선택 → "바로 시작하기" → 단계별 안내 + 타이머 → 결과 버튼으로 기록
- 지안: 대화·토론 → 활동·그림 → 설명·쓰기 → AI 대화 (주 3회, 월·수·토)
- 선규: 언어 → 작업 → 인지 게임, 단계마다 성공/부분/도움 필요 (주 3회, 화·목·일) + 매일 언어 숙제 체크
- 주간 리포트 자동 생성(선규 치료실 공유용 복사 버튼), 엑셀용 CSV, 백업/복원

## PowerShell로 올리기 (추천)

1. 압축을 푼 폴더에서 `deploy.bat` 더블클릭
   - 또는 PowerShell에서: `powershell -ExecutionPolicy Bypass -File .\deploy.ps1`
2. Git·GitHub CLI가 없으면 자동 설치됩니다 (winget).
3. 처음 한 번 브라우저가 열리면 화면의 코드를 입력해 GitHub 로그인 승인
4. 저장소 생성 → 업로드 → Pages 켜기까지 자동으로 되고, 마지막에 앱 주소가 나옵니다.
5. 내용을 고친 뒤 다시 실행하면 업데이트됩니다.
   - 저장소 이름을 바꾸려면: `.\deploy.ps1 -RepoName 원하는이름`

## GitHub 웹에서 직접 올리기 (5분)

1. github.com 로그인 → 오른쪽 위 **+** → **New repository**
2. 이름 예: `home-program` → **Public** 선택 → **Create repository**
3. 새 저장소 화면에서 **uploading an existing file** 클릭
4. 이 폴더의 파일 4개(`index.html`, `manifest.json`, `icon.svg`, `README.md`)를 끌어다 놓기 → **Commit changes**
5. 저장소 **Settings** → 왼쪽 **Pages** → Source: **Deploy from a branch**, Branch: **main / (root)** → **Save**
6. 1~2분 뒤 같은 화면 위쪽에 주소가 나옵니다: `https://<아이디>.github.io/home-program/`

## 폰에서 쓰기

- 위 주소를 폰에서 열고 **홈 화면에 추가** (아이폰: 사파리 공유 버튼 → 홈 화면에 추가)
- 처음에 **설정·원칙** 탭에서 1주차 시작일을 정하세요.

## 알아둘 점

- 기록은 **그 폰의 브라우저에만** 저장됩니다. 엄마·아빠 폰끼리 자동으로 합쳐지지 않으니, 한 폰으로 기록하거나 설정의 백업/복원으로 옮기세요.
- 주소는 공개지만 기록은 각자 폰에만 있어 다른 사람에게 보이지 않습니다. 다만 프로그램 내용(아이 이름, 치료 목표)은 주소를 아는 사람이 볼 수 있습니다. 신경 쓰이면 저장소를 Private으로 두고 파일을 폰에서 직접 여는 방법도 있습니다(Private 저장소의 Pages는 유료 플랜 필요).
- 내용 수정: `index.html` 안 `PROGRAM` 부분의 글자만 바꾸면 됩니다. GitHub에서 파일 열고 연필 아이콘으로 수정 → Commit.
