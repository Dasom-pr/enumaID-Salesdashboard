# 📋 ENUMA Sales Dashboard — Project Note

> 마지막 업데이트: 2026-03-18
> 다음 세션에서 이 파일을 Claude에게 보여주면 바로 작업을 이어갈 수 있습니다.

---

## ✅ 현재 상태 (Last Session Summary)

- 세일즈 대시보드 웹사이트 제작 완료 및 GitHub Pages로 배포
- 최신 버전: 영어 UI, 분기별 차트, 디스트리뷰터 모달 포함
- **현재 라이브 URL:** https://Dasom-pr.github.io/enumaID-Salesdashboard

---

## 🗂️ 프로젝트 핵심 정보

| 항목 | 내용 |
|---|---|
| 로컬 경로 | `C:\Users\ASUS\OneDrive\Desktop\클로드_코워크 연습_ 기사방송보도\` |
| GitHub | https://github.com/Dasom-pr/enumaID-Salesdashboard |
| 라이브 URL | https://Dasom-pr.github.io/enumaID-Salesdashboard |
| 로컬 서버 | `node server.js` → http://localhost:3000 |
| 메인 파일 | `index.html` (루트) + `sales-dashboard/index.html` (항상 동시 수정) |

---

## 🔧 마지막으로 한 작업

1. ✅ 영어로 전체 UI 변환
2. ✅ Jan/Feb 스냅샷 탭 제거
3. ✅ 연간 목표 KPI 카드 제거
4. ✅ 달성률 계산 수정 (Contracted ÷ Total Pipeline)
5. ✅ "Payment received" 상태 제거 → Contracted로 통합
6. ✅ 월별 → 분기별(Q1/Q2/Q3/Q4) 차트 변경
7. ✅ By Distributor 탭에 Target vs Contracted 차트 + 클릭 시 딜 상세 모달 추가
8. ✅ CLAUDE.md 및 project_note.md 작성

---

## 🚀 다음에 할 작업 (Todo)

| 우선순위 | 작업 | 메모 |
|---|---|---|
| P1 | 디스트리뷰터 추가 / 삭제 기능 | UI에서 직접 추가·삭제 가능하도록 |
| P1 | CSV 파일 업로드 연동 | 현재 데이터가 JS에 하드코딩되어 있음 |
| P2 | 지역별 매출 보기 (By Region 탭) 완성 | 현재 탭은 있으나 기능 미완성 |
| P3 | 팀원별 성과 보기 페이지 추가 | Alvan/Adi/Ade 등 팀원별 분리 |

---

## 💬 다음 세션 시작 멘트 예시

```
이 project_note.md 파일 읽고 이어서 작업해줘.
오늘은 [할 작업 내용]을 하고 싶어.
```

---

## ⚠️ 작업 시 주의사항

- `index.html`(루트) 와 `sales-dashboard/index.html` **항상 동시에 수정**
- 수정 후 `git push`까지 완료
- GitHub 토큰은 절대 파일에 기록 금지
- 배포 후 반영까지 1~5분 소요 → Actions 탭 확인
- 캐시 문제 시 `Ctrl+Shift+R` 강제 새로고침
