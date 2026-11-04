# Task Judgment Lite — 사용법

범용 코딩·데이터·의사결정 스킬 1개. 원본 시험 문제, 답안, 개인 정보, 외부 API 호출 코드 없음.

## 설치 (Codex 프로젝트 루트에서)

```bash
git clone --depth 1 https://github.com/kwonmins/skai.git skai-lite
mkdir -p .agents/skills
cp -R skai-lite/.agents/skills/task-judgment-lite .agents/skills/
```

Windows PowerShell:

```powershell
git clone --depth 1 https://github.com/kwonmins/skai.git skai-lite
New-Item -ItemType Directory -Force .agents/skills | Out-Null
Copy-Item -Recurse skai-lite/.agents/skills/task-judgment-lite .agents/skills/
```

**중요:** Codex를 실행할 작업 프로젝트의 `.agents/skills` 폴더로 복사해야 한다. 스킬이 보이지 않으면 Codex를 새로 시작한다.

## 사용

```text
$task-judgment-lite
start: 현재 제공된 과제의 파일을 직접 읽고 G/R/F/J/V로 사실, 규칙,
불확실성, 판단 근거를 정리해. 임의 규칙을 만들지 말고
필수 결과물과 검증 방법부터 확인해.
```

오류가 있을 때: `$task-judgment-lite debug: 오류 원인부터 재현·추적해줘.`

제출 전: `$task-judgment-lite verify: 테스트 실행 증거, 결과 형식, 미검증 항목을 확인해줘.`

## 출처/이용 범위
- [Superpowers](https://github.com/obra/superpowers): debugging, verification (MIT)
- [Ontology-Driven AI Data Management Skills](https://github.com/SuperChason/ontology-driven-ai-data-management-skills): semantic modeling (MIT)

공개 워크플로를 참고해 별도로 만든 축약 안내문이다. 원문 도구의 실행 기능을 복제하지 않는다.

실제 시험 규정이 우선하며, 문제 데이터·답안을 외부로 전송하거나 자동 push하지 않는다.
