# ENUMA Sales Dashboard — Project Memory

## 프로젝트 개요
ENUMA 회사의 디스트리뷰터 영업 파이프라인을 시각화하는 세일즈 대시보드 웹사이트.

---

## GitHub 저장소 정보
- **Repository:** https://github.com/Dasom-pr/enumaID-Salesdashboard
- **GitHub Pages (공개 URL):** https://Dasom-pr.github.io/enumaID-Salesdashboard
- **계정:** Dasom-pr (dasomdari.choi@gmail.com)
- **Token:** (별도 보관 — GitHub Settings > Developer Settings > Personal Access Tokens에서 확인)

---

## 로컬 프로젝트 경로
```
C:\Users\ASUS\OneDrive\Desktop\클로드_코워크 연습_ 기사방송보도\
```

---

## 폴더 구조
```
프로젝트 루트/
├── CLAUDE.md                                        ← 이 파일
├── index.html                                       ← GitHub Pages가 서빙하는 메인 파일
├── server.js                                        ← 로컬 개발 서버 (port 3000)
├── sales-dashboard/
│   └── index.html                                   ← 대시보드 본체 (index.html과 동일 내용 유지)
├── 2026_BD PIPELINE ENUMA - DISTRIBUTOR INFO.csv
├── 2026_BD PIPELINE ENUMA - Jan_Revenue EST-2026.csv
├── 2026_BD PIPELINE ENUMA - Feb_Revenue EST-2026.csv
├── 2026_BD PIPELINE ENUMA - Target 2026.csv
└── 2026_BD PIPELINE ENUMA - PRICE.csv
```

> ⚠️ **중요:** GitHub Pages는 루트의 `index.html`을 서빙함.
> `sales-dashboard/index.html` 수정 시 루트 `index.html`도 함께 동일하게 업데이트해야 함.

---

## 로컬 개발 서버 실행
```bash
cd "C:\Users\ASUS\OneDrive\Desktop\클로드_코워크 연습_ 기사방송보도"
node server.js
# → http://localhost:3000 에서 확인
```

---

## GitHub Push 방법
```bash
cd "C:\Users\ASUS\OneDrive\Desktop\클로드_코워크 연습_ 기사방송보도"
git add index.html sales-dashboard/index.html
git commit -m "커밋 메시지"
git push
```

---

## 데이터 파일 구조 요약

### Target 2026.csv
- 팀(Alvan/Adi/Ade/Ala/Ari/Ammar/Yus/Tabitha)별 연간 목표
- 디스트리뷰터별 세부 목표 금액 (IDR)
- **총 연간 목표: Rp 16,010,000,000**

### Jan/Feb_Revenue EST-2026.csv
- BD 파이프라인 딜 목록
- 주요 컬럼: CLIENT, Partner(디스트리뷰터), Category, 월별 Revenue Forecast, Status
- Status 종류: `Contracted` / `Budgeted` / `Work on Budget` / `New Approach` / `Dropped`
- Category: `LOCAL GOVERNMENTS` / `SCHOOL SALES` / `MoE-DIKDASMEN` / `NGO/GRANT` / `CSR`

### DISTRIBUTOR INFO.csv
- 디스트리뷰터 기본 정보: 이름, 지역, 분류, 계약 상태

### PRICE.csv
- 실제 체결된 계약 가격 및 라이선스 수 내역

---

## 디스트리뷰터별 목표 금액 (Target 2026.csv 기준)
| 디스트리뷰터 | 목표 (IDR) |
|---|---|
| IKM | 3,400,000,000 |
| CV Tirta | 1,125,000,000 |
| Property 21 | 1,125,000,000 |
| Agung | 1,161,000,000 |
| Jabal Rahmah | 1,000,000,000 |
| CV Jabal Rahmah | 1,000,000,000 |
| Andi Offset | 1,000,000,000 |
| CV Keenan | 1,000,000,000 |
| CV Putra Dange Jaya | 630,000,000 |
| MKP | 460,000,000 |
| Mikail Sati | 280,000,000 |
| CV ARDI | 240,000,000 |
| Andreas | 500,000,000 |
| ShaktaVisi | 50,000,000 |

---

## 현재 대시보드 기능 (최신 버전 기준)

### 탭 구성
1. **Dashboard** — KPI 카드 + 분기별 매출 예측 + 카테고리 도넛 차트 + 딜 상태 차트 + 파이프라인 테이블
2. **By Distributor** — 디스트리뷰터별 Target vs Contracted 차트 + 테이블 (클릭 시 딜 상세 모달)
3. **By Region** — 지역별 매출 현황

### KPI 카드 (3개)
- **Total Pipeline** — 전체 파이프라인 합계
- **Achievement Rate** — Contracted 금액 ÷ Total Pipeline × 100%
- **Contracted Amount** — 계약 완료된 딜 합계

### 차트
- **Quarterly Revenue Forecast** — Q1/Q2/Q3/Q4 2026 분기별 예측
- **Pipeline by Category** — 도넛 차트
- **Pipeline by Status** — 수평 막대 그래프
- **Distributor Target vs Contracted** — By Distributor 탭에서 확인

---

## 작업 히스토리 (Git 커밋 순서)
| 커밋 | 내용 |
|---|---|
| `b0f2883` | 최초 파일 업로드 (한국어 원본) |
| `2c43fde` | 영어 전환 + 분기별 차트 + 디스트리뷰터 모달 등 7가지 개선 |
| `e537bd9` | 루트 index.html 동기화 |
| `51b0f41` | 최신 영어 버전 복원 (현재 버전) |

---

## 앞으로 해야 할 작업 (미완료 항목)
- [ ] 디스트리뷰터 추가/삭제 기능
- [ ] 디스트리뷰터별 매출 보기 개선
- [ ] 지역별 매출 보기 기능 완성
- [ ] 실제 CSV 데이터를 대시보드에서 업로드/연동하는 기능
