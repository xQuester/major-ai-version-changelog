# Claude Code 변경사항

## GUI App

- 버전: `2.1.251` (이전: `2.1.247`)
- `PreModelSwitch`/`PostModelSwitch` 훅으로 모델 전환을 막거나 확인·주석할 수 있고, Remote Control은 포그라운드 서브에이전트 도구 호출을 실시간으로 봅니다.
- `/usage`에 Spend limit 바, `/cost`에 세션별 프롬프트 캐시(히트율·miss·재캐시)를 넣었고, `claude --help`에 `attach`/`logs`/`stop`/`respawn`/`rm`이 보입니다.
- `2.1.248`: `--restricted`로 명령·코드 실행·WebFetch를 빼고 작업 디렉터리 파일 도구만 남기며, `experimental.cacheTtl`, self-hosted runner `--client-label`, 서버 관리 설정 진단, Enterprise `/usage-credits`, Bedrock·Vertex·Foundry 교차 세션 메시지를 추가했습니다.
- 권한 검사 뒤 바뀐 심링크·플러그인 경로 탈출·워크플로 `scriptPath`·Grep/Glob deny 우회를 막고, thinking만 있는 턴 후 빈 텍스트 블록 고착·에이전트 팀 최종 답 유실·백그라운드 worktree 편집 불가 등을 고쳤습니다.
- VS Code Remote Control 배너를 푸터 pill로 바꿨고, 바이너리는 약 5MB·하이라이트 축소로 더 작아졌으며 인터랙티브 턴 CPU도 줄였습니다.

## CLI App

- 버전: `2.1.251` (이전: `2.1.247`)
- GUI와 동일 릴리스입니다. 모델 전환 훅, 캐시/`/usage` 지표, `--restricted`, 교차 세션·Remote Control·샌드박스·훅 신뢰성 수정이 함께 들어갔습니다.
- `2.1.250`은 버그 수정·안정성만 반영했습니다.

## Sources

- [Claude Code changelog](https://github.com/anthropics/claude-code/blob/main/CHANGELOG.md)
