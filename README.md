# HWP 뷰어 — 브라우저에서 바로 여는 한글파일 뷰어

**[https://hwp-web.pages.dev](https://hwp-web.pages.dev)**

한글파일(`.hwp`, `.hwpx`)을 설치 없이 브라우저에서 열고, PDF·Word·HTML·텍스트로 내보내는 정적 웹사이트입니다. 이 저장소는 그 사이트의 소스입니다.

## 특징

- **설치가 없습니다.** 웹페이지를 열고 파일을 끌어다 놓으면 끝입니다.
- **파일이 서버로 올라가지 않습니다.** 문서를 읽고 변환하는 작업이 전부 브라우저 안(클라이언트)에서 일어납니다. 업로드 엔드포인트 자체가 없습니다. 이력서·사내 문서처럼 밖으로 나가면 안 되는 파일에 쓸 수 있습니다.
- **서버가 없습니다.** HTML·CSS·JavaScript 정적 파일만으로 동작합니다. 데이터베이스도, 백엔드 API도 없습니다.
- **회원가입이 없습니다.** 로그인도, 사용 횟수 제한도 없습니다.

## 쓰는 법

1. <https://hwp-web.pages.dev> 를 엽니다
2. `.hwp` 또는 `.hwpx` 파일을 화면에 끌어다 놓습니다
3. 내용이 표시되면 PDF · Word(.docx) · HTML · 텍스트 중에서 골라 내려받습니다

데스크톱·모바일 모두 같은 방식입니다. 맥북, 아이폰, 안드로이드에서도 브라우저만 있으면 됩니다.

## 구조

```
index.html        뷰어 본체 — 파일을 읽고 변환하는 화면
guide/            한글파일 사용법 안내 글 (21편)
about/            사이트 소개
privacy/          개인정보처리방침
contact/          문의
_headers          Cloudflare Pages 보안 헤더·캐시 규칙
sitemap.xml       사이트맵
```

변환 라이브러리(`vendor/`)는 각자의 라이선스를 따르는 서드파티 코드라 이 저장소에는 포함하지 않았습니다. 실제 동작은 위 주소에서 확인하실 수 있습니다.

## 가이드 글

사이트를 만들면서 실제로 자주 들어오는 질문들을 정리한 글입니다.

### 기기별로 여는 법

- [한글파일 열기 — 안 열릴 때 기기별로 바로 되는 법](https://hwp-web.pages.dev/guide/open-hwp/)
- [맥북에서 한글파일(hwp) 여는 법](https://hwp-web.pages.dev/guide/mac/)
- [아이폰·아이패드에서 hwp 파일 여는 법](https://hwp-web.pages.dev/guide/iphone/)
- [hwp 뷰어 안드로이드 — 앱 설치 없이 여는 법](https://hwp-web.pages.dev/guide/android/)
- [맥북에서 한글 무료로 쓰는 법 — 되는 것과 안 되는 것](https://hwp-web.pages.dev/guide/mac-free/)

### 변환

- [한글파일 PDF 변환 — 깨짐 없이 저장하는 법](https://hwp-web.pages.dev/guide/pdf/)
- [hwp Word 변환 — 설치 없이 무료로 바꾸는 법](https://hwp-web.pages.dev/guide/word/)
- [한글 표를 엑셀로 옮기기 — 한컴 없이 칸 안 깨지게](https://hwp-web.pages.dev/guide/hwp-to-excel/)
- [PDF를 hwp로 변환하는 법 — 목적별로 갈리는 방법](https://hwp-web.pages.dev/guide/pdf-to-hwp/)
- [맥북에서 hwp를 docx로, docx를 hwp로](https://hwp-web.pages.dev/guide/mac-docx/)
- [hwp 변환 무료 사이트 — 고르기 전에 확인할 세 가지](https://hwp-web.pages.dev/guide/convert-free/)

### 형식과 작성

- [hwp hwpx 차이 — 뭘로 저장해야 하나](https://hwp-web.pages.dev/guide/hwp-vs-hwpx/)
- [hwpx 파일 열기 — 안 열릴 때 hwp로 변환하는 법](https://hwp-web.pages.dev/guide/hwpx/)
- [한글 파일 수정하기 — 한컴 없이 어디까지 되나](https://hwp-web.pages.dev/guide/hwp-edit/)
- [hwp 양식 파일 작성하기 — 받은 양식 채워서 내는 법](https://hwp-web.pages.dev/guide/form-hwp/)
- [공문서 작성법 — 붙임·끝·날짜 표기 규칙](https://hwp-web.pages.dev/guide/official-doc/)
- [한글 쪽번호 매기기 — 안 나올 때 원인별 해결](https://hwp-web.pages.dev/guide/page-number/)
- [한글 목차 점선 넣기 — 원리만 알면 버전 상관없다](https://hwp-web.pages.dev/guide/toc-dots/)
- [한글 자동저장 파일 찾기 — 날린 문서 되찾는 순서](https://hwp-web.pages.dev/guide/autosave/)
- [한글 글자수 세기 — 한컴 없이 브라우저에서](https://hwp-web.pages.dev/guide/char-count/)

[가이드 전체 보기](https://hwp-web.pages.dev/guide/)

## 할 수 있는 것과 없는 것

| | |
|---|---|
| 읽기 | `.hwp`, `.hwpx` — 글·표·목록을 화면에 표시 |
| 내보내기 | PDF · Word(.docx) · HTML · 텍스트 |
| **못 하는 것** | **hwp 파일을 만들어 내는 것.** 읽고 다른 형식으로 내보내는 데까지입니다. hwp로 편집·저장해야 한다면 한컴 공식 제품이 필요합니다 |

복잡하게 병합된 표나 그림이 많은 문서는 간격이 달라질 수 있습니다. 모양이 중요한 문서는 PDF로 내보내 확인하세요.

## 배포

Cloudflare Pages에 정적 파일로 올라갑니다. 빌드 과정이 없습니다.

## 고지

이 프로젝트는 **한글과컴퓨터와 아무 관련이 없습니다.** 「한글」, 「한컴오피스」를 비롯한 제품명은 각 소유자의 상표입니다. 비공식 서드파티 도구입니다.

문서 형식 사양은 한글과컴퓨터가 공개한 HWP 문서 형식 공개 문서를 따릅니다.
