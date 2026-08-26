# Claude Code 변경사항

## GUI App

- 버전: `2.1.246` (이전: `2.1.245`)
- `/permissions`에 Auto 모드 탭을 넣고, 턴 종료 줄에 완료 시각(예: `done 6:05 PM`)을 표시합니다.
- 전체화면에서 터미널을 리사이즈한 뒤 대화가 비거나 스크롤이 튀던 문제를 고쳤고, 매우 긴 한 줄 diff는 잘라 표시해 느려짐을 줄였습니다.
- `/cd` 직후 새 디렉터리의 프로젝트 설정·훅·MCP·스킬·에이전트가 바로 적용되고, UTC 동쪽 타임존에서 `/stats` 히트맵이 하루씩 밀리던 문제를 고쳤습니다.
- `/rename`이 테마 테두리색을 덮어쓰던 문제와 커스텀 테마 diff 색이 무시되던 문제를 고쳤습니다. VS Code는 플랜 모드로 끝난 세션이 플랜 밖으로 재개되던 문제를 수정했습니다.

## CLI App

- 버전: `2.1.246` (이전: `2.1.245`)
- 서브커맨드 앞 와일드카드 Bash 허용 규칙(예: `Bash(git * main)`)에 시작 경고를 넣고, 끊긴 `&&`/`||` 명령은 항상 승인을 받습니다.
- 끊긴 원격 MCP가 "완료(출력 없음)"으로 보고되던 문제와 빈 스키마 인자가 JSON 문자열로 가던 문제를 고쳤고, 비대화형 세션은 스트림 중단 시 자동 이어갑니다.
- 플러그인 캐시 중복·설치/업데이트·BOM·`/reload-plugins` 스킬 0건을 고치고, 큰 세션에서 자동 모드가 "temporarily unavailable"로 막히던 문제를 완화했습니다.
- 제3자 게이트웨이로 API 키가 텔레메트리에 실리지 않게 했고, `apiKeyHelper` JWT는 만료 전 갱신합니다. 서브에이전트가 `maxTurns`에 닿으면 부분 결과로 돌려줍니다.

## Sources

- [Claude Code changelog](https://github.com/anthropics/claude-code/blob/main/CHANGELOG.md)
