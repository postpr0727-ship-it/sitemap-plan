# Firebase 보안 규칙 설정 가이드

## ⚠️ "PERMISSION_DENIED" 오류 해결하기

이 오류는 Firebase Realtime Database의 보안 규칙이 쓰기를 차단할 때 발생합니다.

## 빠른 해결 방법 (1분)

### 1단계: Firebase Console 접속
1. [Firebase Console](https://console.firebase.google.com) 접속
2. 프로젝트 선택 (`sitemap-9177c`)

### 2단계: Realtime Database 규칙 수정
1. 왼쪽 메뉴에서 **"Realtime Database"** 클릭
2. 상단 탭에서 **"규칙"** 클릭

### 3단계: 규칙 입력
다음 규칙을 복사해서 붙여넣기:

```json
{
  "rules": {
    "sitemapProjects": {
      ".read": true,
      ".write": true
    }
  }
}
```

### 4단계: 게시
1. **"게시"** 버튼 클릭
2. 확인 메시지에서 **"게시"** 클릭

### 5단계: 확인
브라우저를 새로고침하고 다시 저장해보세요!

---

## 규칙 설명

```json
{
  "rules": {
    "sitemapProjects": {
      ".read": true,   // 모든 사용자가 읽기 가능
      ".write": true   // 모든 사용자가 쓰기 가능
    }
  }
}
```

- `sitemapProjects`: 우리 앱이 사용하는 데이터 경로
- `.read: true`: 누구나 읽을 수 있음
- `.write: true`: 누구나 쓸 수 있음

---

## 더 안전한 규칙 (선택사항)

나중에 인증을 추가하고 싶다면:

```json
{
  "rules": {
    "sitemapProjects": {
      ".read": "auth != null",
      ".write": "auth != null"
    }
  }
}
```

이 규칙은 로그인한 사용자만 읽기/쓰기를 허용합니다.

---

## 문제 해결

**규칙을 수정했는데도 오류가 나와요**
1. 규칙을 저장했는지 확인 (게시 버튼 클릭)
2. 브라우저를 완전히 새로고침 (Ctrl+F5 / Cmd+Shift+R)
3. Firebase Console에서 규칙이 올바르게 저장되었는지 확인

**여전히 안 돼요**
- Firebase Console → Realtime Database → 데이터 탭에서 데이터가 저장되는지 확인
- 브라우저 개발자 도구(F12) → Console에서 정확한 오류 메시지 확인

