# 📝 Toast Editor for Next.js (TypeScript)

Next.js 환경에 최적화된 Toast UI Editor 통합 패키지입니다.  
SSR 환경에서도 안정적으로 동작하며, 다국어 지원과 플러그인 확장이 가능하도록 커스터마이징 되어 있습니다.

---

## 🧪 개발자 노트 (Developer Notes)

### 🎯 프로젝트 목표
- Toast UI Editor를 Next.js 기반 웹 프로젝트에 쉽게 통합할 수 있도록 구성
- 소규모 SaaS 프로젝트에서도 바로 적용 가능한 에디터 패키지 제공

### 🛠 주요 기능 요약
- **SSR 대응**: `next/dynamic`을 통한 클라이언트 전용 로딩 처리
- **다국어 지원**: 한국어, 영어, 베트남어 전환 및 브라우저 언어 자동 감지
- **툴바 커스터마이징**: 불필요한 툴 제거, 커스텀 버튼 추가 가능
- **이미지 업로드**: `/api/upload` 라우트 기반 서버 업로드 처리
- **폰트 설정**: 사용자 선택에 따라 폰트 실시간 반영
- **플러그인 추가**: 이모지, 유튜브 삽입, 날짜 삽입 등 예시 포함

### 🧩 커스터마이징 가이드
- `components/plugins/` 디렉토리에서 플러그인 정의 가능
- `i18n.ts`에 다국어 라벨 추가 및 확장 가능
- `ToastEditor` 컴포넌트에서 `toolbar`, `plugins` 배열로 확장성 확보

### 📝 개발 환경
- **Next.js 13+**
- **TypeScript**
- **Toast UI Editor v3+**
- **Vercel 또는 로컬 서버 기반 배포 테스트 완료**

---

## 🚀 설치 및 사용법

```bash
npm install toast-editor-next
```

```tsx
import ToastEditor from 'toast-editor-next/components/ToastEditor';
```

---

## 📦 NPM 배포

```bash
npm login
npm publish --access public
```

`package.json` 예시:
```json
{
  "name": "toast-editor-next",
  "version": "1.0.0",
  "main": "components/ToastEditor.tsx",
  "types": "components/ToastEditor.tsx",
  "scripts": {
    "dev": "next dev",
    "build": "next build",
    "start": "next start",
    "vercel-build": "npm install --legacy-peer-deps && next build"
  },
  "license": "MIT",
  "dependencies": {
    "next": "^13.4.19",
    "react": "17.0.2",
    "react-dom": "17.0.2",
    "@toast-ui/react-editor": "^3.2.3",
    "@toast-ui/editor": "^3.2.2",
    "multer": "^1.4.5"
  }
}
```

---

## 📸 데모 생성 가이드
- [Screen Studio](https://screen.studio/) 또는 [LICEcap](https://www.cockos.com/licecap/) 사용 추천
- `public/demo.gif` 저장 후 README에 이미지 삽입

```md
![demo](./public/demo.gif)
```

---

## 🙏 참고 및 기여
- 기반 에디터: [Toast UI Editor](https://github.com/nhn/tui.editor)
- 이 프로젝트는 오픈소스로 누구나 기여 및 포크 가능

---

## 📄 라이선스
MIT © 2025