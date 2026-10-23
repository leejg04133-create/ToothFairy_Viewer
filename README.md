# ToothFairy Viewer

현재 배포 버전: **1.06**

- 실행 파일: [1.06/SkpViewportViewer.exe](1.06/SkpViewportViewer.exe)
- 변경 내역: [1.06/notes.txt](1.06/notes.txt)
- 검증 기록: [1.06/validation.json](1.06/validation.json)
- 자동 업데이트 정보: [latest.json](latest.json)

기존 뷰어의 설정에서 업데이트 확인 → 다운로드 → 다시 시작을 진행합니다.
직접 전달할 때는 `1.06/SkpViewportViewer.exe`를 사용합니다.
`.update-helper.exe`는 업데이트 보조 파일입니다.

## 1.06 변경

대형 모델의 객체 상태 검사, 카메라 깊이 계산, 인스턴스 준비, GPU 설정과
화면 갱신 준비의 중복 작업을 줄였습니다. SDK 텍스처를 중간 이미지로
변환하는 비용도 줄였습니다. 로컬 동일 도시 모델에서 텍스처 읽기는 평균
16.59초에서 13.59초로 줄었으며 텍스처·알파 비교와 SDK 회귀 검사를 통과했습니다.

텍스처 해상도·그림자 품질·Live2D 로딩을 유지합니다. 기존 DPI별 MSAA 선택
정책도 유지합니다. 위 수치는 해당 로컬 측정 구간이며 앱 전체 FPS나
친구 PC의 모든 지연 해결을 의미하지 않습니다. 이전 업데이트 복구를 포함합니다.

## 이후 배포

새 버전 폴더에 내부 버전도 일치하는 `SkpViewportViewer.exe`를 넣고,
`latest.json`의 버전·경로·크기·SHA-256·변경 내역을 함께 갱신합니다.
해당 폴더와 manifest를 커밋하고 GitHub에 푸시하면 업데이트가 표시됩니다.
게시한 EXE를 덮어쓰지 말고 새 버전 번호를 사용합니다.
