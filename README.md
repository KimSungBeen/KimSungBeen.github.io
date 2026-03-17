# KimSungBeen.github.io

Hugo + Blowfish 기반 개인 웹사이트 저장소입니다.

## 로컬 실행

```bash
hugo server
```

## 프로덕션 빌드

```bash
hugo --gc --minify
```

## GitHub Pages 배포

1. GitHub에서 `KimSungBeen.github.io` 공개 저장소 생성
2. 저장소 `Settings > Pages`에서 Source를 `GitHub Actions`로 변경
3. 아래 명령으로 첫 배포

```bash
git remote add origin https://github.com/KimSungBeen/KimSungBeen.github.io.git
git branch -M main
git push -u origin main
```

## Analytics And View Tracking

이 저장소는 두 가지 용도로 조회 데이터를 다룹니다.

- `Google Analytics 4`: 관리자용 대시보드 통계
- `Firebase + Firestore`: 나중에 화면에 공개할 수 있는 누적 조회수 원본

현재 설정은 조회수를 화면에 보여주지 않고, Firebase에만 백그라운드로 누적하도록 맞춰져 있습니다.

### GitHub Secrets

아래 secrets를 GitHub 저장소 `Settings > Secrets and variables > Actions`에 추가합니다.

```txt
GOOGLE_ANALYTICS_ID
FIREBASE_API_KEY
FIREBASE_AUTH_DOMAIN
FIREBASE_PROJECT_ID
FIREBASE_STORAGE_BUCKET
FIREBASE_MESSAGING_SENDER_ID
FIREBASE_APP_ID
FIREBASE_MEASUREMENT_ID
```

배포 시 GitHub Actions가 아래 설정을 자동으로 주입합니다.

- `config/_default/hugo.toml`에 `[services.googleAnalytics]`
- `config/_default/params.toml`에 `[firebase]`

### Google Analytics 4

1. GA4에서 `https://kimsungbeen.github.io/`용 Web Data Stream 생성
2. 측정 ID `G-...` 값을 `GOOGLE_ANALYTICS_ID` secret으로 등록
3. 배포 후 GA4에서 `Reports` 또는 `Explore` 화면에서 `Page path and screen class` 기준으로 글별 조회수 확인

### Firebase / Firestore

1. Firebase 프로젝트 생성
2. Web App 추가 후 앱 설정값을 GitHub secrets에 등록
3. Firestore Database 생성
4. Authentication에서 `Anonymous` 로그인 활성화
5. 아래 규칙을 Firestore에 적용

```bash
firebase deploy --only firestore:rules
```

Firestore 규칙은 [firestore.rules](/Users/tbu/Documents/sbeen/TBU/KimSungBeen.github.io/firestore.rules)에 있습니다. Firebase CLI를 쓰지 않는다면 콘솔에 그대로 붙여 넣어도 됩니다.

### Later: Show Public View Counts

Firebase가 연결된 뒤에는 조회수가 Firestore에 계속 쌓입니다. 나중에 화면에 공개하고 싶으면 아래 설정만 켜면 됩니다.

- `config/_default/params.toml`의 `article.showViews = true`
- 필요하면 `list.showViews = true`

`showLikes`는 현재도 꺼져 있습니다. 공개 좋아요 기능이 필요할 때만 별도로 켜면 됩니다.
