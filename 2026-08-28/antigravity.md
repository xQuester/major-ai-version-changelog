# Antigravity 변경사항

## GUI App

- 버전: `2.11.0` (이전: `2.10.0`, 2026-08-26 공개)
- 생성형 UI로 HTML 아티팩트를 채팅에 인라인으로 그립니다. `AGENTS.md`와 규칙 파일에서 `@path/to/file`을 넣고, YAML 프론트매터는 메타데이터 카드로 보여 줍니다.
- 생성형 UI·아티팩트 미리보기에 KaTeX, Chart.js, Plotly를 쓰고, 터미널을 나란히 분할하며 Darcula 테마를 추가했습니다.
- `view_file`에 페이지 범위·이미지 해상도, 스킬 칩 호버 미리보기, 에이전트 프론트매터 `rules:`와 하위 디렉터리 `skills.json`·`agents.json`·`rules.json`을 넣었습니다.
- 이미지 첨부 유실, WIF 1시간 로그아웃, 마이그레이션 후 권한 규칙 무시, ADC "크레딧 부족" 오표시를 고쳤습니다. 공식 페이지는 점진 배포를 안내하므로 실제 업데이트 도달까지 며칠 걸릴 수 있습니다.

## IDE App

- 버전: `2.5.5`
- 이전 기록 이후 새 IDE 버전은 확인되지 않았습니다.

## CLI App

- 제품 탭: `2.0`, 바이너리: `1.1.22` (이전 바이너리: `1.1.21`, 2026-08-26 공개)
- `/model <이름>`으로 모델을 바꾸고 고스트 완성을 쓰며, `/effort` 힌트는 입력에 맞춰 완성됩니다. 아티팩트가 많이 생길 때 파일시스템 이벤트를 한데 묶습니다.
- Gemini API 키로 Gemini 3.1 Pro·3.5 Flash의 reasoning effort를 고를 수 있고, 유휴 CPU 재그리기, HTTP 502 재시도, Windows 삭제 공유 위반을 고쳤습니다.
- 공식 페이지는 점진 배포를 안내하므로 실제 업데이트 도달까지 며칠 걸릴 수 있습니다.

## Sources

- [Google Antigravity changelog](https://antigravity.google/changelog)
