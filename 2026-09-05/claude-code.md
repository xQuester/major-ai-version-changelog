# Claude Code 변경사항

## GUI App

- 버전: `2.1.260` (이전: `2.1.259`)
- 전체 화면에서 대화 옆에 미커밋 변경을 보여 주는 diff 패널을 넣었고, `/diff`로 켜고 끕니다.
- `/cost`와 상태줄 `prompt_cache`에 프롬프트 캐시 미스의 가능 원인(도구 정의·시스템 프롬프트 변경, TTL 초과 유휴 등)을 표시합니다.
- 헤드리스 세션에 `/reload-plugins`를 추가했고, 데스크톱·Remote Control·SDK용 `/advisor` 텍스트 형태(`/advisor`, `/advisor `, `/advisor off`)를 넣었습니다.
- Claude apps gateway에 `oidc.scope_on_refresh`와 데스크톱 정책 키(`userPluginMarketplacesEnabled`, `userPluginUploadsEnabled`) 지원을 추가했습니다.
- 경로에 괄호가 있는 `Edit`/`Write`/`Read` 규칙이 무시되던 문제, 컴파일 불가 deny 패턴이 모든 편집을 막던 문제, zsh 변수 대입에 숨긴 명령 치환이 자동 승인되던 문제를 고쳤습니다.
- Bedrock 인증서·macOS 샌드박스 git 설정 숨김·관리 설정이 남은 API 키에 가리던 문제, Fable 5.1 모델 선택·프롬프트 캐시·`/effort` 캐시 무효화를 고쳤습니다.
- `/rewind`가 백업 없이 성공으로 보고하거나 파일 읽기 추적을 남기던 문제, 서브에이전트 `SendMessage` 완료 알림이 메인으로만 가던 문제, 에이전트 팀 트랜스크립트 유실을 고쳤습니다.
- 2.1.259에서 Bash 인자에 Read deny를 적용하던 변경을 되돌렸습니다. build 경로 deny 규칙이 일반 빌드 명령까지 막던 부작용을 없앱니다.
- 전체 화면에서 ctrl+l / cmd+k 는 터미널 clear처럼 트랜스크립트 화면만 비웁니다. 스크롤하면 이전 메시지를 볼 수 있습니다.
- [VSCode] 푸터 모델 pill에 effort 표시, 세션 목록 Open/Closed 필터, Remote Control 자동 켜짐 시 환영 화면 소실, 이미 열린 세션 중복 로드, Rename과 재시도 UI 잔상을 고쳤습니다.

## CLI App

- 버전: `2.1.260` (이전: `2.1.259`)
- GUI와 동일 릴리스입니다. diff 패널, 캐시 미스 원인 표시, 헤드리스 reload-plugins, 권한, Fable, Remote Control, 에이전트 팀 수정을 포함합니다.

## Sources

- [Claude Code changelog](https://github.com/anthropics/claude-code/blob/main/CHANGELOG.md)
