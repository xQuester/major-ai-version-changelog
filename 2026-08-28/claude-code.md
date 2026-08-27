# Claude Code 변경사항

## GUI App

- 버전: `2.1.247` (이전: `2.1.246`)
- 세션에서 문제가 나면 Claude가 `/feedback` 초안을 잡아 주고(`feedbackDrafts`로 끔), 조직은 `spinnerTipsOverride`로 자체 팁을 돌릴 수 있습니다.
- Bash 권한 프롬프트에 Auto 모드로 바꾸는 한 키 옵션을 넣었고, `/claude-api cost-optimize`와 Admin API 스킬을 추가했습니다.
- 화살표+Enter가 한 줄 위를 고르던 문제, 비라틴 레이아웃 Ctrl 단축키, 잘린 마우스 리포트 쓰레기 문자, Zed `keymap.json` 전체 덮어쓰기를 고쳤습니다.
- `/rename` 실패를 침묵하지 않고, 백그라운드 세션의 무한 "opening…", 클라우드 권한 모드·컨테이너 재시작 침묵을 수정했습니다. 교차 세션 메시지는 한 줄 미리보기로 접힙니다.

## CLI App

- 버전: `2.1.247` (이전: `2.1.246`)
- 서브에이전트 첫 호출 모델 404는 세션 폴백을 쓰고, 훅·백그라운드 에이전트의 거대 오류가 대화를 넘치던 문제를 막았습니다.
- 샌드박스 정리가 심링크된 `~/.claude/settings.json`을 지우던 문제와, 출력 파일 쓰기 실패 시 메모리 폭주를 고쳤습니다.
- 버전 없는 마켓플레이스 플러그인 캐시 재생성, Remote Control 작업 트리 diff 미보고, self-hosted runner의 조기 `running`을 수정했습니다.
- Bedrock·Vertex·Foundry에서 MCP 연결 실패를 모델에 알리고, Sonnet 5 1M 창 auto-compact를 약 967K로 올렸습니다. 관리 설정을 못 읽으면 조직 로그인을 시작 시 종료합니다.

## Sources

- [Claude Code changelog](https://github.com/anthropics/claude-code/blob/main/CHANGELOG.md)
