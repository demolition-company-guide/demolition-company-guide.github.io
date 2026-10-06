# 철거 선택 노트

철거업체를 비교할 때 공사 범위, 견적 포함 항목, 안전 계획, 폐기물 처리와 인계 상태를 확인하도록 돕는 독립적인 정보형 정적 사이트입니다. 실제 업체나 시공 실적을 소개하지 않습니다.

## 사이트 정보

| 항목 | 값 |
| --- | --- |
| 메인키워드 | 철거업체 |
| Organization | `demolition-company-guide` |
| Repository | `demolition-company-guide.github.io` |
| GitHub Pages | https://demolition-company-guide.github.io/ |

이 폴더의 파일은 빌드 과정 없이 GitHub Pages에서 바로 작동합니다. `index.html`, `style.css`, `robots.txt`, `sitemap.xml`, `404.html`, `favicon.svg`, 아래 IndexNow 키 파일을 모두 Repository 최상단에 두세요.

## GitHub 업로드와 Pages 활성화

1. GitHub에서 Organization `demolition-company-guide`와 공개 Repository `demolition-company-guide.github.io`를 준비합니다.
2. ZIP을 풀고 **ZIP 안의 파일들**을 Repository 최상단에 업로드합니다. ZIP 자체나 별도의 상위 폴더만 올리지 않습니다.
3. Repository의 **Settings → Pages → Build and deployment**에서 **Deploy from a branch**를 선택합니다.
4. Branch를 업로드한 기본 브랜치(보통 `main`), Folder를 `/ (root)`로 설정하고 저장합니다.
5. https://demolition-company-guide.github.io/ 에 접속해 첫 화면과 스타일을 확인합니다.

## 네이버 IndexNow

| 항목 | 값 |
| --- | --- |
| 키값 | `6098c1a534e84c04b7449749e10f5c55` |
| 키 파일명 | `6098c1a534e84c04b7449749e10f5c55.txt` |
| 키 파일 확인 URL | https://demolition-company-guide.github.io/6098c1a534e84c04b7449749e10f5c55.txt |
| 요청 URL | https://searchadvisor.naver.com/indexnow?url=https://demolition-company-guide.github.io/&key=6098c1a534e84c04b7449749e10f5c55 |

1. GitHub Pages 배포가 끝난 뒤 키 파일 확인 URL을 엽니다.
2. 화면에 키값 `6098c1a534e84c04b7449749e10f5c55`만 표시되는지 확인합니다.
3. 키 파일이 404라면 파일 위치와 Pages 배포를 먼저 고칩니다.
4. 키 파일이 정상일 때 위 IndexNow 요청 URL을 주소창에서 실행합니다.

Chrome에서 HTTP 상태를 확인하려면 **F12 → Network**를 열고, 필요하면 **Preserve log**를 켠 뒤 주소창에서 요청 URL을 직접 실행합니다. Network 목록의 `indexnow?...` 요청을 선택하고 **Headers → Status Code**를 확인합니다. 기존 사이트 화면에서 새로고침하는 것만으로는 이 요청의 상태를 확인할 수 없습니다.

| 상태 | 의미 |
| --- | --- |
| 200 | 정상 전송 |
| 202 | 접수 후 키 확인 중 |
| 400 | 요청 형식 오류 |
| 403 | 키 확인 실패 가능성 |
| 422 | URL과 키 정보 불일치 가능성 |
| 429 | 요청 과다 |
| 500 | 서버 오류 |

IndexNow 요청은 URL 변경 사실을 알리는 절차이며 검색 색인이나 검색 순위를 보장하지 않습니다. 키 파일은 ZIP에 포함되어 있으나, GitHub Pages 배포 후 온라인 확인이 필요합니다.
