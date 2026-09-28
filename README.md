# iamaforeigner web

앱 소개 페이지와 개인정보 처리방침. 빌드 없는 정적 HTML/CSS.

- `index.html` 소개 페이지
- `privacy.html` 개인정보 처리방침 (`[대괄호]` 는 채워야 할 값, 노란색으로 표시됨)
- `styles.css` 소개 페이지 전용 스타일 (`privacy.html` 은 스타일을 파일 안에 인라인으로 가진다)
- `images/` 페이지가 실제로 쓰는 에셋만 둔다 (원본: `iamaforeigner/public/`). 안 쓰는 이미지는 지운다.

디자인(안 C, 「산을 오르는 하루」): 스크롤하면 하늘이 밤 → 새벽 → 낮 → 해질녘 → 밤 정상으로 바뀐다. 남색 `#0C1633` + 등불 금색 `#F4B860`, 글꼴은 Hahmlet(제목) + Gothic A1(본문). 오른쪽 tier 레일은 1100px 이상에서만 보인다.
처리방침은 같은 정체성으로 밤색 헤더 띠 + 종이색 본문(가독성 우선). 외부 JS 없음, 빌드 없음.
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
