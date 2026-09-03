# Claude Code 변경사항

## GUI App

- 버전: `2.1.259` (이전: `2.1.258`)
- 조직이 `managedMcpServers`로 HTTP/SSE MCP 서버를 모든 사용자에게 배포할 수 있습니다. 명령을 실행하는 항목은 건너뜁니다.
- 무인 헤드리스용 `--permission-prompts none`을 넣었습니다. 프롬프트가 뜰 작업은 자동 거부하고, 활성 권한 모드(auto 포함)는 그대로 결정합니다.
- `glab mr create/merge/close/reopen/note/update`를 인식해 GitLab 머지 리퀘스트를 접힌 도구 요약에서 `MR !N`으로 보여 주고, `claude plugin validate --json`으로 기계 판독 검증 결과를 받습니다.
- 동시 세션이 서로의 `~/.claude.json`을 되돌리던 문제, 한 번 거절된 thinking이 이후 턴마다 다시 거절되던 문제, Bash `Read()` deny가 옵션·리다이렉트·복합 명령을 빠뜨리던 문제를 고쳤습니다.
- 원격·예약 세션이 일시정지 중 커넥터 도구 권한을 승인한 뒤 아무 일도 안 하던 문제와, Remote Control에서 Stop이 백그라운드 에이전트를 실제로 멈추지 않던 문제를 고쳤습니다.
- [VSCode] 세션 목록에 Active 빠른 필터와 상태 필터(Needs input, Working, Completed)를 넣었습니다.
- `allowedMcpServers`는 사용자가 추가한 서버만 걸러 냅니다. 예전 허용 목록에 없던 `managed-mcp.json` 서버는 업그레이드 후 로드되며, 막으려면 `deniedMcpServers`를 씁니다.

## CLI App

- 버전: `2.1.259` (이전: `2.1.258`)
- GUI와 동일 릴리스입니다. 관리 MCP 배포, 무인 권한 거부, GitLab MR 인식, 동시 세션 설정 충돌과 Remote Control Stop 실패를 함께 고쳤습니다.

## Sources

- [Claude Code changelog](https://github.com/anthropics/claude-code/blob/main/CHANGELOG.md)
