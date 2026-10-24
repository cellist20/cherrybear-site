# site/ — cherrybear.xyz (회사 웹사이트 + 앱별 약관)

GitHub Pages 저장소 `cellist20/cherrybear-site`로 서빙한다. 이 폴더가 원본이고, 배포는 subtree push.

- https://cherrybear.xyz/ — 회사 소개(Play 조직 계정의 "조직 웹사이트")
- https://cherrybear.xyz/unse2027/ — 앱 소개
- https://cherrybear.xyz/unse2027/privacy.html — 개인정보처리방침 (Play·앱 PRIVACY_URL)
- https://cherrybear.xyz/unse2027/terms.html — 이용약관 (앱 TERMS_URL)

```bash
git subtree push --prefix=site site-pages main
```

## DNS (도메인 등록기관에서 설정)
| 유형 | 이름 | 값 |
|---|---|---|
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |
| CNAME | www | cellist20.github.io |
| MX | @ | mx1.improvmx.com (우선순위 10) |
| MX | @ | mx2.improvmx.com (우선순위 20) |
| TXT | @ | v=spf1 include:spf.improvmx.com ~all |

이메일 `contact@cherrybear.xyz`는 ImprovMX(무료 포워딩)로 bearbeer756@gmail.com에 전달한다.

`[대표자명]` 자리는 사업자등록증의 대표자 성명으로 채운다(index.html, unse2027/privacy.html, unse2027/terms.html).
새 앱을 내면 `site/<앱>/`에 같은 구조로 추가한다.
