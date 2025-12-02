# Sitemap Planner

사이트맵 기획을 위한 실시간 협업 도구

## 기능

- 📋 페이지 구조 설계 및 관리
- 🌳 계층형 사이트맵 시각화
- 🔄 Firebase 실시간 동기화
- 💾 로컬 저장 (Firebase 없이도 작동)
- 📤 JSON 내보내기

## 빠른 시작

### 로컬에서 실행

1. `index.html` 파일을 브라우저에서 열기
2. 퀴즈 정답 입력: **"통진"**
3. 바로 사용 가능!

### Firebase 실시간 동기화 설정

→ `FIREBASE_SETUP.md` 파일 참고 (3단계, 5분 소요)

### Vercel에 배포

→ `VERCEL_DEPLOY.md` 파일 참고 (2분 소요)

## 파일 구조

```
sitemap-plan/
├── index.html          # 메인 애플리케이션
├── FIREBASE_SETUP.md   # Firebase 설정 가이드
├── VERCEL_DEPLOY.md    # Vercel 배포 가이드
├── vercel.json         # Vercel 설정 파일
└── README.md           # 이 파일
```

## 사용 방법

1. **프로젝트 생성**: 좌측 사이드바에서 "새 프로젝트" 클릭
2. **페이지 추가**: 페이지 정보 입력 후 "페이지 추가" 클릭
3. **계층 구조**: 상위 메뉴를 선택하여 하위 페이지 구성
4. **실시간 동기화**: Firebase 설정 시 여러 브라우저에서 동시 작업 가능
5. **JSON 내보내기**: 헤더의 "JSON 내보내기" 버튼으로 구조 다운로드

## 기술 스택

- HTML5
- JavaScript (Vanilla)
- TailwindCSS
- Firebase Realtime Database

## 라이선스

자유롭게 사용하세요!


