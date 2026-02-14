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
