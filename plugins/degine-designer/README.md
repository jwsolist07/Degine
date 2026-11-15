# degine-designer

어떤 프로젝트에서든 디자인 업무가 나오면 시니어 디자이너 기준으로 수행하게 하는 Claude Code 플러그인.

## 구성
- **skill `pro-design`**: 디자인 관련 요청 시 자동 적용 (맥락 파악 → 컨셉 → 토큰 기반 구현 → 시각 검증 → 보고)
- **agent `designer`**: 큰 디자인 작업을 위임
- **command `/design-review`**: 화면 비평과 개선안

## 설치
```
/plugin marketplace add jwsolist07/Degine
/plugin install degine-designer@degine
```
