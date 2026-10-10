# 김서환 AI Engineer 포트폴리오

Dacon → ClarifyTrial → MedInTech → Automail → Databrain 순서로 구성한 한국어 단일 페이지 사이트입니다. AI 데이터 서비스 개발 지원에 맞춰 데이터 분석과 전처리, AI 결과 검증, 업무 자동화 및 데이터 시각화 경험을 중심으로 구성했습니다. 교육 섹션은 제외하고 실제 수행한 경험을 담았습니다.

## 디자인 변경

큰 슬로건과 상단 성과 패널을 제거했습니다. 흰 배경에서 이름과 짧은 소개로 시작하며, 프로젝트는 역할·기간과 구현 내용을 두 열로 정렬했습니다. 상단 소개 오른쪽에는 제공한 프로필 사진을 배치했습니다. 카드와 기술 배지를 없애고 여백과 구분선으로 읽는 순서를 만들었습니다. 성과는 각 프로젝트 안에서 표시하며 Agent 구조도는 펼침 영역에서 확인할 수 있습니다.

Impeccable 공식 저장소의 critique, distill, quieter 지침을 참고한 수정입니다. 정식 플러그인 설치나 자동 평가 명령 실행은 하지 않았습니다.

## 실행

설치와 빌드가 필요 없습니다. `index.html`을 브라우저로 열면 됩니다.

로컬 서버로 확인하려면 이 폴더에서 실행하세요.

```bash
python3 -m http.server 8000
```

브라우저에서 `http://localhost:8000`으로 접속합니다. 종료는 `Ctrl+C`입니다.

## 가장 쉬운 GitHub Pages 배포

1. GitHub에 로그인하고 `portfolio`라는 **Public 저장소**를 만듭니다. 무료 계정에서는 공개 저장소 방식이 가장 간단합니다.
2. ZIP을 풀고 **portfolio 폴더 안의 파일**을 저장소 루트에 업로드합니다. 저장소 첫 화면에 `index.html`, `styles.css`, `assets` 폴더가 보여야 합니다. `portfolio` 폴더 자체를 한 단계 더 넣으면 안 됩니다.
3. 저장소 **Settings → Pages → Build and deployment**에서 **Source: Deploy from a branch**를 선택합니다.
4. **Branch: main / Folder: /(root)**를 선택하고 Save를 누릅니다. 업로드한 기본 브랜치 이름이 다른 경우 해당 브랜치를 선택합니다.
5. 배포가 완료되면 Pages 설정에 표시되는 주소를 확인합니다. `portfolio` 저장소라면 보통 `https://GITHUB_USERNAME.github.io/portfolio/` 형식입니다.
6. PC와 휴대폰에서 링크를 열어 내용과 연락처를 확인한 뒤 지원서에 넣습니다.

`.nojekyll`은 정적 파일을 그대로 제공하기 위한 파일입니다. 웹 업로드 때 누락되어도 이 사이트에는 Jekyll 전용 파일이 없어 정상 동작합니다. 가능하면 함께 올리세요.

## 터미널에서 Git으로 배포

빈 Public 저장소를 먼저 만드세요. 아래 명령은 **압축 해제한 portfolio 폴더**에서 실행합니다. `GITHUB_USERNAME`을 본인 계정명으로 바꾸세요. Git 사용자 이름과 이메일이 설정되어 있어야 하며, push 시 GitHub 인증이 필요합니다. 저장소에 이미 README 등의 커밋이 있다면 clone한 뒤 파일을 복사하는 방식이 편합니다.

```bash
git init
git add .
git commit -m "Add AI engineer portfolio"
git branch -M main
git remote add origin https://github.com/GITHUB_USERNAME/portfolio.git
git push -u origin main
```

그다음 위의 **Settings → Pages** 설정을 한 번 완료합니다. 이후에는 변경한 파일을 commit하고 push하면 다시 배포됩니다.

```bash
git add .
git commit -m "Update portfolio"
git push
```

공식 안내: https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site

## 파일 구성

