# Degine Design System v1.0

디자인 스튜디오 Degine의 토큰·컴포넌트 규칙입니다. 라이브 가이드는 `index.html`을 브라우저로 열어 확인합니다.

## 구조
| 파일 | 역할 |
|---|---|
| `src/tokens.css` | 컬러·타입·간격·모션 토큰 (라이트/다크) |
| `src/components.css` | 리셋, 타이포 클래스, 레이아웃, 컴포넌트 |
| `index.html` | 살아있는 스타일 가이드 |

## 사용법
```html
<link rel="stylesheet" href="src/tokens.css">
<link rel="stylesheet" href="src/components.css">
```
브랜드를 바꾸려면 `tokens.css`의 `--signal-*`, `--paper-*`, `--ink-*`만 수정합니다. 컴포넌트는 시맨틱 토큰(`--color-*`)만 참조합니다.

## 원칙
1. **절제** – 강조색(`--color-accent`)은 화면당 하나의 핵심 행동에만 사용
2. **리듬** – 간격은 4px 배수(`--space-*`), 글자 크기는 `--text-*` 스케일만 사용
3. **접근성** – 본문 대비 4.5:1 이상, 터치 영역 44px 이상, `:focus-visible` 유지
4. **한글 우선** – `word-break: keep-all`, 본문 행간 1.65, 본문 폭 62ch

## 컬러 대비 (WCAG)
| 조합 | 라이트 | 다크 |
|---|---|---|
| 본문 / 배경 | 17.3 | 16.7 |
| 보조 텍스트 / 배경 | 6.2 | 8.3 |
| 강조색 / 배경 | 5.0 | 6.7 |
| 강조색 위 텍스트 | 5.4 | 6.5 |

`--color-text-faint`(3.5:1)는 18px 이상 큰 글자·장식에만 사용합니다.

## 컴포넌트
Button(`.btn`, `--accent/--ghost/--sm/--lg`), Link, Field/Input/Textarea/Select, Tag, Alert, Card, Project tile, Nav.

## 다크 모드
OS 설정을 따르며, `<html data-theme="light|dark">`로 강제할 수 있습니다.

## Do / Don't
- Do: 제목에는 `text-wrap: balance`, 세리프 이탤릭은 문장 속 한 단어만
- Don't: 하드코딩 색상·px 간격, 한 화면에 강조 버튼 둘 이상, 아이콘만 있는 버튼(라벨 필수)
