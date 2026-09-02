# Claude Code 변경사항

## GUI App

- 버전: `2.1.258` (이전: `2.1.257`)
- macOS 12(Monterey)에서 Claude Code가 실행되지 않던 문제를 고쳤습니다. `2.1.255`에서 생긴 회귀입니다.
- 권한 승인을 다시 보냈을 때 적용되지 않아, 원격·예약 세션이 "user messages must have non-empty content"로 실패하던 문제를 고쳤습니다.

## CLI App

- 버전: `2.1.258` (이전: `2.1.257`)
- GUI와 동일 릴리스입니다. Monterey 실행 실패와 원격·예약 세션의 빈 메시지 오류를 함께 고쳤습니다.

## Sources

- [Claude Code changelog](https://github.com/anthropics/claude-code/blob/main/CHANGELOG.md)
