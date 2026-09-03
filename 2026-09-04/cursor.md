# Cursor 변경사항

## GUI App

- 버전: `3.11`
- 2026-09-02에 버전 번호 없는 새 기능 공지가 게시되었습니다. 도구 실행을 자체 네트워크 안의 **셀프 호스팅 machines**에서 처리할 수 있습니다. 코드베이스·빌드 산출물·시크릿은 내부 머신에 남고, 도구 호출은 에이전트가 로컬에서 처리합니다.
- My Machines는 노트북이나 VM 한 대를 계정에 연결하고, Team pools는 이름을 붙인 worker 대기열입니다. 요청이 오면 늘고 연결이 끊기면 줄어들며, 유휴 머신은 최대 절전 후 재연결 창 안에서 복원할 수 있습니다. Pools는 특정 리포지토리에 묶이지 않습니다.
- 클라우드 Agent를 이미 쓰는 인프라에서 실행할 수 있습니다. AWS Lambda, Coder, Cloudflare, Daytona, Modal, Namespace, Vercel, E2B를 지원합니다.
- 셀프 호스팅 worker가 Linux와 Mac에서 컴퓨터 사용을 지원합니다. 데스크톱 패키지가 있으면 클릭·입력·스크린샷·브라우저 조작을 하고, 에이전트 데스크톱을 보거나 Cursor에서 제어권을 가져올 수 있습니다. 공지에 새 GUI 버전 번호는 없으므로 버전 기준선은 유지합니다.

## CLI App

- Cursor는 이 변경 로그에서 별도 CLI 버전을 게시하지 않습니다.
- 이전 기록 이후 새 CLI 공지는 확인되지 않았습니다.

## Sources

- [Cursor changelog](https://cursor.com/ko/changelog)
