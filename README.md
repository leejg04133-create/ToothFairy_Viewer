# ToothFairy Viewer

현재 배포 버전: **1.09**

- 실행 파일: [1.09/SkpViewportViewer.exe](1.09/SkpViewportViewer.exe)
- 변경 내역: [1.09/notes.txt](1.09/notes.txt)
- 검증 기록: [1.09/validation.json](1.09/validation.json)
- 자동 업데이트 정보: [latest.json](latest.json)

기존 뷰어의 설정에서 업데이트 확인 → 다운로드 → 다시 시작을 진행합니다.
직접 전달할 때는 `1.09/SkpViewportViewer.exe`를 사용합니다.
`.update-helper.exe`는 업데이트 보조 파일입니다.

## 1.09 변경

회전 시 바뀐 그림자 객체만 갱신하고, 동일 조건의 반복 선택 결과를 재사용하며,
중복된 GPU 상태 전달을 줄였습니다. 실제 Koki 도시 모델에서 MSAA 8배의
화면 비교와 그림자 CPU 갱신 비용 감소를 검증했습니다.
측정 조건·결과·빌드 해시는 검증 기록에 있습니다.

텍스처·그림자 품질과 Live2D를 유지합니다. 그림자 GPU 계산과 첫 선택의
GPU 대기는 남아 있으며, 전체 지연 해소나 친구 PC의 동일 FPS를 뜻하지 않습니다.

## 이후 배포

새 버전 폴더에 내부 버전도 일치하는 `SkpViewportViewer.exe`를 넣고,
`latest.json`의 버전·경로·크기·SHA-256·변경 내역을 함께 갱신합니다.
해당 폴더와 manifest를 커밋하고 GitHub에 푸시하면 업데이트가 표시됩니다.
게시한 EXE를 덮어쓰지 말고 새 버전 번호를 사용합니다.
