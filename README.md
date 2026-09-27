# iamaforeigner web

앱 소개 페이지와 개인정보 처리방침. 빌드 없는 정적 HTML/CSS.

- `index.html` 소개 페이지
- `privacy.html` 개인정보 처리방침 (`[대괄호]` 는 채워야 할 값, 노란색으로 표시됨)
- `style.css` 공용 토큰(색, 글꼴), 헤더·푸터·폰 목업
- `images/` 페이지가 실제로 쓰는 에셋만 둔다 (원본: `iamaforeigner/public/`). 안 쓰는 이미지는 지운다.

디자인: 흰 바탕 + 강조색 하나(앱 파란색 `#2f66e8`), 글꼴은 IBM Plex Sans KR 한 벌. 외부 JS 없음, 빌드 없음.
개인정보 처리방침 표는 700px 미만에서 행 단위 카드로 바뀐다 — 셀의 `data-label` 이 열 이름이므로 표를 고치면 같이 고칠 것.

## 호스팅

GitHub Pages, `main` 브랜치 루트에서 배포 (Settings → Pages → Deploy from a branch → `main` / `/ (root)`).
`.nojekyll` 이 있어 Jekyll 처리를 건너뛴다. 모든 경로는 상대 경로라 `https://<user>.github.io/<repo>/` 하위 경로에서도 동작한다.

커스텀 도메인은 아직 정하지 않아 `CNAME` 파일이 없다. 정하면 루트에 `CNAME` 추가.

## Play Console 에 등록할 URL

- 개인정보 처리방침: `<사이트 URL>/privacy.html`
- 계정 삭제 요청: `<사이트 URL>/privacy.html#delete-account`

## 로컬 미리보기

```
python3 -m http.server 8000
```
