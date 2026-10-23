# ToothFairy Viewer

현재 배포 버전: **1.07**

- 실행 파일: [1.07/SkpViewportViewer.exe](1.07/SkpViewportViewer.exe)
- 변경 내역: [1.07/notes.txt](1.07/notes.txt)
- 검증 기록: [1.07/validation.json](1.07/validation.json)
- 자동 업데이트 정보: [latest.json](latest.json)

기존 뷰어의 설정에서 업데이트 확인 → 다운로드 → 다시 시작을 진행합니다.
직접 전달할 때는 `1.07/SkpViewportViewer.exe`를 사용합니다.
`.update-helper.exe`는 업데이트 보조 파일입니다.

## 1.07 변경

선택 후보와 선택 면 검색, 변환 비교, 장면·깊이·그리기 대상·조명 재사용,
내보내기 준비·텍스처 메모리 계산·HUD 그리기 등 15개 중복 작업을 개선했습니다.
상세 항목은 변경 내역에, 검증 결과와 빌드 해시는 검증 기록에 들어 있습니다.

텍스처 해상도·알파·그림자 품질과 Live2D 로딩을 유지합니다.
기존 DPI별 MSAA 선택 정책은 유지합니다. 로컬 회귀 검사는 통과했으며
친구 PC에서의 FPS 개선은 아직 실측하지 않았습니다. 기존 업데이트 복구도 포함합니다.

## 이후 배포

새 버전 폴더에 내부 버전도 일치하는 `SkpViewportViewer.exe`를 넣고,
`latest.json`의 버전·경로·크기·SHA-256·변경 내역을 함께 갱신합니다.
해당 폴더와 manifest를 커밋하고 GitHub에 푸시하면 업데이트가 표시됩니다.
게시한 EXE를 덮어쓰지 말고 새 버전 번호를 사용합니다.
