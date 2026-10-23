# ToothFairy Viewer

현재 배포 버전: **1.08**

- 실행 파일: [1.08/SkpViewportViewer.exe](1.08/SkpViewportViewer.exe)
- 변경 내역: [1.08/notes.txt](1.08/notes.txt)
- 검증 기록: [1.08/validation.json](1.08/validation.json)
- 자동 업데이트 정보: [latest.json](latest.json)

기존 뷰어의 설정에서 업데이트 확인 → 다운로드 → 다시 시작을 진행합니다.
직접 전달할 때는 `1.08/SkpViewportViewer.exe`를 사용합니다.
`.update-helper.exe`는 업데이트 보조 파일입니다.

## 1.08 변경

선택 표시의 깊이 생성에 표시 대상 목록을 재사용하고, 이동·회전 중 숨겨진
부품 분류와 임시 메모리 할당, 화면 깊이 버퍼 중복 작업을 줄였습니다.
MSAA 8배 픽셀 비교와 실제 대형 SKP 동일 조건 비교를 통과했습니다.
상세 측정 조건·결과·빌드 해시는 검증 기록에 있습니다.

텍스처·그림자 품질과 Live2D를 유지합니다. 그림자를 켠 상태의 GPU 비용은
남아 있으며, 친구 PC의 성능 개선은 아직 실측하지 않았습니다.

## 이후 배포

새 버전 폴더에 내부 버전도 일치하는 `SkpViewportViewer.exe`를 넣고,
`latest.json`의 버전·경로·크기·SHA-256·변경 내역을 함께 갱신합니다.
해당 폴더와 manifest를 커밋하고 GitHub에 푸시하면 업데이트가 표시됩니다.
게시한 EXE를 덮어쓰지 말고 새 버전 번호를 사용합니다.
