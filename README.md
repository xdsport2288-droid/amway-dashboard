# 암웨이 운영본부 25cent ride 모바일 관제 대시보드 (Mobile Web Dashboard)

> **GitHub Pages(무료 호스팅) 100% 호환 · Zero-Backend 정적 웹 앱**  
> 스마트폰 브라우저에서 실제 모바일 네이티브 앱(iOS/Android)과 동일한 가독성과 UX를 제공하는 100% 반응형 웹 대시보드입니다.

---

## 📱 주요 특징 및 UI/UX 디자인
1. **100% 모바일 반응형 & App-Like UX**:
   - 하단 탭 내비게이션 바 (홈 요약, 주문 관제, 창고 재고, 조직·피드)
   - iOS 스타일 바텀 시트 모달 (주문 16열 표준 상세 항목 표출 및 원터치 클립보드 복사)
   - 모바일 Safe-Area(노치/홈바) 완벽 대응 및 부드러운 터치 피드백
2. **Zero-Backend (서버/DB 불필요)**:
   - 파이썬, Node.js 서버나 DB 없이 순수 `HTML`, `CSS`, `JavaScript`로만 구동.
   - GitHub Pages, Netlify, Vercel 등 어디서나 무료 호스팅 가능.
3. **MoviqAI 및 암웨이 운영본부 표준 체계 반영**:
   - 누적 실적 및 당월 실적 실시간 KPI 카드
   - 전국 10대 공식 센터별 3단계(안전/부족주의/재고없음) 가용 재고 게이지
   - 주문 현황 실시간 검색 및 상태별(스케줄확정, 접수완료, 배송완료, 접수대기, 취소) 필터링
   - 4대 실무 부서(CS, 분석, 자동화, 운영) 및 듀얼 실장 가동 상태

---

## 📁 파일 구조
```text
mobile_dashboard/
├── index.html       # 메인 모바일 웹 대시보드 HTML 마크업
├── style.css        # 모바일 앱 전용 다크모드 및 Glassmorphism 디자인 시스템
├── script.js        # 탭 전환, 검색/필터링, 바텀시트, 클립보드 복사 등 인터랙션
├── data.js          # 대시보드 데이터 모듈 (수치 및 주문/재고 데이터 분리)
└── README.md        # 가이드 문서
```

---

## 🚀 GitHub Pages 무료 호스팅 배포 방법 (3단계)

### 방법 A: 신규 GitHub 저장소로 배포할 때 (권장)
1. GitHub에서 새 저장소(예: `amway-mobile-dashboard`)를 생성합니다 (Public 또는 Private).
2. `mobile_dashboard` 폴더 안의 파일들(`index.html`, `style.css`, `script.js`, `data.js`)을 해당 저장소의 루트에 업로드(git push)합니다.
3. GitHub 저장소의 **[Settings] ➔ [Pages]** 메뉴로 이동합니다.
4. **Branch**를 `main` (또는 `master`) / `/(root)`로 선택하고 **[Save]** 버튼을 누릅니다.
5. 약 1분 후 `https://<깃허브_아이디>.github.io/<저장소_이름>/` 주소로 모바일 최적화 웹 대시보드가 즉시 활성화됩니다!

### 방법 B: 기존 저장소의 `/docs` 폴더로 배포할 때
1. 저장소의 `docs/` 폴더 안에 위 4개 파일을 복사합니다.
2. **[Settings] ➔ [Pages]**에서 Branch를 `main`, 폴더를 `/docs`로 설정 후 저장합니다.

---

## 🔄 데이터 갱신 방법 (`data.js`)
- 매일 Daily 리포트나 재고 수치가 갱신될 때, `data.js` 파일의 `kpis`, `warehouses`, `orders` 내용만 수정하여 커밋하면 웹 화면에 실시간으로 즉시 반영됩니다.
