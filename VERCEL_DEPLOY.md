# Vercel 배포 가이드

## 간단 배포 (2분 완료)

### 방법 1: Vercel 웹사이트에서 배포 (추천)

1. [Vercel](https://vercel.com) 접속 → GitHub 계정으로 로그인
2. **"Add New..."** → **"Project"** 클릭
3. GitHub 저장소 선택 또는 **"Import Git Repository"** 클릭
4. 프로젝트 설정:
   - Framework Preset: **Other** 또는 **Vite** 선택
   - Root Directory: `.` (현재 폴더)
   - Build Command: 비워두기 (정적 파일만)
   - Output Directory: `.` 또는 비워두기
5. **"Deploy"** 클릭
6. 완료! 🎉 (약 1분 소요)

### 방법 2: Vercel CLI로 배포

```bash
# Vercel CLI 설치
npm i -g vercel

# 프로젝트 폴더에서 실행
vercel

# 처음이면 로그인 후 배포
# 이후에는 vercel --prod 로 프로덕션 배포
```

---

## 배포 후 확인

배포가 완료되면:
- Vercel이 자동으로 URL 제공 (예: `your-project.vercel.app`)
- 이 URL을 다른 사람과 공유하면 실시간 동기화 가능!

---

## 주의사항

⚠️ **Firebase 설정 필수**
- Vercel에 배포하기 전에 `index.html`의 Firebase 설정을 완료해야 합니다
- Firebase 설정 없이 배포하면 localStorage만 작동합니다

---

## 커스텀 도메인 연결 (선택사항)

1. Vercel 대시보드 → 프로젝트 선택
2. **Settings** → **Domains**
3. 원하는 도메인 입력
4. DNS 설정 안내에 따라 도메인 연결


