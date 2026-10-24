# site/ — cherrybear.xyz (회사 웹사이트 + 앱별 약관)

GitHub Pages 저장소 `cellist20/cherrybear-site`로 서빙한다. 이 폴더가 원본이고, 배포는 subtree push.

- https://cherrybear.xyz/ — 회사 소개(Play 조직 계정의 "조직 웹사이트")
- https://cherrybear.xyz/unse2027/ — 앱 소개
- https://cherrybear.xyz/unse2027/privacy.html — 개인정보처리방침 (Play·앱 PRIVACY_URL)
- https://cherrybear.xyz/unse2027/terms.html — 이용약관 (앱 TERMS_URL)

```bash
git subtree push --prefix=site site-pages main
# 원격에 GitHub가 만든 CNAME 커밋이 있어 거부되면: 분할 커밋에 site-pages/main을 -s ours로 병합한 뒤 일반 push
```

## DNS (Cloudflare, 계정 marchingwthu@gmail.com) — A·CNAME은 반드시 DNS only(회색 구름)
| 유형 | 이름 | 값 |
|---|---|---|
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |
| CNAME | www | cellist20.github.io |

이메일 `contact@cherrybear.xyz`는 Cloudflare Email Routing(MX·SPF 자동 추가)으로 bearbeer756@gmail.com에 전달한다.

대표자 박영주 (index.html, unse2027/privacy.html, unse2027/terms.html 하단).
새 앱을 내면 `site/<앱>/`에 같은 구조로 추가한다.
