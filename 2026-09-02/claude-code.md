# Claude Code 변경사항

## GUI App

- 버전: `2.1.257` (이전: `2.1.251`)
- 기본 Fable 모델을 Claude Fable 5.1(`claude-fable-5-1`, 1M 컨텍스트)로 바꿨고, 시계용 `timeFormat`/`timeZone`과 세션만 바꾸는 `/effort` `s`를 넣었습니다.
- auto 모드에 Containment Escape 규칙과 작업 디렉터리 밖 첫 파일 읽기 확인을 넣고, `CLAUDE_CODE_SUBAGENT_MODEL_FORCE`로 서브에이전트 모델을 강제합니다.
- `2.1.252`: Mac Bash `task output swap refused`, always allow 미저장, Remote Control 수분 지연, 거대 실패 출력으로 API 한도 초과를 고쳤습니다.
- Remote Control·백그라운드 세션·샌드박스 deny·심링크 플러그인 경로·서브에이전트 스트림 중단 자동 이어가기를 고쳤고, VS Code는 계정/사용량 섹션·모델 pill·세션 Archive를 넣었습니다.

## CLI App

- 버전: `2.1.257` (이전: `2.1.251`)
- GUI와 동일 릴리스입니다. Fable 5.1, 시간 설정, auto 모드 격리, 백그라운드/Remote Control/샌드박스 수정이 함께 들어갔습니다.
- `2.1.252`는 Mac 작업 출력 스왑, always allow, Remote Control 지연, 거대 실패 출력 한도를 고친 패치입니다.

## Sources

- [Claude Code changelog](https://github.com/anthropics/claude-code/blob/main/CHANGELOG.md)
