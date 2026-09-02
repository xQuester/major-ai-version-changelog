# Antigravity 변경사항

## GUI App

- 버전: `2.11.0`
- 이전 기록 이후 새 GUI 버전은 확인되지 않았습니다.

## IDE App

- 버전: `2.5.5`
- 이전 기록 이후 새 IDE 버전은 확인되지 않았습니다.

## CLI App

- 제품 탭: `2.0`, 바이너리: `1.1.23` (이전: `1.1.22`)
- `/model` 자동완성에서 Tab으로 제안 모델명을 받을 수 있고, 서브에이전트 스트리밍 메타데이터 전송을 줄였습니다.
- 서브커맨드 stdin 멈춤, prompt hook 크래시, Gemini 요청 히스토리의 tool-call ID 누락, MCP 도구 권한 제목, 로그인 직후 프롬프트 유실, 취소된 서브에이전트 Running 고착, Windows BOM JSON 파싱을 고쳤습니다.
- `enable_mcp_tools=true` 서브에이전트에 MCP dispatcher가 없어 실패하던 문제를 고쳤고, OAuth 토큰을 만료 5분 전에 미리 갱신합니다.

## Sources

- [Google Antigravity changelog](https://antigravity.google/changelog)
