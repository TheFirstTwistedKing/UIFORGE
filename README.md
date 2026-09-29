# Rasyancut UI Forge

Roblox 게임 UI를 브라우저에서 배치·편집하고 Luau 코드로 내보내는 웹 에디터.

## 기능

- 드래그로 이동, 8방향 핸들로 크기 조절
- 편집 단위 전환: Scale / Offset
- 지원 요소: Frame, TextLabel, TextButton, TextBox, ImageLabel, ImageButton, ScrollingFrame
- 속성 편집: Position·Size(UDim2), AnchorPoint, Rotation, 색상, 투명도, ZIndex, Visible, ClipsDescendants, 텍스트·글꼴, 이미지, 스크롤
- UICorner, UIStroke 설정
- Scale ↔ Offset 일괄 변환, 부모 기준 9방향 배치
- 기기 미리보기: 1920×1080 / 1366×768 / 1024×768 / 844×390 / 390×844
- IgnoreGuiInset 미리보기 (상단 바 높이 표시)
- 코드 내보내기: LocalScript / Command Bar / JSON
- 자동 저장, 이름별 저장·불러오기 (브라우저 localStorage)
- JSON 붙여넣기·파일로 불러오기

## 사용법

1. 왼쪽 `삽입`에서 요소 추가 (선택된 요소가 있으면 그 안에 자식으로 추가)
2. 캔버스에서 드래그로 배치, 오른쪽 `속성`에서 값 수정
3. `코드 내보내기`에서 형식 선택 후 복사

| 형식 | 사용 위치 | 결과 |
|---|---|---|
| LocalScript | StarterPlayer › StarterPlayerScripts | 게임 시작 시 PlayerGui에 UI 생성 |
| Command Bar | Studio 보기 탭 › Command Bar | StarterGui에 ScreenGui 생성 |
| JSON | 이 에디터의 `불러오기` | 작업 상태 복원 |

## 단축키

| 키 | 동작 |
|---|---|
| Delete / Backspace | 삭제 |
| Ctrl+D | 복제 |
| Ctrl+Z | 되돌리기 |
| Ctrl+Shift+Z / Ctrl+Y | 다시 |
| 방향키 | 1px 이동 (Shift: 10px) |
| Esc | 선택 해제 |

## 실행

- 빌드 과정 없음. `index.html` 파일 하나로 동작
- 로컬: `index.html`을 브라우저로 열기
- 글꼴은 Google Fonts에서 불러옴 (오프라인이면 기본 글꼴로 표시)

## GitHub Pages 배포

1. 저장소 루트에 `index.html`, `README.md` 업로드
2. 저장소 `Settings` › `Pages`
3. `Source`: Deploy from a branch → Branch: `main` / `/(root)` → `Save`
4. 배포 주소: `https://<사용자명>.github.io/<저장소명>/`

## 파일 구조

```
rasyancut-ui-forge/
├── index.html   # 에디터 전체 (HTML·CSS·JS)
├── README.md
└── .gitignore
```

## 제한 사항

- 미리보기 글꼴은 Roblox 글꼴과 비슷한 웹 글꼴로 대체 (실제 글자 폭과 차이 있음)
- `rbxassetid` 이미지는 미리보기에서 빗금 영역으로 표시
- UIListLayout, UIGridLayout 등 레이아웃 객체 미지원
- 저장 데이터는 사용 중인 브라우저에만 보관 (다른 기기로 옮길 때 JSON 사용)
