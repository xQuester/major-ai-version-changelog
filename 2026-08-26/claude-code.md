# Claude Code 변경사항

## GUI App

- 버전: `2.1.245` (이전: `2.1.241`)
- `2.1.245`는 glibc 2.44를 쓰는 Linux(Arch, CachyOS, Fedora Rawhide 등)에서 시작 시 크래시하던 문제를 고쳤습니다.
- `2.1.243`에서 `/usage`에 루프별 횟수·토큰 분해를 넣고, `/model` 목록을 고르는 `modelPicker`, 프롬프트 캐시 TTL(`promptCacheTtl`/`subagentPromptCacheTtl`), 계약 단가 `modelPricing`을 추가했습니다.
- `/login`에 Anthropic Console 계정으로 키 없이 로그인하는 경로를 더했고, `/status`에 건너뛴 관리 설정 출처와 GitHub 웹 연결 상태를 표시합니다.
- 네이티브 설치를 zstd로 줄이고(Linux x64 약 75 MB), 코드를 필요할 때 불러 세션당 메모리 약 40–70 MB를 줄였습니다. VS Code는 설치 직후 권한 모드와 Focus 뷰가 혼자 접히던 문제를 고쳤습니다.

## CLI App

- 버전: `2.1.245` (이전: `2.1.241`)
- 비대화형(`-p`)·SDK에서 끊긴 원격 MCP가 자동 재연결되고, 데스크톱에서 시작한 MCP 로그인이 "Invalid redirect URI"로 실패하던 문제를 고쳤습니다.
- 자동 모드가 캐시된 일시 비활성·API 과부하 재시도에서 막히던 문제, `/model`의 Ultracode 선택 무시, `/resume` 50개 제한, 네임스페이스·루트리스 컨테이너의 교차 세션 메시징 끊김을 수정했습니다.
- API가 응답을 시작하지 않으면 약 3분 후 한 번 재시도하고 `API Error: No response from API`를 냅니다. `claude --teleport`는 커밋되지 않은 변경이 있으면 stash 후 이어가기를 제안합니다.
- 샌드박스 Bash 프롬프트는 허용 호스트 목록을 더 이상 보여 주지 않으며, macOS 컴퓨터 사용에서 데스크톱·Dock·Finder 클릭은 Finder 권한을 요구합니다. 공식 로그는 GUI와 CLI의 별도 빌드가 아닌 공통 릴리스로 게시합니다.

## Sources

- [Claude Code changelog](https://github.com/anthropics/claude-code/blob/main/CHANGELOG.md)