- `index.html`: 소개, 프로젝트, 성과, 기술, 상단 이메일
- `styles.css`: 데스크톱·모바일 레이아웃 및 인쇄 스타일
- `assets/favicon.svg`: 브라우저 탭 아이콘
- `assets/profile.jpeg`: 프로필 사진
- `.nojekyll`: GitHub Pages 정적 파일 설정
- `.gitignore`: OS 임시 파일 제외

JavaScript, npm 패키지, 외부 CDN, API Key 없이 동작합니다. 링크는 상대 경로이므로 저장소 이름이 달라도 자산 경로를 따로 수정할 필요가 없습니다.

## 내용 수정

`index.html`을 텍스트 편집기로 열어 문장을 수정합니다. 이름, 이메일, 프로젝트 기간도 이 파일에서 바꿉니다. 프로젝트 본문은 제공된 LG CNS 지원 이력서를 기준으로 수정했으며 데이터브레인 기간도 해당 이력서의 인턴 기간을 반영했습니다.

- 연락처 이메일: `kksh3549@gmail.com`을 검색하여 텍스트와 `mailto:` 링크를 함께 수정합니다.
- GitHub 주소: 계정 주소를 확인한 뒤 메뉴 또는 연락처 영역에 실제 링크를 추가하세요. 확인되지 않은 저장소 링크는 넣지 않았습니다.
- 포인트 색상: `styles.css` 맨 위 `--teal`을 수정합니다.
- 폰트: Pretendard가 PC에 설치되어 있으면 우선 사용하고, 없으면 운영체제의 한국어 폰트를 사용합니다. 폰트 파일을 외부에서 자동으로 불러오지는 않습니다.
- 사진: `assets/profile.jpeg`에 제공한 사진을 넣었습니다. 같은 파일명으로 교체할 수 있습니다. 사진 표시 크기는 `styles.css`의 `.profile-photo`에서 수정합니다.

## 콘텐츠 확인 사항

공개 배포 전 프로젝트 사실과 회사의 공개 가능한 범위를 본인이 최종 확인하세요. 메디인테크의 사내 데이터셋명, 정확한 데이터 규모, 세부 설정값 및 절대 F2 성능값은 포함하지 않았습니다. F2 개선율과 서비스 적용 사실은 제공한 포트폴리오를 기준으로 작성했습니다.

ClarifyTrial 결과는 가상 데이터 150개 조합에서의 평가 조건은 구현 본문에 명시하고, 성과는 판정 일치율 85.3% → 99.3%로 표시했습니다. Dacon은 시나리오 기준 검증과 파생변수 설계, MAE 7% 개선 및 상위 13% 성과를 포함했습니다. 교육 섹션과 교육에서만 사용한 기술은 포함하지 않았습니다. Dacon 기간은 2026.04 - 2026.05이며 모든 프로젝트 기간을 YYYY.MM - YYYY.MM 형식으로 표기했습니다.

## 검증 범위

HTML 파싱, 내부 앵커, 로컬 자산 경로, CSS 중괄호 균형, 필수 콘텐츠와 프로젝트 순서를 점검했습니다. PC 및 모바일 브라우저의 실제 화면 렌더링과 GitHub 원격 배포는 이 패키지 생성 과정에서 수행하지 않았습니다. 배포 후 실제 화면을 한 번 확인하세요.

번호와 프로젝트명은 모두 22px로 표시하며 프로젝트 섹션의 연도 표시는 삭제했습니다.

각 대표 프로젝트는 배경, 구현, 결과 순서로 정리했습니다. 메디인테크의 추가 도구 개발은 모델 개선 및 배포 결과 뒤에 분리했습니다.

데이터브레인 경험은 광고 성과 시각화와 LLM 요약 기능 중심으로 축약했습니다.

ClarifyTrial 수상 표기는 제공한 상장으로 확인했습니다. Healthcare Agentic AI Challenge 2026 대상(1위), 팀명 Prescreen, 수상월 2026.08이며 김서환은 팀원으로 기재되어 있습니다.

상단 AI Engineer 표기와 하단 저작권 문구를 제거했습니다. Dacon의 SHAP 기여도는 혼잡도 누적 평균 최대 31%, 순간값 1%로 표시했습니다.
