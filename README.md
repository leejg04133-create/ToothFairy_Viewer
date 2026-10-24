# ToothFairy Viewer

현재 배포 버전: **1.13**

- 실행 파일: [1.13/SkpViewportViewer.exe](1.13/SkpViewportViewer.exe)
- 변경 내역: [1.13/notes.txt](1.13/notes.txt)
- 검증 기록: [1.13/validation.json](1.13/validation.json)
- 자동 업데이트 정보: [latest.json](latest.json)

기존 뷰어의 설정에서 업데이트 확인 → 다운로드 → 다시 시작을 진행합니다.
직접 전달할 때는 `1.13/SkpViewportViewer.exe`를 사용합니다.
`.update-helper.exe`는 업데이트 보조 파일입니다.

## 1.13 변경

그림자 방향 조작 중 화면 뒤에 가려진 면의 불필요한 GPU 광선 검사를 줄였습니다.
Done 이후 카메라 이동 시 수동 그림자 방향이 돌아가던 문제의 수정도 포함합니다.
텍스처·그림자 품질과 Live2D를 유지합니다.

실제 Koki 도시 모델, MSAA 8배 검사에서 10개 방향의 수정 전후 픽셀이 일치했습니다.
1920×1000에서 장면과 미리보기의 렌더링 완료 시간은 약 189ms → 135ms로 감소했습니다.
이 수치는 로컬 GPU 렌더링 검사 결과이며 전체 앱 입력 지연이나 다른 PC의 FPS를 뜻하지 않습니다.
본 장면 렌더링 비용은 남아 있습니다. 자세한 측정 조건과 빌드 해시는 검증 기록에 있습니다.

## 이후 배포

새 버전 폴더에 내부 버전도 일치하는 `SkpViewportViewer.exe`를 넣고,
`latest.json`의 버전·경로·크기·SHA-256·변경 내역을 함께 갱신합니다.
해당 폴더와 manifest를 커밋하고 GitHub에 푸시하면 업데이트가 표시됩니다.
게시한 EXE를 덮어쓰지 말고 새 버전 번호를 사용합니다.
