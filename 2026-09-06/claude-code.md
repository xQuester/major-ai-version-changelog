# Claude Code 변경사항

## GUI App

- 버전: `2.1.261` (이전: `2.1.260`)
- `/status`와 `claude doctor`에 조직 정책을 불러오지 못한 이유를 보여주는 Organization policy 줄을 넣었습니다.
- `bashOutputMaxChars`·`taskOutputMaxChars` 설정으로 명령·백그라운드 작업 출력을 파일로 넘기기 전 인라인으로 받을 양을 최대 128K까지 올릴 수 있습니다.
- `--append-subagent-system-prompt-file`로 너무 긴 서브에이전트 시스템 프롬프트를 파일에서 읽을 수 있고, `/skill-doctor`로 안 쓰이는 스킬과 컨텍스트 비용을 볼 수 있습니다.
- 빠른 입력·키 반복 때 글자가 뒤섞이거나 빠지던 문제, `/net` 오토마운트에서 `/add-dir` 오탐, Bedrock 설정 마법사 응답 없음·TLS 검사 프록시 모델 확인 실패를 고쳤습니다.
- 관리 설정이 강제 켠 플러그인을 클라우드 세션이 버리고 마켓플레이스 클론으로 떨어지던 문제, 인라인 `[Image #N]` 바로 앞 글자 삭제 실패, 병렬 도구 호출 주변 훅 출력을 resume이 잃던 문제를 고쳤습니다.
- Remote Control의 권한 모드·작업 중 표시·`/teleport` 업로드·TLS 프록시 이벤트 스트림·effort 표시를 고쳤고, SDK·클라우드에서 첫 프롬프트 직후 Stop이 무시되던 문제도 고쳤습니다.
- `gcpAuthRefresh`의 불필요한 브라우저 열림, 커넥터 타임아웃 후 백그라운드 재시도, 재개 불가 백그라운드 에이전트의 CPU 루프, 구버전에도 새 버전 플래그가 적용되던 문제를 고쳤습니다.
- `/usage` 주간 한도 행 누락, 잘못된 resume 세션 ID, 백그라운드 작업 중에도 끝난 것처럼 보이던 터미널 진행 표시, 레이아웃 높이 오류를 고쳤습니다.
- Claude apps gateway의 `X-Forwarded-For` 포트 처리·Desktop OTEL 형식, Desktop/웹의 아티팩트 감시만 하는 세션 busy 표시, Chrome `file_upload` 경로 오류, 오프라인 Remote Control `SendMessage` 전달 표시를 고쳤습니다.
- 백그라운드 Bash의 플러그인 설치 힌트 태그 유출, 에이전트 팀 동료의 첫 턴 도구·스킬 재공지(프롬프트 캐시 미스), `/model`·VS Code 모델 pill의 Bedrock/Vertex/게이트웨이 원문 ID 표시를 개선했습니다.
- Vertex 시작 시 불필요한 프로젝트 탐색·`gcloud` 스폰을 줄였고, 이미 그린 블록의 레이아웃 재검사를 줄여 스트리밍을 빠르게 했습니다.
- 위험한 `rm -rf` 안전 프롬프트가 위치 인자·따옴표 안 `sh -c`도 잡고, API 헤더 없음 재시도는 기본 최대 10분(`API_TIMEOUT_MS`)까지 기다립니다.
- 게이트웨이 managed settings 403은 조직에 Claude Code가 꺼져 있을 수 있다고 안내하고, `forceLoginMethod: "gateway"` 기기는 남은 API 키·claude.ai 로그인을 무시하고 `/login`을 요구합니다.
- 공개 다이어그램 렌더러 URL에 내용을 실은 링크는 업로드로 취급해 요청하지 않으면 auto mode에서 자동 승인하지 않습니다.
- 프롬프트 단어 편집 키는 Bash와 같게 바뀌었고(`Ctrl+W`, `Alt+F`/`Alt+D`), `keybindingFlavor`는 더 이상 효과가 없습니다. `/context`는 토큰 계산 API가 없으면 로컬 추정으로 셉니다.
- [VSCode] Output styles에 커스텀 스타일 만들기 안내, MCP 서버 추가·제거 UI, 다른 창·터미널·Desktop에 열린 세션용 빈 링, 권한·질문 접기, 세션 Archive를 넣었습니다.
- [VSCode] Rename 빈 상자, 접힌 섹션 깜빡임, Focus view 도구 실행 잔상, 탭·그룹·모델 피커·`/btw`·질문 카드·로그인 프롬프트·권한 큐·사용량 미터·Remote Control 토글·Open 필터 등 다수를 고쳤고, 모델 피커는 한 목록으로 합쳤습니다.

## CLI App

- 버전: `2.1.261` (이전: `2.1.260`)
- GUI와 동일 릴리스입니다. 조직 정책 진단, 출력 한도 설정, 서브에이전트 프롬프트 파일, `/skill-doctor`, Remote Control·권한·Vertex·스트리밍·자동 승인 규칙 수정을 포함합니다.

## Sources

- [Claude Code changelog](https://github.com/anthropics/claude-code/blob/main/CHANGELOG.md)
